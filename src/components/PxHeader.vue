<template>
  <header class="Header">
    <a class="Header--LogoContainer" href="#Inicio">
      <img class="Header--Logo" src="../assets/logo.png" alt="westudy" />
    </a>
    <div class="menu-btn" @click="toggleMenu">
      <div class="menu-btn__burger"></div>
    </div>
    <div class="Header--List">
      <a class="Header--List--Ancle" href="#Inicio">Inicio</a>
      <a class="Header--List--Ancle" href="#Beneficios">Beneficios</a>
      <a class="Header--List--Ancle" href="#Secciones">Secciones</a>
      <a class="Header--List--Ancle" href="#Solucion">¿Cómo funciona?</a>
    </div>
    <a class="Formulario--Container" href="#Formulario">
      <px-button class="Formulario--Buton" :color="buttonBlue">¡Estoy interesado/a!</px-button>
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
      menuOpen: false,
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
    toggleMenu(){
      const menuBtn = document.querySelector('.menu-btn');
      const nav = document.querySelector('.Header--List');
      const headerAll = document.querySelector('.Header');
      if(!this.menuOpen) {
        menuBtn.classList.add('open');
        this.menuOpen = true;
        nav.classList.add('active');
        headerAll.classList.add('active');
      } else {
        menuBtn.classList.remove('open');
        this.menuOpen = false;
        nav.classList.remove('active');
        headerAll.classList.remove('active');
      }
    }
  },
};
</script>

<style scoped> 
.menu-btn {
    display: none;
  justify-content: center;
  align-items: center;
  width: 60px;
  height: 40px;
  cursor: pointer;
  transition: all .5s ease-in-out;
} 
.menu-btn__burger {
    background: #4479FF;
    width: 50px;
    height: 6px;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(255,101,47,.2);
    transition: all .5s ease-in-out;
  }  
.menu-btn__burger::before,
.menu-btn__burger::after {
  content: '';
  position: absolute;
  width: 50px;
  height: 6px;
  background: #4479FF;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(255,101,47,.2);
  transition: all .5s ease-in-out;
}
.menu-btn__burger::before {
  transform: translateY(-16px);
}
.menu-btn__burger::after {
  transform: translateY(16px);
}
/* ANIMATION */
.menu-btn.open .menu-btn__burger {
  transform: translateX(-50px);
  background: transparent;
  box-shadow: none;
}
.menu-btn.open .menu-btn__burger::before {
  transform: rotate(45deg) translate(35px, -35px);
}
.menu-btn.open .menu-btn__burger::after {
  transform: rotate(-45deg) translate(35px, 35px);
}
.Header {
  z-index: 2;
  width: 100vw;
  height: var(--header-height);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 8vw;
  box-sizing: border-box;
  position: fixed;
  background-color: white;
}
.Header--LogoContainer{
  height: 60%;
}
.Header--Logo {
  margin: 0;
  height: 4.2rem;
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
@media (max-width: 1280px) {
  .Header--List {
    width: 47vw;
  }  
  .Header--List--Ancle {
    padding: 0.6rem 1.5rem;
  }
  .Formulario--Buton{
    padding-left: 2.4rem;
    padding-right: 2.4rem;
  }
}
@media (max-width: 1024px) {
  .Header--List {
    width: 70vw;
    grid-area: List;
    justify-self: center;
  }
  .Header{
    display: grid;
    grid-template-columns: 1fr 100px 1fr;
    grid-template-rows: 7rem 1fr;
    grid-template-areas: "Logo Burger Button" "List List List";
    height: var(--header-height);
  }
  .Header--List--Ancle {
    padding: 0.8rem 2rem;
  }
  .Formulario--Buton{
    padding-left: 3.5rem;
    padding-right: 3.5rem;
  }
  .Formulario--Container{
    justify-self: end;
    grid-area: Button;
  }
}
@media (max-width: 768px) {
  .menu-btn{
    display: flex;
    justify-self: center;
  }
  .Header{
    height: 7rem;
  }
  .Header.active{
    height: 13rem;
  }
  .Header--List {
    display: none;
    width: 80vw;
  }
  .Header--List.active {
    display: flex;
  }
  .Formulario--Buton{
    padding: 1rem 2rem;
  }
  .Header--List--Ancle {
    text-decoration: none;
    padding: 0.6rem 0;
    background-color: transparent;
  }
}
@media (max-width: 585px) {
  .menu-btn{
    grid-area: Button;
    justify-self: end;
  }
  .Header{
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 7rem 1fr;
    grid-template-areas: "Logo Button" "List List";
  }
  .Header.active{
    height: 15rem;
  }
  .Formulario--Container{
    display: none;
  }
  .Header--List.active {
    width: 100%;
    justify-self: center;
    display: grid;
    justify-items: center;
    align-items: center;
    grid-template-columns: 2fr 3fr;
    grid-template-rows: 1fr 1fr;
  }
}
</style>
