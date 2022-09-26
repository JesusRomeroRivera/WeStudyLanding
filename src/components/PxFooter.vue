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
      <a class="Footer--Text" href="https://www.instagram.com/westudy_ig/?hl=es">
        <img src="../assets/igIcon.png" alt="InstagramIcon">
        <span>@westudy_ig</span>
      </a>
      <a class="Footer--Text" href="">
        <img src="../assets/fbIcon.png" alt="">
        <span>WeStudy</span>
      </a>
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
  height: 4.2rem;
}
.Footer--Logo img{
  height: 100%;
}
.Footer--Container {
  width: auto;
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
  display: flex;
  align-items: center;
}
.Header--Logo {
  margin: 0;
}
.Footer--Text img{
  width: 20px;
  height: auto;
}
.Footer--Text span{
  margin-left: 5px;
}
@media (max-width: 1024px){
  .Footer--Container:nth-child(4){
    display: none;
  }
}
@media (max-width: 585px){
  .Footer--Container:nth-child(2){
    display: none;
  }
  .Footer{
    height: 16rem;
  }
  .Footer--Title {
    font-size: 1.4rem;
  }
  .Footer--Text {
    font-size: 1.2rem;
  }
}
</style>
