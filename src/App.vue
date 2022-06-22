<template>
  <main class="main__container">
    <NavBar />
    <HeaderSection />
    <ServicesSection />
    <PortfolioSection />
    <TestimonialsSection />
    <NewsSection />
    <FooterSection />
  </main>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import HeaderSection from "./components/HeaderSection.vue";
import ServicesSection from "./components/ServicesSection.vue";
import PortfolioSection from "./components/PortfolioSection.vue";
import TestimonialsSection from "./components/TestimonialsSection.vue";
import NewsSection from "./components/NewsSection.vue";
import FooterSection from "./components/FooterSection.vue";

export default {
  components: {
    NavBar,
    HeaderSection,
    ServicesSection,
    PortfolioSection,
    TestimonialsSection,
    NewsSection,
    FooterSection,
  },
};
</script>

<style lang="scss">
@import "./assets/styles/main.scss";
@font-face {
  font-family: "Roboto";
  src: local("Roboto"), url(./fonts/Roboto-Medium.ttf) format("truetype");
}
@font-face {
  font-family: "Roboto-Regular";
  src: local("Roboto-Regular"),
    url(./fonts/Roboto-Regular.ttf) format("truetype");
}
</style>
