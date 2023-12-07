<template>
  <div class="contact-us">
    <div class="contact-us__wrapper">
      <div class="contact-us__info">
        <div class="contact-us__title-wrp">
          <div class="contact-us__title">
            {{ $t('contact-us.title') }}
          </div>
          <div class="contact-us__contact-details">
            {{ $t('contact-us.contact-details.') }}
          </div>
        </div>
        <div class="contact-us__call-info">
          <div class="contact-us__phone-number">

          </div>
          <div class="contact-us__e-mail">
            
          </div>
          <div class="contact-us__messenger">
            <img src="" alt="">
            <img src="" alt="">
            <img src="" alt="">
          </div>
          <div class="contact-us__adress">
            {{ $t('contact-us.adress') }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'contact-us',
  components: {
    
  },
  data: () => ({
    
  })
}
</script>


<style scoped lang="scss">
@import "@/scss/variables.scss";


</style>