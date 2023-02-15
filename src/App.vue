<template>
  <v-app>
    <Header />
    <v-main>
      <Hero />
      <About />
      <Portfolio />
      <Project />
      <Gallery />
      <ContactUs />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import About from "./components/About.vue";
import Portfolio from "./components/Portfolio.vue";
import Project from "./components/Project.vue";
import Gallery from "./components/Gallery.vue";
import ContactUs from "./components/ContactUs.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",

  components: {
    Header,
    Hero,
    About,
    Portfolio,
    Project,
    Gallery,
    ContactUs,
    Footer,
  },
};
</script>
