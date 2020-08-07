<template>
  <div>
    <h3>About DadJokes</h3>
    <p>This is an app that displays corny dad jokes</p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "About the App",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Best place for corny dad jokes"
        }
      ]
    };
  }
};
</script>
