<template>
  <div class="home">
    <p>{{ name }}</p>
    <img alt="invader" src="../assets/invader.png" class="invader" />
    <h2>Our Games</h2>
    <Showcase />
  </div>
</template>

<script>
import Showcase from "@/components/Showcase.vue";

export default {
  name: "Home",
  components: {
    Showcase,
  },
};
</script>

<style lang="scss">
@import "../styles.scss";
.invader {
  animation: float 2s infinite;
  width: 6em;
  @include md {
    width: 8em;
  }
}
h2 {
  font-size: calc(3rem + 2vw);
  margin: 0.5em 0;
  @include md {
    font-size: calc(4rem + 2vw);
  }
}
</style>
