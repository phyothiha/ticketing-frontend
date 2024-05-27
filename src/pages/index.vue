<template>
  <v-container class="fill-height justify-center">
    <div class="d-flex flex-column">
      <div class="text-center mb-10">
        <div class="text-h5 font-weight-light mb-3">Welcome to</div>

        <h1 class="text-h4 font-weight-bold text-indigo">
          Customer Issue Management System
        </h1>
      </div>

      <div class="text-center mb-5">
        <p>Are you?</p>
      </div>

      <div class="d-flex align-center justify-center ga-3">
        <AppBtn to="/customer/login">Customer</AppBtn>

        <AppBtn>Staff</AppBtn>
      </div>
    </div>
  </v-container>
</template>

<script setup>
//
</script>
