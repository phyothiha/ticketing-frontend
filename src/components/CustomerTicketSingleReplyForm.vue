<template>
  <v-form>
    <AppCard class="my-10">
      <template #card-text>
        <AppInputLabel>Write Reply</AppInputLabel>

        <v-textarea placeholder="Please explain briefly"></v-textarea>
      </template>

      <template #card-actions>
        <v-spacer></v-spacer>
        <AppBtn to="/customer/dashboard"> Reply </AppBtn>
      </template>
    </AppCard>
  </v-form>
</template>

<script>
//
</script>
