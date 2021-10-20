<template>
  <div>
    <v-data-table :headers="headers" :items="movies" class="elevation-1 black--te"></v-data-table>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      movies: [],
      headers: ["Title", "Director", "Genre", "Year", "Rated", "Plot"]
    };
  },
  methods: {
    async getMovies() {
      const movies = await axios({ method: "GET", url: "http://127.0.0.1:3000/movies" });

      movies.forEach(el => {
        this.movies.push(el);
      });
    }
  },
  created() {
    this.getMovies();
  }
};
</script>

<style lang="css" scoped></style>
