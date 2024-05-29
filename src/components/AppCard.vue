<template>
  <v-card border="thin" variant="text" rounded="lg" :class="computedClass">
    <v-card-text class="pa-0">
      <slot name="card-text"></slot>
    </v-card-text>

    <v-card-actions class="pa-0 mt-1">
      <slot name="card-actions"></slot>
    </v-card-actions>
  </v-card>
</template>

<script setup>
import { computed } from "vue";

const props = defineProps({
  classOverride: String,
});

const computedClass = computed(() => {
  if (props.classOverride) {
    return props.classOverride;
  }

  return "px-6 py-6";
});
</script>
