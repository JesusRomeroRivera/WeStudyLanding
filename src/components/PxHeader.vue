<template>
  <header class="Header">
    <img class="Header--Logo" src="@/assets/Logo.png" alt="westudy" />
    <div class="Header--List">
      <a class="Header--List--Ancle" href="#inicio">Inicio</a>
      <a class="Header--List--Ancle" href="#nosotros">Nosotros</a>
      <a class="Header--List--Ancle" href="#app">Nuestra App</a>
      <a class="Header--List--Ancle" href="#contacto">Contacto</a>
    </div>
    <px-button :color="buttonBlue">Empecemos</px-button>
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
  height: 140px;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 8vw;
}
.Header--Logo {
  margin: 0;
}
.Header--List {
  width: 30vw;
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
  font-weight: 600;
  transition: 0.4s;
}
.Header--List--Ancle:hover {
  transition: 0.4s;
  color: var(--principal-color);
}
</style>
