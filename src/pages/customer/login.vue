<template>
  <v-container class="fill-height justify-center">
    <v-sheet width="420">
      <h1 class="text-h4 font-weight-medium text-indigo mb-5">
        Customer Login
      </h1>

      <v-form>
        <AppCard>
          <template #card-text>
            <AppInputLabel>Username</AppInputLabel>

            <v-text-field placeholder="Enter your username"></v-text-field>

            <AppInputLabel>Password</AppInputLabel>

            <v-text-field
              :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
              :type="visible ? 'text' : 'password'"
              placeholder="Enter your password"
              @click:append-inner="visible = !visible"
            ></v-text-field>
          </template>

          <template #card-actions>
            <v-spacer></v-spacer>
            <AppBtn to="/customer/dashboard"> Log In </AppBtn>
          </template>
        </AppCard>
      </v-form>

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
