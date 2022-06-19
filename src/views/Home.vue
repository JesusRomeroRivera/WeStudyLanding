<template>
  <section class="Home">
    <px-principal></px-principal>
    <px-quote></px-quote>
    <px-solution></px-solution>
    <px-feature></px-feature>
    <px-contact></px-contact>
  </section>
</template>

<script>
import PxPrincipal from "@/components/PxPrincipal.vue";
import PxQuote from "@/components/PxQuote.vue";
import PxContact from "@/components/PxContact.vue";
import PxSolution from "@/components/PxSolution.vue";
import PxFeature from "@/components/PxFeature.vue";

export default {
  name: "home-view",
  components: {
    PxPrincipal,
    PxQuote,
    PxContact,
    PxSolution,
    PxFeature,
  },
  data() {
    return {};
  },
};
</script>
<style scoped>
.Home {
}
</style>
