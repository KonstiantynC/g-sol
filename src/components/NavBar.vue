<template>
  <div class="nav-bar">
    <div class="nav-bar__wrapper section-container">
      <div class="nav-bar__logo">
        <img
            class="nav-bar__logo-image"
            src="../assets/logo.svg"
            alt=""
        >
        <p
            class="nav-bar__logo-text"
            v-html="$t('nav.label')"
        />
      </div>

      <div class="nav-bar__row">
        <div class="nav-bar__links">
          <a href="#" class="nav-bar__link nav-bar__link-active">
            {{ $t('nav.services') }}
          </a>
          <a href="#" class="nav-bar__link">
            {{ $t('nav.projects') }}
          </a>
          <a href="#" class="nav-bar__link">
            {{ $t('nav.about us') }}
          </a>
          <a href="#" class="nav-bar__link">
            {{ $t('nav.contacts') }}
          </a>
        </div>

        <lang-selector class="nav-bar__lang-selector" />
      </div>
    </div>
  </div>
</template>

<script>
import LangSelector from '@/components/LangSelector'

export default {
  name: 'nav-bar',
  components: { LangSelector },
}
</script>

<style scoped lang="scss">
@import "../scss/variables";

.nav-bar {
  width: 100%;
  display: flex;
  justify-content: center;
  height: 10rem;
  background: $nav-bar-bg-color;
}

.nav-bar__wrapper {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 1440px;
}

.nav-bar__row {
  display: flex;
  align-items: center;
}

.nav-bar__logo-image {
  height: 5.2rem;
}

.nav-bar__logo-text {
  font-family: 'SF Pro Display', sans-serif;
  font-size: 2rem;
  line-height: 2.4rem;
  margin-left: 1rem;
  font-weight: 500;
  color: $nav-bar-label-color;
}

.nav-bar__link {
  font-family: 'SF Pro Display', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 2rem;
  line-height: 2.4rem;
  text-decoration: none;
  padding: 0.8rem 0;
  color: $nav-bar-link-color;

  & {
    margin-left: 5rem;
  }

  &.nav-bar__link-active {
    border-bottom: 0.1rem solid $nav-bar-active-link-border-color;
  }
}

.nav-bar__lang-selector {
  margin-left: 5rem;
}

.nav-bar__logo {
  display: flex;
  align-items: center;
}
</style>