<template>
  <div>
    <span>{{ movies }}</span>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      movies: []
    };
  },
  methods: {
    async getMovies() {
      const movies = await axios({ method: "GET", url: "http://127.0.0.1:3000/movies" });

      this.movies = movies.data;
    }
  },
  created() {
    this.getMovies();
  }
};
</script>

<style lang="css" scoped></style>
