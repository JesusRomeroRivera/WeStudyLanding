<template>
  <div id="app">
    <px-header />
    <home-view />
    <px-footer />
  </div>
</template>

<style>
:root {
  --principal-font: "Montserrat", serif;
  --off-white: #f3f7ff;
  --soft-gray: #d9d9d9;
  --strong-gray: #b3b3b3;
  --off-black: #0d0949;
  --principal-color: #5f75da;
  --header-height: 12.5vh;
  --blue-gradient: linear-gradient(0deg, #708ae4 0%, #a4b1ff 100%);
}
html {
  font-size: 62.5%;
  scroll-behavior: smooth;
  font-family: var(--principal-font);
  overflow-x: hidden;
}
body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: var(--principal-font);
}
</style>
<script>
import PxHeader from "@/components/PxHeader.vue";
import HomeView from "@/views/Home.vue";
import PxFooter from "@/components/PxFooter.vue";

export default {
  components: {
    PxHeader,
    PxFooter,
    HomeView,
  },
};
</script>
