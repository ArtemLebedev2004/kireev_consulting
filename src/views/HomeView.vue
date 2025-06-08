<template>
  <header id="">
    <navBar />
  </header>

  <!-- <section id="main">
    <mainSection />
  </section>

  <section id="projects">
    <projectsSection />
  </section>

  <section id="services">
    <servicesSection />
  </section>

  <section id="about">
    <aboutSection @id-active="idActiveEmit" />
  </section> -->

  <footer id="contacts">
    <footerContacts :idActive="idActive" />
  </footer>
</template>

<script setup>

// import mainSection from '../components/sections/HomeViewSections/mainSection.vue';
// import projectsSection from '../components/sections/HomeViewSections/projectsSection.vue';
// import servicesSection from '../components/sections/HomeViewSections/servicesSection.vue';
// import aboutSection from '../components/sections/HomeViewSections/aboutSection.vue';
import navBar from '../components/structure/navBar.vue';
// import footerContacts from '@/components/structure/footerContacts.vue';
import { ref } from 'vue';

let idActive = ref(null)

// let idActiveEmit = (data) => {
//   idActive.value = data
// }
</script>

<style>
#main:before, #projects:before, #services:before, #about:before {
	display: block;
	content: "";
	height: 55px;
	margin: -55px 0 0;
}
</style>