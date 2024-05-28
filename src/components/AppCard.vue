<template>
  <v-card border="thin" variant="text" rounded="lg" class="px-6 py-6">
    <v-card-text class="pa-0">
      <slot name="card-text"></slot>
    </v-card-text>

    <v-card-actions class="pa-0 mt-1">
      <slot name="card-actions"></slot>
    </v-card-actions>
  </v-card>
</template>
