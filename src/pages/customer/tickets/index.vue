<route lang="json">
{
  "meta": {
    "layout": "customers"
  }
}
</route>

<template>
  <div>
    <AppPageHeader heading="Tickets" />

    <AppCard>
      <template #card-text>
        <v-data-table-server
          v-model:items-per-page="itemsPerPage"
          :headers="headers"
          :items="serverItems"
          :items-length="totalItems"
          :loading="loading"
          @update:options="loadItems"
        ></v-data-table-server>
      </template>
    </AppCard>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { useQuery } from "@tanstack/vue-query";
import axios from "axios";

const itemsPerPage = ref(6);
const headers = ref([
  {
    title: "No.",
    align: "start",
    sortable: false,
    key: "id",
  },
  {
    title: "Email",
    align: "start",
    sortable: false,
    key: "email",
  },
  {
    title: "First Name",
    align: "start",
    sortable: false,
    key: "first_name",
  },
  {
    title: "Last Name",
    align: "start",
    sortable: false,
    key: "last_name",
  },
]);
const serverItems = ref([]);
const totalItems = ref(0);
const loading = ref(true);
const currentPage = ref(1);

async function fetchItems({ queryKey }) {
  const [_key, { page }] = queryKey;

  console.log(page);

  try {
    const { data } = await axios.get(
      `https://reqres.in/api/users?page=${page}`
    );

    serverItems.value = data.data;
    totalItems.value = data.total;

    return Promise.resolve(data);
  } catch (err) {
    return Promise.reject(err);
  } finally {
    loading.value = false;
  }
}

const { isPending, isFetching, isError, data, error, refetch } = useQuery({
  queryKey: ["users", { page: currentPage.value }],
  queryFn: fetchItems,
});

function loadItems({ page }) {
  if (page > 1) {
    currentPage.value = page;
  }
}
</script>
