<template>
  <div class="bitalo-app app__page">
    <div class="bitalo-app__wrapper app__wrapper">
      <div class="bitalo-app__info">
        <span class="bitalo-app__tech-marker app-details__tech-marker">
          {{ $t('bitalo.web-dev') }}
        </span>

        <h2 class="app-details__app-name">
          {{ $t('bitalo.app-name') }}
        </h2>

        <div
            v-html="$t('bitalo.details')"
            class="bitalo-app__app-details app-details__app-details"
        />
        <div class="app-details__technologies">
          <span class="app-details__technologies-label">
            {{ $t('bitalo.tech-lbl') }}
          </span>

          <ul class="app-details__technologies-list">
            <li class="app-details__technology">
              <span class="app-details__technology-label">
                {{ $t('bitalo.mobile-lbl') }}
              </span>
              <div class="app-details__technology-details">
                <img
                    class="app-details__technology-icon"
                    src="../assets/icons/flutter.svg"
                    alt=""
                >
                <span class="app-details__technology-name">
                  {{ TECHNOLOGIES.flutter }}
                </span>
              </div>
            </li>
            <li class="app-details__technology">
              <span class="app-details__technology-label">
                {{ $t('bitalo.front-lbl') }}
              </span>
              <div class="app-details__technology-details">
                <img
                    class="app-details__technology-icon"
                    src="../assets/icons/vue.svg"
                    alt=""
                >
                <span class="app-details__technology-name">
                  {{ TECHNOLOGIES.vue }}
                </span>
              </div>
            </li>
            <li class="app-details__technology">
              <span class="app-details__technology-label">
                {{ $t('bitalo.back-lbl') }}
              </span>
              <div class="app-details__technology-details">
                <div class="bitalo-app__tech-details">
                  <img
                      class="app-details__technology-icon"
                      src="../assets/icons/js.svg"
                      alt=""
                  >
                  <span class="app-details__technology-name">
                    {{ TECHNOLOGIES.node }}
                  </span>
                </div>
                <div class="bitalo-app__tech-details">
                  <img
                      class="app-details__technology-icon"
                      src="../assets/icons/rails.svg"
                      alt=""
                  >
                  <span class="app-details__technology-name">
                    {{ TECHNOLOGIES.rubyOnRails }}
                  </span>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
      <div class="bitalo-app__screens">
        <carousel
            class="bitalo-app__carousel"
            :navigationEnabled="true"
            :perPage="1"
        >
          <slide class="bitalo-app__screen-slide">
            <img
                src="../assets/bitalo/main.png"
                alt=""
                class="bitalo-app__screen"
            >
          </slide>
          <slide class="bitalo-app__screen-slide">
            <img
                src="../assets/bitalo/history.png"
                alt=""
                class="bitalo-app__screen"
            >
          </slide>
          <slide class="bitalo-app__screen-slide">
            <img
                src="../assets/bitalo/offers.png"
                alt=""
                class="bitalo-app__screen"
            >
          </slide>
          <slide class="bitalo-app__screen-slide">
            <img
                src="../assets/bitalo/map.png"
                alt=""
                class="bitalo-app__screen"
            >
          </slide>
          <slide class="bitalo-app__screen-slide">
            <img
                src="../assets/bitalo/home-web.png"
                alt=""
                class="bitalo-app__screen"
            >
          </slide>
          <slide class="bitalo-app__screen-slide">
            <img
                src="../assets/bitalo/home.png"
                alt=""
                class="bitalo-app__screen"
            >
          </slide>
          <slide class="bitalo-app__screen-slide">
            <img
                src="../assets/bitalo/drawer.png"
                alt=""
                class="bitalo-app__screen"
            >
          </slide>
          <slide class="bitalo-app__screen-slide">
            <img
                src="../assets/bitalo/register.png"
                alt=""
                class="bitalo-app__screen"
            >
          </slide>
        </carousel>
      </div>
    </div>

    <div class="bitalo-app__bg-blur-left" />
    <div class="bitalo-app__bg-blur-right" />
    <img
        class="bitalo-app__bg-decoration"
        src="../assets/bitalo-bg-decoration.png"
        alt=""
    />
  </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'
import { TECHNOLOGIES } from '@/technologies.const'

export default {
  name: 'bitalo-app',
  components: { Carousel, Slide },
  data: () => ({
    TECHNOLOGIES,
  })
}
</script>

<style scoped lang="scss">
@import "../scss/variables";

.bitalo-app {
  position: relative;
  background-color: $bitalo-bg-color;
}

.bitalo-app__wrapper {
  padding: 12rem 13.5rem;
  display: flex;
  justify-content: space-between;
}

.bitalo-app__bg-decoration {
  z-index: 0;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.bitalo-app__bg-blur-left {
  position: absolute;
  width: 45rem;
  height: 75rem;
  left: 4rem;
  top: 15rem;

  background: $bitalo-left-blur-bg-color;
  filter: blur(40rem);
}

.bitalo-app__bg-blur-right {
  position: absolute;
  width: 72rem;
  height: 73rem;
  left: 57rem;
  top: 16rem;

  background: $bitalo-right-blur-bg-color;
  filter: blur(40rem);
}

.bitalo-app__app-details {
  width: 28rem;
}

.bitalo-app__tech-details {
  display: flex;
  align-items: center;

  &:last-child {
    margin-left: 1.2rem;
  }
}

.bitalo-app__info {
  width: 38rem;
  z-index: 1;
}

.bitalo-app__screens {
  height: 45rem;
  width: calc(100% - 38rem);
  margin-top: 4.8rem;
  padding: 0 1.6rem;
  z-index: 1;
}

.bitalo-app__screen {
  padding: 0 1.6rem;
  height: 45rem;
  max-width: calc(100%);
}

.bitalo-app__screen-slide {
  display: flex;
  justify-content: center;
}


</style>