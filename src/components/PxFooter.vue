<template>
  <footer class="Footer">
    <a class="Footer--Logo" href="#Inicio">
      <img src="../assets/logo.png" alt="westudy" />
    </a>
    <div class="Footer--Container">
      <h3 class="Footer--Title">Secciones</h3>
      <a class="Footer--Text" href="#Inicio">Inicio</a>
      <a class="Footer--Text" href="#Beneficios">Beneficios</a>
      <a class="Footer--Text" href="#Secciones">Secciones</a>
      <a class="Footer--Text" href="#Solucion">¿Cómo funciona?</a>
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
  height: 24rem;
  padding: 4rem 8vw;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  box-sizing: border-box;
}
.Footer--Logo{  
  height: 26%;
}
.Footer--Logo img{
  height: 100%;
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
  text-decoration: none;
}
.Header--Logo {
  margin: 0;
  margin-bottom: 3rem;
}
</style>
