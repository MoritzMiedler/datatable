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

      <v-btn href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank" text>
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
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
