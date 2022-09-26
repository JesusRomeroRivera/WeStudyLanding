<template>
  <section id="Formulario" class="Contact">
      <h1 class="Contact--Title">
        ¿Quieres saber más?
      </h1>
      <p class="Contact--Text">
        Te invitamos a registrarte para acelerar el lanzamiento oficial de WeStudy.
      </p>
      <section class="Contact--Container">
        <div class="Contact--Container--Info">
          <p class="Contact--Container--Info--Title">Utiliza las siguientes vías de contacto, o rellena el formulario.</p>
          <p class="Contact--Container--Info--Text">Vía E-mail:</p>
          <p class="Contact--Container--Info--Text">WeStudy@gmail.com</p>
          <p class="Contact--Container--Info--Text">Por teléfono:</p>
          <p class="Contact--Container--Info--Text">952 123 567</p>
        </div>
        <div class="Contact--Container--Form">
          <input type="text" class="Contact--Box" placeholder="Nombre" />
          <input type="text" class="Contact--Box" placeholder="Apellido" />
          <input type="text" class="Contact--Box" placeholder="E-mail" />
          <input type="text" class="Contact--Box" placeholder="Teléfono celular (opcional)" />
          <textarea
            class="Contact--Textarea"
            type="text"
            placeholder="Escribe un comentario (opcional)"
          />
          <p class="Contact--Container--Title">También estoy interesad@ en:</p>
          <label class="Contact--Container--Checkbox">Sección Comunidad<input class="InputCheckbox" type="checkbox" id="cbox1" value="first_checkbox"></label>
          <label class="Contact--Container--Checkbox">Sección Eventos de WeStudy<input class="InputCheckbox" type="checkbox" id="cbox1" value="first_checkbox"></label>
          <px-button class="Contact--Button" :color="buttonBlue"
            >¡Estoy interesado/a!</px-button
          >
        </div>
      </section>
  </section>
</template>

<script>
import PxButton from "@/components/PxButton.vue";

export default {
  name: "px-contact",
  components: {
    PxButton,
  },
  data() {
    return {
      buttonBlue: "blue",
      userData: {
        firstName: "",
        lastName: "",
        imageUrl: "",
        description: "",
        phoneNumber: "",
      },
    };
  },
  methods: {},
};
</script>
<style scoped>
.Contact {
  padding: 15rem 8vw 10rem 8vw;
  height: 70rem;
  width: 100vw;
  box-sizing: border-box;
  background: rgb(68,121,255);
  background: var(--blue-gradient);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  gap: 2.4rem;
}
.Contact--Title {
  font-size: 3.4rem;
  font-weight: 700;
  color: #ACF0FF;
  text-align: center;
}
.Contact--Text {
  font-size: 1.6rem;
  font-weight: 500;
  color: #fff;
  text-align: center;
  padding: 0 10vw;
}
.Contact--Container{
  height: 70%;
  width: 100%;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 4rem;
}
.Contact--Container--Info{
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 1.2rem;
  color: var(--off-white);
  align-self: flex-start;
}
.Contact--Container--Info--Title{
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 2rem;
}
.Contact--Container--Info--Text{
  font-weight: 500;
  font-size: 1.6rem;
}
.Contact--Container--Form {
  width: 100%;
  display: grid;
  height: 100%;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 3.6rem 3.6rem 1fr 2rem 2rem 6rem;
  align-items: center;
  column-gap: 2rem;
  row-gap: 1.4rem;
}
.Contact--Container--Title{
  grid-column-start: 1;
  grid-column-end: 3;
  font-size: 1.6rem;
  color: var(--off-white);
  font-weight: 600;
}
.Contact--Container--Checkbox{
  color: var(--off-white);
  font-weight: 400;
  font-size: 1.2rem;
  display: flex;
  align-items: center;
  gap: 0.4rem;
}
.InputCheckbox{
  width: 2rem;
  height: 2rem;
  border: 0;
  outline: 0;
}
.Contact--Box {
  padding: 1.2rem 0 1.2rem 2rem;
  border-radius: 1.2rem;
  border-color: white;
  font-weight: 500;
  font-size: 1.4rem;
  color: var(--strong-gray);
  box-sizing: border-box;
  height: 100%;
}
.Contact--Textarea {
  grid-column-start: 1;
  grid-column-end: 3;
  padding: 1.2rem 2rem 1.2rem 2rem;
  height: 100%;
  border-radius: 1.2rem;
  border-color: white;
  font-weight: 500;
  font-size: 1.6rem;
  color: var(--strong-gray);
  box-sizing: border-box;
}
.Contact--Button {
  grid-column-start: 1;
  grid-column-end: 3;
  justify-self: flex-end;
  width: 25rem;
}
@media (max-width: 768px){
  .Contact {
    height: 100rem;
    display: grid;
    grid-template-rows: 5rem 10rem 1fr;
  }
  .Contact--Container{
    height: auto;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 20rem;
    grid-template-areas: "Form" "Text";
    gap: 2rem;
  }
  .Contact--Textarea {
    height: 10rem;
  }
  
  .Contact--Container--Info{
    grid-area: Text;
  }
}
@media (max-width: 495px){
  .Contact {
    height: 120rem;
  }
  .Contact--Container--Title{
    grid-column-start: 1;
    grid-column-end: 2;
  }
  .Contact--Textarea {
    grid-column-start: 1;
    grid-column-end: 2;
  }
  .Contact--Button {
    grid-column-start: 1;
    grid-column-end: 2;
  }
  .Contact--Container--Form {
    width: 100%;
    height: 60rem;
    grid-template-columns: 1fr;
    grid-template-rows: 3.6rem 3.6rem 3.6rem 3.6rem 1fr 2rem 2rem 2rem 6rem;
  }
  .Contact--Container--Info--Title{
    font-size: 1.6rem;
  }
  .Contact--Container--Info--Text{
    font-size: 1.2rem;
  }
}

</style>
