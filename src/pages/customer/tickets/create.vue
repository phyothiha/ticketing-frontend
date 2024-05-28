<route lang="json">
{
  "meta": {
    "layout": "customers"
  }
}
</route>

<template>
  <div>
    <AppPageHeading> Add New Ticket </AppPageHeading>

    <v-form>
      <AppCard>
        <template #card-text>
          <AppInputLabel>Title</AppInputLabel>

          <v-text-field placeholder="Enter your title"></v-text-field>

          <AppInputLabel>Content</AppInputLabel>

          <v-textarea placeholder="Write your message"></v-textarea>
        </template>

        <template #card-actions>
          <v-spacer></v-spacer>
          <AppBtn to="/customer/dashboard"> Publish </AppBtn>
        </template>
      </AppCard>
    </v-form>
  </div>
</template>

<script setup>
//
</script>
