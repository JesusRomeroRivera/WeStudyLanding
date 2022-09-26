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
  --off-black: #0d0949;
  --title-color: #ACF0FF;
  --light-blue: #DCEBFF;
  --strong-blue: #4479FF;
  --principal-color: #3101FF;
  --header-height: 7rem;
  --blue-gradient: linear-gradient(90deg, rgba(68,121,255,1) 0%, rgba(187,89,255,1) 100%);
  scroll-padding-top: var(--header-height);
  overflow-x: hidden;
}
@media (max-width: 1024px) {
  :root{
    --header-height: 13rem;
  }
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
h1{
  margin: 0;
}
p{
  margin: 0;
}
input{
  outline: none;
  border: 0;
}
textarea{
  outline: 0;
  border: 0;
}
svg{
  margin: 0;
  padding: 0;
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
