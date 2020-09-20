<template>
  <div class="showcase-container">
    <button
      @click="showRightArrow"
      :class="[{ hideArrow: hideLeftArrow }, 'arrowBtn']"
    >
      <img alt="left arrow" src="../assets/leftArrow.svg" class="arrow" />
    </button>
    <a
      v-for="game in games"
      :key="game.id"
      :class="{ hideGame: game.hide }"
      :href="game.link"
      >{{ game.name }}</a
    >
    <button
      @click="showLeftArrow"
      :class="[{ hideArrow: hideRightArrow }, 'arrowBtn']"
    >
      <img alt="right arrow" src="../assets/rightArrow.svg" class="arrow" />
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      games: [
        {
          name: "Tryangle",
          link: "#",
          id: 1,
          hide: false,
        },
        {
          name: "BagRPG",
          link: "#",
          id: 2,
          hide: true,
        },
      ],
      hideLeftArrow: true,
      hideRightArrow: false,
    };
  },
  methods: {
    showLeftArrow() {
      this.hideLeftArrow = !this.hideLeftArrow;
      this.hideRightArrow = !this.hideRightArrow;
      this.games[0].hide = true;
      this.games[1].hide = false;
    },
    showRightArrow() {
      this.hideLeftArrow = !this.hideLeftArrow;
      this.hideRightArrow = !this.hideRightArrow;
      this.games[0].hide = false;
      this.games[1].hide = true;
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
  a {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 3em;
    padding: 2em 1em;
    font-size: calc(2rem + 2vw);
    border: 10px solid #fff;
    color: #fff;
    text-decoration: none;
    text-align: center;
    @include md {
      width: 4em;
    }
  }
  button {
    outline: 0;
    cursor: pointer;
  }
  .hideArrow {
    visibility: hidden;
  }
  .arrowBtn {
    margin: 0 1em;
    background: none;
    border: 0;
    @include md {
      margin: 0 2em;
    }
    > img {
      width: 2em;
      @include md {
        width: 4em;
      }
    }
  }
  .hideGame {
    display: none;
  }
}
</style>
