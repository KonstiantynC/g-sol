<template>
  <div class="jelly-wallet app__page">
    <div class="jelly-wallet__wrapper app__wrapper">
      <div class="jelly-wallet__screens">
        <carousel
            :navigationEnabled="true"
            :perPage="1"
        >
          <slide>
            <img
                src="../assets/jelly/preview.png"
                alt=""
                class="jelly-wallet__screen-img"
            >
          </slide>
          <slide>
            <img
                src="../assets/jelly/confirmation.png"
                alt=""
                class="jelly-wallet__screen-img"
            >
          </slide>
          <slide>
            <img
                src="../assets/jelly/liquidity.png"
                alt=""
                class="jelly-wallet__screen-img"
            >
          </slide>
          <slide>
            <img
                src="../assets/jelly/lock.png"
                alt=""
                class="jelly-wallet__screen-img"
            >
          </slide>
          <slide>
            <img
                src="../assets/jelly/pools.png"
                alt=""
                class="jelly-wallet__screen-img"
            >
          </slide>
          <slide>
            <img
                src="../assets/jelly/swap.png"
                alt=""
                class="jelly-wallet__screen-img"
            >
          </slide>
        </carousel>
      </div>
      <div class="jelly-wallet__info">
        <span class="jelly-wallet__tech-marker app-details__tech-marker">
          {{ $t('jelly.web-dev') }}
        </span>

        <h2 class="app-details__app-name">
          {{ $t('jelly.app-name') }}
        </h2>

        <div
            v-html="$t('jelly.details')"
            class="app-details__app-details"
        />
        <div class="app-details__technologies">
          <ul class="app-details__technologies-list">
            <li class="app-details__technology">
              <span class="app-details__technology-label">
                {{ $t('jelly.tech-lbl') }}
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
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'
import { TECHNOLOGIES } from '@/technologies.const'

export default {
  name: 'jelly-wallet',
  components: { Carousel, Slide },
  data: () => ({
    TECHNOLOGIES,
  }),
}
</script>

<style scoped lang="scss">
@import "../scss/variables";

.jelly-wallet {
  min-height: 100vh;
  position: relative;
  background-color: $jelly-bg-color;

  &:before {
    content: '';
    position: absolute;
    width: 58rem;
    height: 55rem;
    left: 27rem;
    top: 29rem;

    background: $jelly-left-blur-bg-color;
    filter: blur(25rem);
  }

  &:after {
    content: '';
    position: absolute;
    width: 72rem;
    height: 68rem;
    left: 68rem;
    top: 12rem;

    background: $jelly-right-blur-bg-color;
    filter: blur(250px);
  }
}

.jelly-wallet__wrapper {
  padding: 17.4rem 13.5rem;
  display: flex;
  justify-content: space-between;
}

.jelly-wallet__screens {
  height: 40rem;
  width: 90rem;
  margin-top: 4.8rem;
  padding: 0 4.6rem;
  z-index: 1;
}

.jelly-wallet__screen-img {
  padding: 0 6.6rem;
  height: 40rem;
  width: 100%;
}

.jelly-wallet__info {
  z-index: 1;
  width: 28rem;
}

.jelly-wallet__tech-marker {
  background-color: $jelly-marker-bg-color;
}

.app-details__app-name,
.app-details__app-details,
.app-details__technology-label,
.app-details__technology-name {
  color: #000000;
}

.app-details__technology-icon {
  filter: brightness(1) invert(0);
}
</style>