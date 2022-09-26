<template>
  <section id="Solucion" class="Solution">
    <svg class="TopCurve" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
      <path fill="#A4BAFF" fill-opacity="1" d="M0,96L60,85.3C120,75,240,53,360,48C480,43,600,53,720,69.3C840,85,960,107,1080,112C1200,117,1320,107,1380,101.3L1440,96L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path>
    </svg>
    <div class="Solution--Content">
      <h1 class="Solution--Title">¿Cómo funciona WeStudy?</h1>
      <div class="Solution--Container">
        <iframe class="Solution--Video" src="https://www.youtube.com/embed/uivyCAOrRzI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <px-button :color="buttonBlue">¡Estoy interesado/a!</px-button>
      </div>
    </div>
    <svg class="BackCurve" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
      <path fill="#A4BAFF" fill-opacity="1" d="M0,96L60,85.3C120,75,240,53,360,48C480,43,600,53,720,69.3C840,85,960,107,1080,112C1200,117,1320,107,1380,101.3L1440,96L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z"></path>
    </svg>
  </section>
</template>

<script>
import PxButton from "@/components/PxButton.vue";

export default {
  name: "px-solution",
  components: {
    PxButton,
  },
  data() {
    return {
      buttonBlue: "blue",

    };
  },
};
</script>
<style scoped>
.TopCurve{
  margin-top: -20rem;
  min-width: 1200px;
}
.BackCurve{
  margin-top: 0;
  min-width: 1200px;
}
.Solution {
  width: 100vw;
  height: 60rem;
  display: grid;
  grid-template-rows: 1rem 1fr 1rem;
  background-color: #A4BAFF;
}
.Solution--Content{
  width: 100vw;
  padding: 5rem 8vw 0 8vw;
  box-sizing: border-box;
  display: grid;
  grid-template-rows: 0 1fr;
  gap: 2rem;
}
.Solution--Container {
  border-radius: 2rem;
  box-sizing: border-box;
  width: 100%;
  display: grid;
  grid-template-rows: 1fr 5rem;
  align-items: center;
  justify-items: center;
}
.Solution--Video{
  width: 50vw;
  height: 37.5rem;
}
.Solution--Title {
  color: var(--strong-blue);
  font-size: 3rem;
  font-weight: 700;
}
.Solution--SubTitle {
  color: var(--off-black);
  font-size: 2.4rem;
  text-align: center;
  font-weight: 600;
  margin: 0;
}
.Solution--Text {
  margin: 0;
  margin-top: 3.2rem;
  color: var(--strong-gray);
  font-size: 1.6rem;
  font-weight: 500;
  text-align: center;
}
@media (max-width: 768px){
  .Solution--Video{
    width: 80vw;
    height: 35rem;
  }
}
</style>
