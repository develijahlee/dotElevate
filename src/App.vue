<template>
  <div id="app">
    <nav id="nav">
      <div class="logo">
        <router-link to="/">.elevate</router-link>
      </div>
      <div>
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
      </div>
    </nav>
    <router-view />
    <footer>
      © dotElevate
    </footer>
  </div>
</template>

<style lang="scss">
@import "./styles.scss";
@font-face {
  font-family: "pixeboy";
  src: url("./assets/pixeboy.ttf") format("truetype");
}
html {
  height: 100%;
}
body {
  background: linear-gradient(-45deg, #7c5ed6, #0077a3, #23a6d5, #23d5ab);
  background-size: 400% 400%;
  animation: gradient 15s ease infinite;
  font-family: "pixeboy", Helvetica, Arial, sans-serif;
  font-size: calc(1rem + 1vw);
  color: #fff;
  text-align: center;
}
.logo {
  font-size: 1.5rem;
  @include xs {
    font-size: calc(2rem + 2vw);
  }
}
#nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5em 0;
  @include md {
    justify-content: space-around;
  }
  a {
    padding: 0.5em;
    color: #fff;
    text-decoration: none;
    &:not(:last-child) {
      margin-right: 0.5em;
    }
  }
}
footer {
  margin-top: 2em;
}
</style>
