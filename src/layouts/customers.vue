<template>
  <v-app>
    <v-app-bar elevation="0" border="thin">
      <template v-slot:prepend>
        <v-app-bar-title class="pl-3">Dashboard</v-app-bar-title>

        <div class="px-1"></div>

        <v-app-bar-nav-icon
          class="px-3 d-lg-none"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
      </template>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer">
      <v-list density="compact" nav>
        <v-list-item to="/customer/dashboard">
          <template v-slot:prepend>
            <v-icon icon="mdi-view-dashboard-outline"></v-icon>
          </template>

          <v-list-item-title> Dashboard </v-list-item-title>
        </v-list-item>

        <v-list-group>
          <template v-slot:activator="{ props }">
            <v-list-item v-bind="props">
              <template v-slot:prepend>
                <v-icon icon="mdi-ticket-outline"></v-icon>
              </template>

              <v-list-item-title> Tickets </v-list-item-title>
            </v-list-item>
          </template>

          <v-list-item to="/customer/tickets">
            <v-list-item-title> All Tickets </v-list-item-title>
          </v-list-item>

          <v-list-item to="/customer/tickets/create">
            <v-list-item-title> Add New Ticket </v-list-item-title>
          </v-list-item>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container class="pa-4 pa-sm-6 pa-md-8">
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: null,
    };
  },
};
</script>
