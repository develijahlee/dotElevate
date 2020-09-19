<template>
  <div class="about">
    <h1>About Us</h1>
    <p>
      We are a group of passionate game developers and designers trying to make
      the world more fun one byte at a time.
    </p>
    <p>
      We are a group of passionate game developers and designers trying to make
      the world more fun one byte at a time.
    </p>
    <p>
      We are a group of passionate game developers and designers trying to make
      the world more fun one byte at a time.
    </p>
    <p>
      We are a group of passionate game developers and designers trying to make
      the world more fun one byte at a time.
    </p>
  </div>
</template>

<style lang="scss">
@import "../styles.scss";
.about {
  padding: 0 calc(1em + 2vw);
  @include md {
    padding: 0 calc(5em + 2vw);
  }
  p {
    font-family: sans-serif;
    line-height: 1.5;
    text-align: left;
  }
}
</style>
