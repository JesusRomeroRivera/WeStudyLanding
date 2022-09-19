<template>
  <header class="Header">
    <a class="Header--LogoContainer" href="#Inicio">
      <img class="Header--Logo" src="../assets/logo.png" alt="westudy" />
    </a>
    <div class="Header--List">
      <a class="Header--List--Ancle" href="#Inicio">Inicio</a>
      <a class="Header--List--Ancle" href="#Beneficios">Beneficios</a>
      <a class="Header--List--Ancle" href="#Secciones">Secciones</a>
      <a class="Header--List--Ancle" href="#Solucion">¿Cómo funciona?</a>
    </div>
    <a href="#Formulario">
      <px-button :color="buttonBlue">¡Estoy interesado/a!</px-button>
    </a>
  </header>
</template>

<script>
import PxButton from "@/components/PxButton.vue";

export default {
  name: "px-header",
  props: ["login"],
  components: {
    PxButton,
  },
  data() {
    return {
      buttonBlue: "blue",
      buttonWhite: "white",
    };
  },
  computed: {
    whatHeader() {
      return this.$route.name == "Home";
    },
  },
  methods: {
    goHome() {
      this.$store.state.userId = 0;
      this.$router.push({
        path: "/",
      });
    },
    navToggle() {
      const menuBtn = document.querySelector(".menu-btn");
      this.navAppears = !this.navAppears;
      if (!this.menuOpen) {
        menuBtn.classList.add("open");
        this.menuOpen = true;
      } else {
        menuBtn.classList.remove("open");
        this.menuOpen = false;
      }
    },
  },
};
</script>

<style scoped>
.Header {
  width: 100vw;
  height: var(--header-height);
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 8vw;
  position: fixed;
  background-color: white;
}
.Header--LogoContainer{
  height: 60%;
}
.Header--Logo {
  margin: 0;
  height: 100%;
}
.Header--List {
  width: 42vw;
  display: flex;
  justify-content: space-between;
  margin: 0;
  padding: 0;
}
.Header--List--Ancle {
  text-decoration: none;
  color: var(--strong-gray);
  font-family: var(--principal-font);
  font-size: 1.6rem;
  font-weight: 500;
  transition: 0.4s;
  padding: 0.6rem 1.8rem;
  background-color: #DCEBFF;
  border-radius: 1.6rem;
}
.Header--List--Ancle:hover {
  transition: 0.4s;
  color: var(--principal-color);
}
</style>
