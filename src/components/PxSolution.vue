<template>
  <section class="Solution">
    <div class="Solution--Container">
      <h3 class="Solution--SubTitle">Brindamos una</h3>
      <h3 class="Solution--Title">SOLUCIÓN INTEGRAL</h3>
      <p class="Solution--Text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Massa
        ullamcorper consectetur arcu odio elit. Libero sit ut convallis gravida
        elementum.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: "px-solution",
  data() {
    return {};
  },
};
</script>
<style scoped>
.Solution {
  width: 100vw;
  height: 360px;
  box-sizing: border-box;
  padding: 0 8vw;
}
.Solution--Container {
  width: 100%;
  height: 100%;
  border-radius: 2rem;
  box-sizing: border-box;
  padding: 0 8vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.Solution--Title {
  color: var(--off-black);
  font-size: 3.6rem;
  text-align: center;
  margin: 0;
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
</style>
