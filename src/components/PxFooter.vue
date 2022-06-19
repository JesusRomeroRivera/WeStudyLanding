<template>
  <footer class="Footer">
    <div class="Footer--Info">
      <img class="Header--Logo" src="@/assets/Logo.png" alt="westudy" />
      <p class="Footer--Text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Massa
        ullamcorper consectetur arcu odio elit.
      </p>
    </div>
    <div class="Footer--Container">
      <h3 class="Footer--Title">Secciones</h3>
      <p class="Footer--Text">Inicio</p>
      <p class="Footer--Text">Nosotros</p>
      <p class="Footer--Text">Nuestra App</p>
      <p class="Footer--Text">Contáctanos</p>
    </div>
    <div class="Footer--Container">
      <h3 class="Footer--Title">Redes Sociales</h3>
      <p class="Footer--Text">WeStudy_fb</p>
      <p class="Footer--Text">WeStudy_ig</p>
    </div>
    <div class="Footer--Container">
      <h3 class="Footer--Title">Contacto</h3>
      <p class="Footer--Text">902955015</p>
      <p class="Footer--Text">westudy@gmail.com</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "px-footer",
  data() {
    return {
      buttonColor: "black",
    };
  },
  computed: {
    whatHeader() {
      return this.$route.name == "Home";
    },
  },
};
</script>

<style scoped>
.Footer {
  width: 100vw;
  height: 320px;
  padding: 0 8vw;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  box-sizing: border-box;
}
.Footer--Info {
  width: 25vw;
}
.Footer--Container {
  width: 15vw;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  gap: 1.5rem;
}
.Footer--Title {
  margin: 0;
  font-weight: 700;
  font-size: 1.6rem;
  color: var(--off-black);
}
.Footer--Text {
  margin: 0;
  font-weight: 600;
  font-size: 1.6rem;
  color: var(--strong-gray);
}
.Header--Logo {
  margin: 0;
  margin-bottom: 3rem;
}
</style>
