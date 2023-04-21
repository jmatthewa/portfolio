<template>
 

  <NavbarSection />
  <HeroSection />
  <AboutSection />
  <ProjectsSection />
  <SkillsSection />
  <ContactSection />
  <SocialLinks />
  <FooterSection />



</template>

<script>

import NavbarSection from '@/components/NavbarSection.vue'
import HeroSection from '@/components/HeroSection.vue';
import SocialLinks from '@/components/SocialLinks.vue';
import AboutSection from '@/components/AboutSection.vue';
import ProjectsSection from '@/components/ProjectsSection.vue'
import SkillsSection from './components/SkillsSection.vue';
import ContactSection from './components/ContactSection.vue';
import FooterSection from './components/FooterSection.vue';


export default {
  components: {
   NavbarSection,
   HeroSection,
   SocialLinks,
   AboutSection,
   ProjectsSection,
   SkillsSection,
   ContactSection,
   FooterSection
  }
}

</script>
<style>

</style>
