<template>
  <v-app>
    <v-app-bar app class="white " dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="mt-15"
          src="/images/logo.png"
          transition="scale-transition"
          width="75"
        />
      </div>
      <span class="black--text text-h4"> MOVIES</span>
      <v-spacer></v-spacer>

      <v-btn href="https://www.imdb.com/movies-in-theaters/" target="_blank" text>
        <span class="mr-2 black--text">Latest Release</span>
        <v-icon class="black--text">mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  })
};
</script>
