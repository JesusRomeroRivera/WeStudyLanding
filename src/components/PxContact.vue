<template>
  <section class="Contact">
    <div class="Contact--Container">
      <h3 class="Contact--Title">
        ¿Listo para disfrutar de los beneficios de WeStudy?
      </h3>
      <p class="Contact--Text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Massa
        ullamcorper consectetur arcu odio elit. Libero sit ut convallis gravida
        elementum.
      </p>
      <div class="Contact--Form">
        <input type="text" class="Contact--Box" placeholder="Nombre" />
        <input type="text" class="Contact--Box" placeholder="E-mail" />
        <textarea
          class="Contact--Textarea"
          type="text"
          placeholder="Déjanos un mensaje"
        />
        <px-button class="Contact--Button" :color="buttonWhite"
          >Enviar</px-button
        >
      </div>
    </div>
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
      buttonWhite: "white",
      userData: {
        firstName: "",
        lastName: "",
        imageUrl: "",
        description: "",
        phoneNumber: "",
      },
      address: {
        region: "",
        province: "",
        district: "",
        fullAddress: "",
      },
    };
  },
  methods: {},
};
</script>
<style scoped>
.Contact {
  padding: 10vh 8vw;
  height: 100vh;
  box-sizing: border-box;
}
.Contact--Container {
  display: flex;
  flex-direction: column;
  height: 100%;
  background: var(--blue-gradient);
  border-radius: 2rem;
  align-items: center;
  justify-content: space-between;
  padding: 10vh 10vw;
  box-sizing: border-box;
  gap: 2.4rem;
}
.Contact--Title {
  font-size: 3.6rem;
  font-weight: 700;
  margin: 0;
  color: #ffffff;
  text-align: center;
}
.Contact--Text {
  font-size: 1.6rem;
  font-weight: 600;
  margin: 0;
  color: #f0f0f0;
  text-align: center;
}
.Contact--Form {
  width: 100%;
  display: grid;
  height: 80%;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 3fr 60px;
  align-items: center;
  gap: 2.5rem;
}
.Contact--Box {
  padding: 1.2rem 0 1.2rem 2.5rem;
  border-radius: 2rem;
  border-color: white;
  font-weight: 500;
  font-size: 1.6rem;
  color: var(--strong-gray);
  box-sizing: border-box;
}
.Contact--Textarea {
  grid-column-start: 1;
  grid-column-end: 3;
  padding: 1.2rem 0 0 2.5rem;
  height: 100%;
  border-radius: 2rem;
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
  width: 20rem;
}
</style>
