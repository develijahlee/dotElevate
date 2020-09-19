<template>
  <div class="showcase-container">
    <button v-bind:class="{ leftArrow: noGames }">test</button>
    <a href="#">{{ game1 }}</a>
    <button>test</button>
  </div>
</template>

<script>
export default {
  noGames: true,
  data() {
    return {
      game1: "Coming Soon!!!!",
      game2: "Awesome Game",
      noGames: true,
    };
  },
  methods: {
    showGame() {
      alert(this.game1);
    },
  },
};
</script>

<style lang="scss">
@import "../styles.scss";
.showcase-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 1.5em;
  a {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 2em 1em;
    font-size: calc(2rem + 2vw);
    border: 10px solid #fff;
    color: #fff;
    text-decoration: none;
    text-align: center;
  }
  button {
    outline: 0;
    cursor: pointer;
  }
}
.leftArrow {
  visibility: hidden;
}
</style>
