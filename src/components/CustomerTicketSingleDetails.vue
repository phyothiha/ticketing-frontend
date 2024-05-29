<template>
  <AppCard class-override="px-4 py-4">
    <template #card-text>
      <h4 class="text-h6 mb-5">Ticket Details</h4>

      <v-table density="comfortable">
        <tbody>
          <tr class="text-caption">
            <td class="font-weight-medium">ID</td>
            <td>#3231</td>
          </tr>
          <tr class="text-caption">
            <td class="font-weight-medium">Status</td>
            <td>
              <v-chip class="flex-shrink-0" size="x-small">
                In Progress
              </v-chip>
            </td>
          </tr>
          <tr class="text-caption">
            <td class="font-weight-medium">Created At</td>
            <td>2024-05-29 12:11:00</td>
          </tr>
          <tr class="text-caption">
            <td class="font-weight-medium">Updated At</td>
            <td>2024-05-29 15:30:00</td>
          </tr>
          <tr class="text-caption">
            <td class="font-weight-medium">Assigned</td>
            <td>John, Stacy, Climatte, Uzi, Foleyn</td>
          </tr>
        </tbody>
      </v-table>
    </template>
  </AppCard>
</template>

<style scoped>
table {
  table-layout: fixed;
}

.v-table .v-table__wrapper > table > tbody > tr:not(:last-child) > td,
.v-table .v-table__wrapper > table > tbody > tr:not(:last-child) > th {
  border-bottom: 0 !important;
}

.v-table > .v-table__wrapper > table > tbody > tr > td {
  padding: 0 16px 0 0 !important;
}
.v-table > .v-table__wrapper > table > tbody > tr > td:last-child {
  padding-right: 0 !important;
}
</style>
