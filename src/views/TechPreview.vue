<template>
  <div class="tech-preview app__page">
    <div class="tech-preview__wrapper app__wrapper">
      <div class="tech-preview__header">
        <div class="tech-preview__title">
          <h1 class="tech-preview__title-label app__page-title">
            {{ $t('tech-preview.title') }}
          </h1>
          <span class="tech-preview__title-description">
            {{ $t('tech-preview.description') }}
          </span>
        </div>
        <div class="tech-preview__hint">
          <span class="tech-preview-hint__title">
            {{ $t('tech-preview.hint') }}
          </span>
          <img
              class="hint__suffix"
              src="../assets/icons/hint.svg"
              alt=""
          />
        </div>
      </div>

      <div class="tech-preview__technologies">
        <tech-details
            icon="strategy.svg"
            :title="$tc('tech-preview.technologies.strategy.title')"
            :description="$tc('tech-preview.technologies.strategy.description')"
            :technologies="$tc('tech-preview.technologies.strategy.technologies')"
        />
        <tech-details
            icon="product.svg"
            :title="$tc('tech-preview.technologies.product.title')"
            :description="$tc('tech-preview.technologies.product.description')"
            :technologies="$tc('tech-preview.technologies.product.technologies')"
        />
        <tech-details
            icon="web.svg"
            :title="$tc('tech-preview.technologies.web.title')"
            :description="$tc('tech-preview.technologies.web.description')"
            :technologies="$tc('tech-preview.technologies.web.technologies')"
        />
        <tech-details
            icon="mobile.svg"
            :title="$tc('tech-preview.technologies.mobile.title')"
            :description="$tc('tech-preview.technologies.mobile.description')"
            :technologies="$tc('tech-preview.technologies.mobile.technologies')"
        />
        <tech-details
            icon="video.svg"
            :title="$tc('tech-preview.technologies.video.title')"
            :description="$tc('tech-preview.technologies.video.description')"
            :technologies="$tc('tech-preview.technologies.video.technologies')"
        />
        <tech-details
            icon="3d.svg"
            :title="$tc('tech-preview.technologies.3d.title')"
            :description="$tc('tech-preview.technologies.3d.description')"
            :technologies="$tc('tech-preview.technologies.3d.technologies')"
        />
      </div>

      <div class="tech-preview__qualities">
        <span class="tech-preview__quantity">
          {{ $t('tech-preview.qualities.flex') }}
        </span>
        <span class="tech-preview__quantity">
          {{ $t('tech-preview.qualities.quality') }}
        </span>
        <span class="tech-preview__quantity">
          {{ $t('tech-preview.qualities.innovation') }}
        </span>
      </div>

      <div class="tech-preview__tag-decoration">
        <img src="../assets/icons/tag.svg" alt="" />
      </div>
    </div>

    <div class="tech-preview__bg-blur"/>
  </div>
</template>

<script>
import TechDetails from '@/components/TechDetails'

export default {
  name: 'tech-preview',
  components: { TechDetails },
}
</script>

<style lang="scss" scoped>
@import "../scss/variables";

.tech-preview {
  position: relative;
  background-color: $tech-preview-bg-color;
}

.tech-preview__wrapper {
  padding: 16.6rem 13.5rem 4.6rem;
}

.tech-preview__bg-blur {
  z-index: 1;
  position: absolute;
  left: 2%;
  right: 4%;
  top: 14%;
  bottom: 26%;
  background: $tech-preview-blur-bg-color;
  filter: blur(50rem);
  border-radius: 10rem;
}

.tech-preview__header {
  z-index: 11;
  display: flex;
  justify-content: space-between;
}

.tech-preview__title,
.tech-preview__hint {
  color: $tech-preview-hint-color;
}

.tech-preview__title-description {
  font-family: 'SF Pro Display', sans-serif;
  white-space: pre-line;
  font-weight: 300;
  font-size: 2rem;
}

.tech-preview__hint {
  display: flex;
  align-items: center;
}

.tech-preview-hint__title {
  font-family: 'SF Pro Display', sans-serif;
  white-space: pre-line;
  text-transform: uppercase;
  letter-spacing: 0.1rem;
  font-weight: 400;
  font-size: 2.2rem;
  padding-right: 0.6rem;
}

.tech-preview__technologies {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 4.6rem 6.8rem;
  margin-top: 18rem;
}

.tech-preview__qualities {
  margin-top: 16rem;
  display: flex;
  justify-content: space-around;
}

.tech-preview__quantity {
  font-family: 'Bebas Neue', sans-serif;
  font-weight: 400;
  font-size: 5.2rem;
  color: $tech-preview-quantity-color;
  border-bottom: 0.1rem solid $tech-preview-quantity-border-color;
}

.tech-preview__tag-decoration {
  display: flex;
  justify-content: center;
  margin-top: 11.2rem;
}
</style>