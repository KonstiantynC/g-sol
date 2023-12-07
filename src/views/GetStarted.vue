<template>
  <div class="get-started app__page">
    <div class="get-started__wrapper app__wrapper section-container">
      <div class="get-started__title-wrp">
        <h1
            class="get-started__title"
            v-html="$t('get-started.title')"
        />
        <primary-button label="Order a project" />
      </div>
      <div class="get-started__footer">
        <div class="get-started__footer-links">
          <img
              class="get-started__footer-link-icon"
              src="../assets/icons/upwork.svg"
              alt=""
          >
          <img
              class="get-started__footer-link-icon"
              src="../assets/icons/facebook.svg"
              alt=""
          >
          <img
              class="get-started__footer-link-icon"
              src="../assets/icons/instagram.svg"
              alt=""
          >
          <img
              class="get-started__footer-link-icon"
              src="../assets/icons/linkedin.svg"
              alt=""
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PrimaryButton from '@/components/PrimaryButton'

export default {
  name: 'get-started',
  components: { PrimaryButton },
}
</script>

<style lang="scss">
@import "../scss/variables";

.get-started__title-wrp span {
  font-size: inherit;
  color: $get-started-title-accent-color;
}
</style>
<style lang="scss" scoped>
@import "../scss/variables";

.get-started {
  background-color: $get-started-bg-color;
}

.get-started__wrapper {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 91.5rem;
  padding-top: 14.8rem;
  padding-bottom: 7.6rem;
  background-image: url('../assets/get-started-bg-decoration.png');
  background-repeat: no-repeat;
}

.get-started__title-wrp {
  padding-left: 20rem;
}

.get-started__title-wrp h1 {
  color: $get-started-title-primary-color;
}

.get-started__title {
  font-family: 'Bebas Neue', sans-serif;
  font-weight: 400;
  font-size: 13rem;
}

.get-started__footer-links {
  display: flex;
  justify-content: flex-end;

  .get-started__footer-link-icon {
    margin-left: 1.6rem;
  }
}
</style>