<script setup>
import { ref } from 'vue'
import TopNavBar from './components/TopNavBar.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Gallery from './components/Gallery.vue'
import Contact from './components/Contact.vue'

const homeRef = ref(null);
const aboutRef = ref(null);
const projectsRef = ref(null);
const galleryRef = ref(null);
const contactRef = ref(null);

const handleNavigation = (section) => {
  if (section === 'home' && homeRef.value) {
    homeRef.value.scrollIntoView({ behavior: 'smooth' });
  } else if (section === 'about' && aboutRef.value) {
    aboutRef.value.scrollIntoView({ behavior: 'smooth' });
  } else if (section === 'projects' && projectsRef.value) {
    projectsRef.value.scrollIntoView({ behavior: 'smooth' });
  } else if (section === 'gallery' && galleryRef.value) {
    galleryRef.value.scrollIntoView({ behavior: 'smooth' });
  } else if (section === 'contact' && contactRef.value) {
    contactRef.value.scrollIntoView({ behavior: 'smooth' });
  }
}
</script>

<template>
  <TopNavBar @navigate="handleNavigation"></TopNavBar>
  <section ref="homeRef">
    <Home></Home>
  </section>
  <section ref="aboutRef">
    <About></About>
  </section>
  <section ref="projectsRef">
    <Projects></Projects>
  </section>
  <section ref="galleryRef">
    <Gallery></Gallery>
  </section>
  <section ref="contactRef">
    <Contact></Contact>
  </section>
</template>

<style scoped>
  section {
    padding: 4rem 0;
  }
</style>
