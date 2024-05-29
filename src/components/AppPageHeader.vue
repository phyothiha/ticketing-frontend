<template>
  <div class="mb-6">
    <AppPageHeading v-if="heading" :title="heading" />
    <AppPageBreadcrumb v-if="breadcrumbs" :items="breadcrumbs" />
  </div>
</template>

<script setup>
defineProps({
  heading: String,
  breadcrumbs: Array,
});
</script>
