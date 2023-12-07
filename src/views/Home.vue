<template>
  <div class="home">
    <nav-bar />
    <get-started />
    <tech-preview />
    <case-studies />
    <amhora-app />
    <jelly-wallet />
    <bitalo-app />
    <about-us />
  </div>
</template>

<script>
import NavBar from '@/components/NavBar'
import GetStarted from '@/views/GetStarted'
import TechPreview from '@/views/TechPreview'
import CaseStudies from '@/views/BookReader'
import AmhoraApp from '@/views/AmhoraApp'
import JellyWallet from '@/views/JellyWallet'
import BitaloApp from '@/views/BitaloApp'
import AboutUs from '@/views/AboutUs'

export default {
  name: 'home',
  components: {
    NavBar,
    GetStarted,
    TechPreview,
    CaseStudies,
    AmhoraApp,
    JellyWallet,
    BitaloApp,
    AboutUs,
  }
}
</script>
