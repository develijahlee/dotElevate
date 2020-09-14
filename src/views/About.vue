<template>
  <div class="about">
    <h1>This is an about page</h1>
    <AboutWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import AboutWorld from "@/components/AboutWorld.vue";

export default {
  name: "about",
  components: {
    AboutWorld,
  },
};
</script>
