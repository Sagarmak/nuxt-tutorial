<template>
  <div class="single-joke">
    <nuxt-link to="/jokes">Back to Jokes</nuxt-link>
    <h2>
      {{ joke }}
    </h2>
    <hr>
    <div class="id">{{ $route.params.id }}</div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "SingleJoke",
  data() {
    return {
      joke: {}
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };

    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );
      this.joke = res.data.joke;
    } catch (error) {
      console.log("created -> error", error);
    }
  }
};
</script>

<style>
h2 {
  padding: 1rem 0 0.5rem;
}
.id {
  padding: 0.5rem 0 0 0;
}
</style>
