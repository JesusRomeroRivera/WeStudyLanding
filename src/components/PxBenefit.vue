<template>
  <section class="Benefit">
    <svg id="Beneficios"  class="TopCurve" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
      <path fill="#fff" fill-opacity="1" d="M0,160L60,176C120,192,240,224,360,202.7C480,181,600,107,720,85.3C840,64,960,96,1080,112C1200,128,1320,128,1380,128L1440,128L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path>
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
      <path fill="#fff" fill-opacity="1" d="M0,224L60,218.7C120,213,240,203,360,176C480,149,600,107,720,90.7C840,75,960,85,1080,85.3C1200,85,1320,75,1380,69.3L1440,64L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z"></path>
    </svg>
  </section>
</template>

<script>
let image_1 = require('../assets/BenefitIcons/Icon1.svg');
let image_2 = require('../assets/BenefitIcons/Icon2.svg');
let image_3 = require('../assets/BenefitIcons/Icon3.svg');
let image_4 = require('../assets/BenefitIcons/Icon4.svg');
export default {
  name: "px-benefit",
  data() {
    return {
      features: [
        {
          id: 1,
          url: image_1,
          name: 'Usa la aplicación en cualquier lugar',
          description: 'Lleva la aplicación siempre en tu dispositivo para poder consultar la información desde cualquier lugar.'
        },
        {
          id: 2,
          url: image_2,
          name: 'Sincroniza tus datos con tus cuentas',
          description: 'Utiliza tus cuentas en redes sociales para sincronizar tus datos generales.'
        },
        {
          id: 3,
          url: image_3,
          name: 'Accede a la aplicación sin conexión',
          description: 'No necesitarás conexión para utilizar la aplicación, siempre tendrás la información a mano.'
        },
        {
          id: 4,
          url: image_4,
          name: 'Comparte los datos con tus contactos',
          description: 'Podrás compartir la información que te interese con tus contactos fácilmente.'
        }
      ]
    };
  },
};
</script>
<style scoped>
  .TopCurve{
    margin-top: -20rem;
  }
  .BackCurve{
    margin-top: 0;
  }
.Benefit {
  width: 100vw;
  height: 25rem;
  box-sizing: border-box;
  display: grid;
  background-color: #fff;
  grid-template-rows: 1rem 1fr 1rem;
}
.Benefit--Content{
  margin-top: -10rem;
  padding: 0 8vw;
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
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 2rem;
}
.Benefit--Container--Feature--Img{
  height: auto;
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
</style>
