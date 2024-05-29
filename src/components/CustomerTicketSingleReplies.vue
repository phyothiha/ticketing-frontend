<template>
  <AppCard class="mb-5">
    <template #card-text>
      <!-- This section contains user profile image, user name and ticket created timestamps -->
      <div class="d-flex align-center ga-4 mb-10">
        <v-avatar color="indigo">
          <v-img
            alt="John"
            src="https://cdn.vuetifyjs.com/images/john.jpg"
          ></v-img>

          <!-- If there is no user profile image, use first two initials -->
          <!-- <span class="text-h5">JL</span> -->
        </v-avatar>
        <div>
          <div class="text-subtitle-2">John Lweis Hanthan</div>
          <em class="text-medium-emphasis">
            20 days ago (Wed, 22 Mar 2023 at 6:02 AM)
          </em>
        </div>
      </div>

      <!-- This section contains ticket content -->
      <div>
        Hi Ticket Management System Service Team,
        <br />
        <br />

        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolore ex qui
        quasi commodi adipisci illum blanditiis dolorum. Molestiae, commodi.
        Deleniti quidem officiis molestiae repellat natus laborum. Consequatur
        doloribus modi veniam.

        <br />
        <br />

        Best, <br />
        John
      </div>
    </template>
  </AppCard>
</template>

<script>
//
</script>
