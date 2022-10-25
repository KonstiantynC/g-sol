<template>
  <button class="primary-button">
    <span class="primary-button__label">
      {{ label }}
    </span>
  </button>
</template>

<script>
export default {
  name: 'primary-button',
  props: {
    label: {
      type: String,
      required: true,
    }
  }
}
</script>

<style scoped lang="scss">
@import "../scss/variables";

.primary-button {
  border: 0.1rem solid $primary-button-border-color;
  border-radius: 0.2rem;
  box-shadow: none;
  background-color: transparent;
  padding: 1.4rem 3.2rem;

  .primary-button__label {
    font-family: 'SF Pro Display', sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 1.8rem;
    line-height: 2.1rem;
    text-transform: uppercase;
    letter-spacing: 0.04rem;
    color: $primary-button-label-color;
  }
}
</style>