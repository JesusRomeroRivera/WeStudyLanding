<template>
  <button
    @click="buttonClick"
    class="button"
    :class="
      this.color == 'blue'
        ? 'blue'
        : this.color == 'white'
        ? 'white'
        : 'NoColor'
    "
    type="button"
  >
    <p style="margin: 0">
      <slot></slot>
    </p>
  </button>
</template>

<script>
export default {
  name: "px-button",
  props: {
    color: String,
  },

  methods: {
    buttonClick() {
      this.$emit("custom-click");
    },
  },
};
</script>
<style scoped>
.button {
  font-family: var(--principal-font);
  padding: 1.5rem 3.5rem;
  border: 0;
  border-radius: 2rem;
  font-size: 1.6rem;
  font-weight: 600;
  cursor: pointer;
}
.blue {
  background: var(--principal-color);
  color: var(--off-white);
}
.white {
  background-color: var(--off-white);
  color: var(--off-black);
}
</style>
