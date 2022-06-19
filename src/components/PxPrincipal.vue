<template>
  <section class="Principal">
    <div class="Principal--Info">
      <h1 class="Principal--Title">
        Plataforma que te acerca a tu curso ideal
      </h1>
      <p class="Principal--Text">
        Plataforma que te acerca a tu curso ideal con nuestro buscador de manera
        eficiente, con procesos unificados y simplificados.
      </p>
      <px-button class="Principal--Button" :color="buttonBlue"
        >Contáctanos</px-button
      >
    </div>
    <img class="Principal--Image" src="@/assets/principalImage.png" alt="" />
  </section>
</template>

<script>
import PxButton from "@/components/PxButton.vue";

export default {
  name: "Principal",
  components: {
    PxButton,
  },
  data() {
    return {
      buttonBlue: "blue",
    };
  },
  computed: {
    showPopUpOpinion() {
      return this.$store.state.popUpOpinion;
    },
    showPopUpReport() {
      return this.$store.state.popUpReport;
    },
  },
  beforeMount() {},
};
</script>
<style scoped>
.Principal {
  width: 100vw;
  box-sizing: border-box;
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.Principal--Image {
  width: 100%;
}
.Principal--Info {
  padding: 0 3.2vw 10rem 8vw;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 3.2rem;
}
.Principal--Title {
  margin: 0;
  font-weight: 700;
  font-size: 4rem;
  color: var(--off-black);
}
.Principal--Text {
  margin: 0;
  font-weight: 600;
  font-size: 1.6rem;
  color: var(--strong-gray);
}
.Principal--Button {
  width: 20rem;
}
</style>
