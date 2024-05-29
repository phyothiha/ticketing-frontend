<template>
  <v-breadcrumbs density="compact" :items="items" class="text-body-2 px-0">
    <template v-slot:title="{ item }">
      {{ item.title }}
    </template>
  </v-breadcrumbs>
</template>

<script setup>
defineProps({
  items: Array,
});
</script>
