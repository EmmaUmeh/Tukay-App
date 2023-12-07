<script setup>
import Navbar from './components/Navbar.vue';
import HeroSection from './components/HeroSection.vue';
import SectionOne from './components/SectionOne.vue';
import SectionBanner from './components/SectionBanner.vue';
import SectionTwo from './components/SectionTwo.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <header>
   <div class="wrapper">
      <Navbar/>
    </div>
  </header>

  <main>
    <HeroSection />
  </main>
  
  <div>
    <SectionOne text="What you stand to benefit"/>
    <SectionBanner />
    <SectionTwo />
    <Footer />
  </div>
</template>