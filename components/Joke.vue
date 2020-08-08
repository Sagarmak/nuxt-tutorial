<template>
  <nuxt-link :to="'jokes/' + id">
    <div class="joke">
      {{ joke }}
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke", "id"]
};
</script>
<style>
.joke {
  padding: 1rem;
  border: 1px solid black;
  margin: 0.5rem 0;
}
</style>
