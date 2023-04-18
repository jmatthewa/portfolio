<template>
  <div class="home">

    <NavbarSection />
    <HeroSection />
    <AboutSection />
    <ProjectsSection />

    <SkillsSection />
    <SocialLinks />

  </div>
</template>

<script>

import NavbarSection from '@/components/NavbarSection.vue'
import HeroSection from '@/components/HeroSection.vue';
import SocialLinks from '@/components/SocialLinks.vue';
import AboutSection from '@/components/AboutSection.vue';
import ProjectsSection from '@/components/ProjectsSection.vue'
import SkillsSection from './components/SkillsSection.vue';

export default {
  components: {
   NavbarSection,
   HeroSection,
   SocialLinks,
   AboutSection,
   ProjectsSection,
   SkillsSection
  }
}

</script>
<style>

</style>
