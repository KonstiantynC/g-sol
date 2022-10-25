<template>
  <div class="tech-details">
    <div class="tech-details__icon-wrp">
      <img
          :src="require(`@/assets/icons/${icon}`)"
          alt=""
      />
    </div>
    <span class="tech-details__title">
      {{ title }}
    </span>
    <p class="tech-details__description">
      {{ description }}
    </p>
    <span class="tech-details__technologies">
      {{ technologies }}
    </span>
  </div>
</template>

<script>
export default {
  props: {
    icon: {type: String, required: true},
    title: {type: String, required: true},
    description: {type: String, required: true},
    technologies: {type: String, required: true},
  },
  name: 'tech-details'
}
</script>

<style scoped lang="scss">
@import "../scss/variables";

.tech-details {
  z-index: 11;
  padding: 6rem 3rem 3.2rem;
  position: relative;

  &:before {
    z-index: 11;
    content: '';
    box-sizing: border-box;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    position: absolute;
    border: 0.4rem solid $tech-details-border-color;
    background: linear-gradient(140deg,
        transparent 0%,
        $tech-details-gradient-color 40%,
        $tech-details-gradient-color 60%,
        transparent 100%);
  }

  &:after {
    z-index: 1;
    content: '';
    box-sizing: border-box;
    left: 1.2rem;
    top: 1.2rem;
    width: 100%;
    height: 100%;
    position: absolute;
    border: 0.4rem solid $tech-details-scale-border-color;
  }
}

.tech-details__icon-wrp {
  display: flex;
  justify-content: center;
  margin-bottom: 4rem;
}

.tech-details__title {
  font-family: 'SF Pro Display', sans-serif;
  white-space: pre-line;
  color: $tech-details-title-color;
  font-weight: 400;
  font-size: 2rem;
}

.tech-details__description {
  min-height: 10rem;
  font-family: 'SF Pro Display', sans-serif;
  font-weight: 200;
  font-size: 1.6rem;
  color: $tech-details-description-color;
  margin-top: 1.2rem;
  margin-bottom: 3rem;
}

.tech-details__technologies {
  font-family: 'SF Pro Display', sans-serif;
  font-weight: 400;
  font-size: 16px;
  color: $tech-details-technologies-color;
}
</style>