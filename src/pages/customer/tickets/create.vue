<route lang="json">
{
  "meta": {
    "layout": "customers"
  }
}
</route>

<template>
  <div>
    <AppPageHeader heading="Add New Ticket" :breadcrumbs="breadcrumbs" />

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
const breadcrumbs = [
  {
    title: "All Tickets",
    disabled: false,
    to: "/customer/tickets",
  },
  {
    title: "Add Ticket",
    disabled: true,
  },
];
</script>
