<template>
  <div class="home">

    <NavbarSection />
    <HeroSection />
  </div>
</template>

<script>
// @ is an alias to /src

import NavbarSection from '@/components/NavbarSection.vue'
import HeroSection from '@/components/HeroSection.vue';

export default {
  components: {
   NavbarSection,
   HeroSection
  }
}
</script>
