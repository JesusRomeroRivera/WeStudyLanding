<template>
  <section class="Benefit">
    <svg id="Beneficios" class="TopCurve" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
      <path fill="#fff" fill-opacity="1" d="M0,96L60,85.3C120,75,240,53,360,48C480,43,600,53,720,69.3C840,85,960,107,1080,112C1200,117,1320,107,1380,101.3L1440,96L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path>
    </svg>
    <div class="Benefit--Content">
      <h1 class="Benefit--Title">Les ofrecemos...</h1>
      <div class="Benefit--Container">
        <article class="Benefit--Container--Feature" :key="feature.id" v-for="feature in features">
          <img class="Benefit--Container--Feature--Img" :src="feature.url" :alt="feature.url" width="50" height="20">
          <p class="Benefit--Container--Feature--Title">{{ feature.name }}</p>
          <span class="Benefit--Container--Feature--Text">{{ feature.description }}</span>
        </article>
      </div>
    </div>
    <svg class="BackCurve" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
      <path fill="#fff" fill-opacity="1" d="M0,96L60,85.3C120,75,240,53,360,48C480,43,600,53,720,69.3C840,85,960,107,1080,112C1200,117,1320,107,1380,101.3L1440,96L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z"></path>
    </svg>
  </section>
</template>

<script>
let image_1 = require('../assets/BenefitIcons/Icon1.png');
let image_2 = require('../assets/BenefitIcons/Icon2.png');
let image_3 = require('../assets/BenefitIcons/Icon3.png');
let image_4 = require('../assets/BenefitIcons/Icon4.png');
export default {
  name: "px-benefit",
  data() {
    return {
      features: [
        {
          id: 1,
          url: image_1,
          name: 'Encontrar el curso que mejor se adapte a ti',
          description: 'Un marketplace con las mejores ofertas académicas de todas las universidades de Latinoamérica.'
        },
        {
          id: 2,
          url: image_2,
          name: 'Compartir tu pasión por aprender',
          description: '¡Únete a tu gente! Espacio para interactuar y conocer personas con aspiraciones similares a las tuyas.'
        },
        {
          id: 3,
          url: image_3,
          name: 'Mejorar tu experiencia de búsqueda',
          description: 'Encuentra el curso que tanto deseas en el menor tiempo posible y al mejor precio.'
        },
        {
          id: 4,
          url: image_4,
          name: 'Impulsar tu desarrollo personal y profesional',
          description: 'Entérate de novedades como becas, concursos, eventos de networking y más.'
        }
      ]
    };
  },
};
</script>
<style scoped>
  .TopCurve{
    margin-top: -25rem;
    min-width: 1200px;
    background-image: center;
  }
  .BackCurve{
    min-width: 1200px;
  }
.Benefit {
  width: 100vw;
  height: 30rem;
  box-sizing: border-box;
  display: grid;
  background-color: #fff;
  grid-template-rows: 1rem 1fr 1rem;
}
.Benefit--Content{
  margin-top: -10rem;
  padding: 0 8vw;
  width: 100vw;
  box-sizing: border-box;
  display: grid;
  grid-template-rows: 4rem 1fr;
  gap: 2rem;
}
.Benefit--Title{
  color: var(--strong-blue);
  font-size: 3rem;
}
.Benefit--Container{
  display: grid;
  height: auto;
  gap: 4rem;
  grid-template-columns: repeat(4, 1fr);
}
.Benefit--Container--Feature{
  height: auto;
  display: grid;
  grid-template-rows: 15rem 3rem 1fr;
  justify-items: center;
  align-items: flex-start;
  gap: 2rem;
}
.Benefit--Container--Feature--Img{
  height: 15rem;
  width: auto;
}
.Benefit--Container--Feature--Title{
  font-size: 1.6rem;
  text-align: center;
  font-weight: 600;
}
.Benefit--Container--Feature--Text{
  font-size: 1.2rem;
  text-align: center;
  color: var(--off-black);
}
@media (max-width: 1280px){
  .Benefit{
    height: 50rem;
  }
  .Benefit--Container{
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr 1fr;
    row-gap: 2.5rem;
  }
}
@media (max-width: 1024px){
  .Benefit{
    height: 55rem;
  }
}
@media (max-width: 585px){
  .Benefit{
    height: 115rem;
  }
  .Benefit--Container{
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr;
    row-gap: 2.5rem;
  }
  .Benefit--Container--Feature--Img{
  }
  .Benefit--Container--Feature{
  }
}
</style>
