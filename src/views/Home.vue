<template>
  <section class="Home">
    <px-curve></px-curve>
    <px-principal></px-principal>
    <px-benefit></px-benefit>
    <px-sections></px-sections>
    <px-solution></px-solution>
    <px-contact></px-contact>
  </section>
</template>

<script>
import PxPrincipal from "@/components/PxPrincipal.vue";
import PxBenefit from "@/components/PxBenefit.vue";
import PxContact from "@/components/PxContact.vue";
import PxSolution from "@/components/PxSolution.vue";
import PxSections from "@/components/PxSections.vue";
import PxCurve from "@/components/PxCurve.vue";

export default {
  name: "home-view",
  components: {
    PxPrincipal,
    PxBenefit,
    PxContact,
    PxSolution,
    PxSections,
    PxCurve
  },
  data() {
    return {
      colorWhite: '#ffffff',
      lightBlue: '#DCEBFF',
      strongBlue: '#A4BAFF',
    };
  },
};
</script>
<style scoped>
.Home {
}
</style>
