<template>
  <section class="Quote">
    <div class="Quote--Container">
      <h3 class="Quote--SubTitle">Queremos para ti una</h3>
      <h3 class="Quote--Title">MEJOR EDUCACIÓN</h3>
      <p class="Quote--Text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Massa
        ullamcorper consectetur arcu odio elit. Libero sit ut convallis gravida
        elementum. Feugiat ut tortor, ut eget euismod mi. Ipsum eu, iaculis
        morbi donec est sed consectetur. Habitant dignissim volutpat ut volutpat
        nec sit semper leo.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: "px-quote",
  data() {
    return {};
  },
};
</script>
<style scoped>
.Quote {
  width: 100vw;
  height: 360px;
  box-sizing: border-box;
  padding: 0 8vw;
}
.Quote--Container {
  width: 100%;
  height: 100%;
  background: linear-gradient(0deg, #708ae4 0%, #a4b1ff 100%);
  border-radius: 2rem;
  box-sizing: border-box;
  padding: 0 8vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.Quote--Title {
  color: #ffffff;
  font-size: 3.6rem;
  text-align: center;
  margin: 0;
  font-weight: 700;
}
.Quote--SubTitle {
  color: #ffffff;
  font-size: 2.4rem;
  text-align: center;
  font-weight: 600;
  margin: 0;
}
.Quote--Text {
  margin: 0;
  margin-top: 2.4rem;
  color: #f0f0f0;
  font-size: 1.6rem;
  font-weight: 600;
  text-align: center;
}
</style>
