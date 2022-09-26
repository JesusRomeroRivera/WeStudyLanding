<template>
  <section id="Secciones" class="Section">
    <h1 class="Section--Title">En WeStudy encontrarás:</h1>
    <div class="Section--Container">
      <article class="Section--Container--Section" :key="section.id" v-for="section in sections">
        <img class="Section--Container--Section--Img" :src="section.url" :alt="section.url" width="50" height="20">
        <p class="Section--Container--Section--Title">{{ section.name }}</p>
        <span class="Section--Container--Section--Text">{{ section.description }}<br><br>{{ section.badge }}</span>
      </article>
    </div>
  </section>
</template>

<script>
let image_1 = require('../assets/feature1.png');
let image_2 = require('../assets/feature2.png');
let image_3 = require('../assets/feature3.png');
let image_4 = require('../assets/feature4.png');
export default {
  name: "px-sections",
  components: {},
  data() {
    return {
      sections: [
        {
          id: 1,
          url: image_1,
          name: 'Sección de búsqueda',
          description: "Aquí podrás buscar, analizar y comparar la oferta educativa disponible gracias a nuestros filtros de búsqueda y el sistema de comparación.",
          badge: '¡Podrás encontrar tu curso ideal!'
        },
        {
          id: 2,
          url: image_2,
          name: 'Comunidad',
          description: 'Si tienes dudas o quieres conocer las experiencias de los demás sobre el sector educativo y profesional, el foro de socialización te ayudará en tu búsqueda.',
          badge: '¡Podrás relacionarte con la comunidad!'
        },
        {
          id: 3,
          url: image_3,
          name: 'Eventos de WeStudy',
          description: 'Cada mes encontrarás eventos que pueden mejorar tu perfil, desde webinars gratuitos, eventos de networking y concursos donde podrás mostrar tus habilidades.',
          badge: '¡Podrás entrar a eventos únicos!'
        },
        {
          id: 4,
          url: image_4,
          name: 'Noticias de interés',
          description: 'Encontrarás webinars informativos de los nuevos cursos, información de las becas otorgadas por instituciones de todo el mundo y de eventos para emprendedores.',
          badge: '¡Podrás ver las últimas noticias del sector!'
        }
      ]
    };
  },
};
</script>
<style scoped>
.Section {
  width: 100vw;
  height: 180rem;
  box-sizing: border-box;
  padding: 20rem 8vw 20rem 8vw;
  display: grid;
  grid-template-rows: 4rem 1fr;
  gap: 4rem;
  background-color: var(--light-blue);
}
.Section--Title {
  color: var(--strong-blue);
  font-size: 3rem;
}
.Section--Container {
  display: grid;
  height: auto;
  gap: 2rem;
  grid-template-rows: repeat(4, 1fr);
}
.Section--Container--Section{
  height: auto;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 3fr 7fr;
  column-gap: 2rem;
}
.Section--Container--Section:nth-child(odd){
  grid-template-areas: "Imagen Title" "Imagen Text";
}
.Section--Container--Section:nth-child(even){
  grid-template-areas: "Title Imagen" "Text Imagen";
}
.Section--Container--Section--Img{
  grid-area: Imagen;
  width: 100%;
  height: auto;
  align-self: center;
}
.Section--Container--Section--Title{
  font-size: 2.4rem;
  text-align: center;
  font-weight: 700;
  grid-area: Title;
  align-self: flex-end;
}
.Section--Container--Section--Text{
  font-size: 1.6rem;
  text-align: center;
  font-weight: 400;
  color: var(--off-black);
  grid-area: Text;
  align-self: center;
  margin-bottom: 5rem;
}
@media (max-width: 768px){
  .Section{
    height: 260rem;
    padding: 15rem 8vw 20rem 8vw;
  }
  .Section--Container--Section{
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 5rem 12.5rem 1fr;
  }
  .Section--Container--Section:nth-child(odd){
    grid-template-areas: "Title" "Text" "Imagen";
  }
  .Section--Container--Section:nth-child(even){
    grid-template-areas: "Title" "Text" "Imagen";
  }
  .Section--Container--Section--Title{
    align-self: center;
  }
  .Section--Container--Section--Text{
    margin-bottom: 0;
  }
}
@media (max-width: 585px){
  .Section{
    height: 240rem;
  }
  .Section--Container--Section{
    grid-template-rows: 5rem 15rem 1fr;
  }
  .Section--Container--Section--Text{
    font-size: 1.6rem;
  }
}
@media (max-width: 425px){
  .Section{
    height: 220rem;
  }
  .Section--Container--Section{
    grid-template-rows: 5rem 17.5rem 1fr;
  }
}
</style>
