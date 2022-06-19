<template>
  <section class="Feature">
    <div class="Feature--Context FirstImage">
      <img class="Feature--Img" src="@/assets/feature1.png" alt="" />
      <div class="Feature--Container">
        <h3 class="Feature--Title">Procesos simplificados</h3>
        <p class="Feature--Text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Massa
          ullamcorper consectetur arcu odio elit. Libero sit ut convallis
          gravida elementum.
        </p>
      </div>
    </div>
    <div class="Feature--Context FirstText">
      <div class="Feature--Container">
        <h3 class="Feature--Title">Fácil de usar</h3>
        <p class="Feature--Text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Massa
          ullamcorper consectetur arcu odio elit. Libero sit ut convallis
          gravida elementum.
        </p>
      </div>
      <img class="Feature--Img" src="@/assets/feature2.png" alt="" />
    </div>
    <div class="Feature--Context FirstImage">
      <img class="Feature--Img" src="@/assets/feature3.png" alt="" />
      <div class="Feature--Container">
        <h3 class="Feature--Title">Mide el progreso</h3>
        <p class="Feature--Text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Massa
          ullamcorper consectetur arcu odio elit. Libero sit ut convallis
          gravida elementum.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "px-feature",
  components: {},
  data() {
    return {};
  },
};
</script>
<style scoped>
.Feature {
  width: 100vw;
  box-sizing: border-box;
  padding: 0 8vw;
  display: flex;
  flex-direction: column;
}
.Feature--Context {
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  width: 100%;
  gap: 5rem;
  padding: 0 4.5vw;
}
.Feature--Container {
  width: auto;
  display: flex;
  flex-direction: column;
  gap: 1.6rem;
  justify-content: center;
}
.Feature--Title {
  font-weight: 700;
  color: var(--off-black);
  font-weight: 700;
  font-size: 4rem;
  margin: 0;
}
.Feature--Text {
  font-weight: 500;
  font-size: 1.6rem;
  color: var(--strong-gray);
  margin: 0;
}
.Feature--Img {
  width: 28rem;
}
</style>
