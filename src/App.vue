<template>
 

  <NavbarSection />
  <HeroSection />
  <AboutSection />
  <ProjectsSection />
  <SkillsSection />
  <ContactSection />
  <SocialLinks />




</template>

<script>

import NavbarSection from '@/components/NavbarSection.vue'
import HeroSection from '@/components/HeroSection.vue';
import SocialLinks from '@/components/SocialLinks.vue';
import AboutSection from '@/components/AboutSection.vue';
import ProjectsSection from '@/components/ProjectsSection.vue'
import SkillsSection from './components/SkillsSection.vue';
import ContactSection from './components/ContactSection.vue';

export default {
  components: {
   NavbarSection,
   HeroSection,
   SocialLinks,
   AboutSection,
   ProjectsSection,
   SkillsSection,
   ContactSection
  }
}

</script>
<style>

</style>
