<template>
  <div class="home">
    <nav-bar class="home__nav"/>
    <div class="home__container section-container">
      <div class="home__title-wrp">
        <h1
            class="home__title"
            v-html="$t('home.title')"
        />
        <primary-button label="Order a project"/>
      </div>
      <div class="home__footer">
        <div class="home__footer-links">
          <img
              class="home__footer-link-icon"
              src="../assets/icons/upwork.svg"
              alt=""
          >
          <img
              class="home__footer-link-icon"
              src="../assets/icons/facebook.svg"
              alt=""
          >
          <img
              class="home__footer-link-icon"
              src="../assets/icons/instagram.svg"
              alt=""
          >
          <img
              class="home__footer-link-icon"
              src="../assets/icons/linkedin.svg"
              alt=""
          >
        </div>
      </div>
    </div>
    <tech-preview />
    <case-studies />
    <amhora-app />
    <jelly-wallet />
    <bitalo-app />
  </div>
</template>

<script>
import NavBar from '@/components/NavBar'
import PrimaryButton from '@/components/PrimaryButton'
import TechPreview from '@/views/TechPreview'
import CaseStudies from '@/views/BookReader'
import AmhoraApp from '@/views/AmhoraApp'
import JellyWallet from '@/views/JellyWallet'
import BitaloApp from '@/views/BitaloApp'

export default {
  name: 'home',
  components: {
    NavBar,
    PrimaryButton,
    TechPreview,
    CaseStudies,
    AmhoraApp,
    JellyWallet,
    BitaloApp,
  }
}
</script>

<style lang="scss">
@import "../scss/variables";

.home__title-wrp span {
  font-size: inherit;
  color: $home-title-accent-color;
}
</style>

<style scoped lang="scss">
@import "../scss/variables";

.home {
  background-color: $home-bg-color;
}

.home__container {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 91.5rem;
  padding-top: 14.8rem;
  padding-bottom: 7.6rem;
  width: 100%;
  background-image: url('../assets/home-bg-decoration.png');
}

.home__title-wrp {
  padding-left: 20rem;
}

.home__title-wrp h1 {
  color: $home-title-primary-color;
}

.home__title {
  font-family: 'Bebas Neue', sans-serif;
  font-weight: 400;
  font-size: 13rem;
}

.home__footer-links {
  display: flex;
  justify-content: flex-end;

  .home__footer-link-icon {
    margin-left: 1.6rem;
  }
}
</style>
