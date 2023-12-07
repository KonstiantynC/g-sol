<template>
  <div class="book-reader app__page">
    <div class="book-reader__wrapper app__wrapper">
      <h1 class="book-reader__title app__page-title">
        {{ $t('book-reader.title') }}
      </h1>

      <div class="book-reader__preview">
        <div class="book-reader__screens">
          <img
              class="book-reader__phone-screen"
              src="../assets/reader/home.png"
              alt=""
          >
          <img
              class="book-reader__phone-screen"
              src="../assets/reader/reviews.png"
              alt=""
          >
          <img
              class="book-reader__phone-screen"
              src="../assets/reader/about.png"
              alt=""
          >
        </div>
        <div class="book-reader__info">
          <span class="app-details__tech-marker">
            {{ $t('book-reader.mobile-dev') }}
          </span>
          <h2 class="app-details__app-name">
            {{ $t('book-reader.app-name') }}
          </h2>

          <div
              v-html="$t('book-reader.details')"
              class="app-details__app-details"
          />

          <div class="app-details__technologies">
            <span class="app-details__technologies-label">
              {{ $t('book-reader.tech-lbl') }}
            </span>

            <ul class="app-details__technologies-list">
              <li class="app-details__technology">
                <span class="app-details__technology-label">
                  {{ $t('book-reader.mobile-lbl') }}
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
                {{ $t('book-reader.front-lbl') }}
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
                  {{ $t('book-reader.back-lbl') }}
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
      </div>
    </div>

    <div class="book-reader__bg-blur" />
  </div>
</template>

<script>
import { TECHNOLOGIES } from '@/technologies.const'

export default {
  name: 'book-reader',
  data: () => ({
    TECHNOLOGIES,
  })
}
</script>

<style scoped lang="scss">
  @import "../scss/variables";

  .book-reader {
    position: relative;
    background-color: $book-reader-bg-color;
  }

  .book-reader__wrapper {
    padding: 12rem 13.5rem;
  }

  .book-reader__bg-blur {
    z-index: 1;
    position: absolute;
    width: 65rem;
    height: 60rem;
    left: 14rem;
    top: 30rem;

    background: $book-reader-blur-bg-color;
    filter: blur(40rem);
  }

  .book-reader__title {
    color: $book-reader-text-color;
  }

  .book-reader__preview {
    margin-top: 12rem;
    display: flex;
    justify-content: space-between;
  }

  .book-reader__screens {
    display: flex;
    position: relative;
  }

  .book-reader__phone-screen {
    z-index: 11;
    width: 24rem;
    height: 48rem;

    &:nth-child(2) {
      margin-left: -6rem;
      margin-top: 4rem;
      top: 2rem;
    }

    &:nth-child(3) {
      margin-left: -6rem;
      margin-top: 8rem;
      top: 2rem;
    }
  }

  .book-reader__info {
    width: 28rem;
  }
</style>