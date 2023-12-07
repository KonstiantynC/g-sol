<template>
  <div class="amhora-app app__page">
    <div class="amhora-app__wrapper app__wrapper">
      <div class="amhora-app__info">
        <span class="amhora-app__tech-marker app-details__tech-marker">
          {{ $t('amhora.web-dev') }}
        </span>

        <h2 class="app-details__app-name">
          {{ $t('amhora.app-name') }}
        </h2>

        <div
            v-html="$t('amhora.details')"
            class="app-details__app-details"
        />
        <div class="app-details__technologies">
          <span class="app-details__technologies-label">
            {{ $t('amhora.tech-lbl') }}
          </span>

          <ul class="app-details__technologies-list">
            <li class="app-details__technology">
              <span class="app-details__technology-label">
                {{ $t('amhora.front-lbl') }}
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
                {{ $t('amhora.back-lbl') }}
              </span>
              <div class="app-details__technology-details">
                <img
                    class="app-details__technology-icon"
                    src="../assets/icons/js.svg"
                    alt=""
                >
                <span class="app-details__technology-name">
                  {{ TECHNOLOGIES.node }}
                </span>
              </div>
            </li>
          </ul>
        </div>
      </div>
      <div class="amhora-app__screens">
        <carousel
            :navigationEnabled="true"
            :perPage="1"
        >
          <slide>
            <img
                src="../assets/amhora/explorer.png"
                alt=""
                class="amhora-app__screen"
            >
          </slide>
          <slide>
            <img
                src="../assets/amhora/market.png"
                alt=""
                class="amhora-app__screen"
            >
          </slide>
          <slide>
            <img
                src="../assets/amhora/transactions.png"
                alt=""
                class="amhora-app__screen"
            >
          </slide>
        </carousel>
      </div>
    </div>

    <div class="amhora-app__bg-blur" />
  </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'
import { TECHNOLOGIES } from '@/technologies.const'

export default {
  name: 'amhora-app',
  components: { Carousel, Slide },
  data: () => ({
    TECHNOLOGIES,
  })
}
</script>

<style scoped lang="scss">
  @import "../scss/variables";

  .amhora-app {
    position: relative;
    background-color: $amhora-bg-color;
  }

  .amhora-app__wrapper {
    padding: 12rem 13.5rem;
    display: flex;
    justify-content: space-between;
  }

  .amhora-app__bg-blur {
    position: absolute;
    width: 88rem;
    height: 60rem;
    left: 46rem;
    top: 16rem;
    background: $amhora-blur-bg-color;
    filter: blur(40rem);
  }

  .amhora-app__info {
    width: 28rem;
  }

  .amhora-app__tech-marker {
    background-color: $amhora-marker-bg-color;
  }

  .amhora-app__screens {
    height: 50rem;
    width: 100%;
    margin-top: 4.8rem;
    padding: 0 4.6rem;
    z-index: 1;
  }

  .amhora-app__screen {
    padding: 0 1.6rem;
    height: 50rem;
    width: 100%;
  }
</style>