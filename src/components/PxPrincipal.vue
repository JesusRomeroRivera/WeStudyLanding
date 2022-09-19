<template>
  <section id="Inicio" class="Principal">
    <div class="Principal--Info">
      <h1 class="Principal--Title">
        Descubre la nueva web de búsqueda de 
        <span class="Principal--Title--SpecialWord">{{ typeValue }}</span>
        <span class="Cursor" :class="{'typing:' : typeStatus}">&nbsp;</span> 
      </h1>
      <p class="Principal--Text">
        Pronto disponible con la oferta de todos los programas académicos actuales!
      </p>
      <a href="#Formulario">
        <px-button class="Principal--Button" :color="buttonBlue"
          >¡Estoy interesado/a!</px-button
        >
      </a>
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
      typeValue: '',
      typeStatus: false,
      typeArray: ['cursos', 'diplomados', 'maestría', 'doctorados'],
      typingSpeed: 200,
      erasingSpeed: 100,
      newTextDelay: 2000,
      typeArrayIndex: 0,
      charIndex: 0
    };
  },
  methods: {
    typeText() {
      if(this.charIndex < this.typeArray[this.typeArrayIndex].length) {
        if(!this.typeStatus)
          this.typeStatus = true;
        this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex);
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      }
      else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if(this.charIndex > 0) {
        if(!this.typeStatus)
          this.typeStatus = true;
        this.typeValue = this.typeArray[this.typeArrayIndex].substring(0, this.charIndex - 1);
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      }
      else {
        this.typeStatus = false;
        this.typeArrayIndex += 1;
        if(this.typeArrayIndex >= this.typeArray.length)
          this.typeArrayIndex = 0;
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    }
  },
  created() {
    setTimeout(this.typeText, this.newTextDelay + 200);
  },
  computed: {
    showPopUpOpinion() {
      return this.$store.state.popUpOpinion;
    },
    showPopUpReport() {
      return this.$store.state.popUpReport;
    },
  },
  beforeMount() {
  },
};
</script>
<style scoped>
.Principal {
  padding-top: var(--header-height);
  width: 100vw;
  height: 60rem;
  box-sizing: border-box;
  display: grid;
  grid-template-columns: 6fr 5fr;
  background: rgb(68,121,255);
  background: var(--blue-gradient);
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
  align-items: flex-start;
  gap: 3.2rem;
}
.Principal--Title {
  margin: 0;
  font-weight: 800;
  font-size: 4.8rem;
  color: var(--title-color);
}
.Principal--Title--SpecialWord{
  color: var(--off-white);
}
.Cursor{
  color: var(--off-white);
  display: inline-block;
  margin-left: 3px;
  width: 4px;
  background-color: #fff;
  animation: cursorBlink 1s infinite;
}
.Principal--Text {
  margin: 0;
  font-weight: 600;
  font-size: 1.6rem;
  color: var(--off-white);
}
.Principal--Button{
  justify-self: center;
}

@keyframes cursorBlink {
    49% { background-color: #fff; }
    50% { background-color: transparent; }
    99% { background-color: transparent; }
  }
</style>
