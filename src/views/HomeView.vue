<template>
  <div class="home">

    <NavbarSection />
    <HeroSection />
    <AboutSection />
    <SocialLinks />
    
  </div>
</template>

<script>
// @ is an alias to /src

import NavbarSection from '@/components/NavbarSection.vue'
import HeroSection from '@/components/HeroSection.vue';
import SocialLinks from '@/components/SocialLinks.vue';
import AboutSection from '@/components/AboutSection.vue';


export default {
  components: {
   NavbarSection,
   HeroSection,
   SocialLinks,
   AboutSection
  }
}
</script>
