<template>
  <v-container class="fill-height justify-center">
    <v-sheet width="420">
      <h1 class="text-h4 font-weight-medium text-indigo mb-5">
        Customer Login
      </h1>

      <AppCard>
        <AppInputLabel>Username</AppInputLabel>

        <v-text-field
          density="compact"
          placeholder="Enter your username"
          variant="outlined"
        ></v-text-field>

        <AppInputLabel>Password</AppInputLabel>

        <v-text-field
          :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
          :type="visible ? 'text' : 'password'"
          density="compact"
          placeholder="Enter your password"
          variant="outlined"
          @click:append-inner="visible = !visible"
        ></v-text-field>

        <AppBtn
          class="mt-5"
          size="large"
          variant="tonal"
          block
          to="/customer/dashboard"
        >
          Log In
        </AppBtn>
      </AppCard>

      <div class="text-right mt-5">
        <AppBtn
          class="text-right"
          variant="plain"
          color="blue-grey"
          to="/"
          prepend-icon="mdi-arrow-left"
        >
          Back to Home
        </AppBtn>
      </div>
    </v-sheet>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    visible: false,
  }),
};
</script>
