<template>
  <div class="lang-selector">
    <img class="lang-selector__icon" src="../assets/icons/lang.svg" alt="">
    <span class="lang-selector__value">EN</span>
    <img class="lang-selector__arrow" src="../assets/icons/arrow-down.svg" alt="">
  </div>
</template>

<script>
export default {
  name: 'lang-selector',
}
</script>

<style scoped lang="scss">
.lang-selector {
  border: 1px solid #FFFFFF;
  border-radius: 10px;
  padding: 0.6rem 0.8rem;
  display: flex;
  align-items: center;
}

.lang-selector__icon {
  width: 1.4rem;
  height: 1.4rem;
}

.lang-selector__arrow {
  width: 0.8rem;
}

.lang-selector__value {
  font-family: 'SF Pro Display';
  font-style: normal;
  font-weight: 500;
  font-size: 1.6rem;
  line-height: 1.9rem;
  margin: 0 0.4rem;
  color: #FFFFFF;
}
</style>