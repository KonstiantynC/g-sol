<template>
  <div class="about-us app__page">
    <div class="about-us__wrapper app__wrapper">
      <div class="about-us__preview">
        <div class="about-us__title-wrapper">
          <span class="about-us__subtitle">
            {{ $t('about-us.subtitle') }}
          </span>
          <h1 class="about-us__title">
            {{ $t('about-us.title') }}
          </h1>
        </div>
        <div class="about-us__info">
          <div class="about-us__about-team">
            <p class="about-us__about-team-text">
              {{ $t('about-us.about-team.name') }}
            </p>
            <p class="about-us__about-team-text">
              {{ $t('about-us.about-team.ideas') }}
            </p>
            <p class="about-us__about-team-text">
              {{ $t('about-us.about-team.products') }}
            </p>
          </div>

          <div class="about-us__comment">
            <p class="about-us__comment-text">
              {{ $t('about-us.comment') }}
            </p>

            <div class="about-us__founder">
              <img
                  class="about-us__founder-img"
                  src="../assets/founder.png"
                  alt=""
              >
              <div class="about-us__founder-details">
                <span class="about-us__founder-name">
                  {{ $t('about-us.founder') }}
                </span>
                <span class="about-us__founder-label">
                  {{ $t('about-us.founder-lbl') }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="about-us__text-decoration-wrapper">
        <img
            class="about-us__text-decoration"
            src="../assets/objective-text.svg"
            alt=""
        >
      </div>
    </div>

    <div class="about-us__bg-blur-left" />
    <div class="about-us__bg-blur-right" />
    <img
        class="about-us__bg-decoration"
        src="../assets/about-us-bg-decoration.png"
        alt=""
    />
  </div>
</template>

<script>
export default {
  name: 'about-us',
}
</script>

<style scoped lang="scss">
@import "../scss/variables";

.about-us {
  position: relative;
  background-color: $about-us-bg-color;
}

.about-us__bg-blur-left {
  z-index: 1;
  position: absolute;
  width: 72rem;
  height: 20rem;
  left: 6.6rem;
  top: 42rem;
  background: $about-us-left-blur-bg-color;
  filter: blur(21rem);
  transform: rotate(1.51deg);
}

.about-us__bg-blur-right {
  z-index: 1;
  position: absolute;
  width: 37rem;
  height: 27rem;
  left: 90rem;
  top: 36rem;
  background: $about-us-right-blur-bg-color;
  filter: blur(15rem);
}

.about-us__bg-decoration {
  z-index: 0;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.about-us__wrapper {
  z-index: 1;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 95.5rem;
  padding: 6.6rem 13.5rem 0;
}

.about-us__title {
  font-family: 'Bebas Neue', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 13rem;
  text-transform: uppercase;
  color: $about-us-text-color;
}

.about-us__subtitle {
  font-family: 'SF Pro Display', sans-serif;
  font-style: normal;
  font-weight: 300;
  font-size: 1.6rem;
  text-transform: uppercase;
  color: $about-us-text-color;
}

.about-us__info {
  margin-top: 7.2rem;
  display: flex;
  justify-content: space-between;
}

.about-us__about-team {
  width: 64rem;
}

.about-us__comment {
  width: 32rem;
}

.about-us__about-team-text {
  color: $about-us-text-color;
  font-family: 'SF Pro', sans-serif;
  font-style: normal;
  font-weight: 200;
  font-size: 2rem;
  margin-bottom: 4.2rem;
}

.about-us__comment-text {
  font-family: 'SF Pro Display', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 2.8rem;
  color: $about-us-text-color;
}

.about-us__founder {
  display: flex;
  margin-top: 3.8rem;
}

.about-us__founder-img {
  width: 5.8rem;
  height: 5.8rem;
}

.about-us__founder-details {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 1rem;
}

.about-us__founder-name {
  font-family: 'SF Pro Display', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 1.8rem;
  color: #FFFFFF;
}

.about-us__founder-label {
  font-family: 'SF Pro Display', sans-serif;
  font-style: normal;
  font-weight: 300;
  font-size: 1.4rem;
  color: $about-us-text-color;
}

.about-us__text-decoration-wrapper {
  display: flex;
  justify-content: center;
}
</style>