<route lang="json">
{
  "meta": {
    "layout": "customers"
  }
}
</route>

<template>
  <v-row>
    <v-col cols="8">
      <AppPageHeader :breadcrumbs="breadcrumbs" />

      <CustomerTicketSingleContent />

      <CustomerTicketSingleReplyForm />

      <!-- Ticket replies with pagination -->
      <CustomerTicketSingleReplies v-for="index in 5" :key="index" />
    </v-col>

    <v-col cols="4">
      <CustomerTicketSingleDetails />
    </v-col>
  </v-row>
</template>

<script setup>
const breadcrumbs = [
  {
    title: "All Tickets",
    disabled: false,
    to: "/customer/tickets",
  },
  {
    title: "#3231",
    disabled: true,
  },
];
</script>
