<template>
  <v-app>
    <NavBar @scrollToSection="scrollToSection"/>
    <DailyNews class="daily-news-component"/>
    <ServiceAdvantage/>
    <Menu ref="menu"/>
    <Delivery ref="delivery"/>
    <Testimonlial/>
    <FAQ ref="faq"/>
    <AboutUs/>
    <SpecialOffer/>
    <Footer/>
  </v-app>
</template>
<style>

@import './assets/styles/style.css';
</style>
<script>
import NavBar from './components/NavBar';
import DailyNews from './components/DailyNews';
import ServiceAdvantage from './components/ServiceAdvantage';
import Menu from './components/Menu';
import Delivery from './components/Delivery';
import Testimonlial from './components/Testimonlial';
import FAQ from './components/FAQ';
import AboutUs from './components/AboutUs';
import SpecialOffer from './components/SpecialOffer'
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    NavBar,
    DailyNews,
    ServiceAdvantage,
    Menu,
    Delivery,
    Testimonlial,
    FAQ,
    AboutUs,
    SpecialOffer,
    Footer
  },
  methods: {
    scrollToSection(sectionRef) {
      const element = this.$refs[sectionRef].$el;

      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
  },
};
</script>
