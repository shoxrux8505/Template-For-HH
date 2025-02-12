<template>
  <TopNav />
  <NavBar />
  <MainContent />
  <FlashSales />
  <BbCotigory />
  <BestProducts />
  <JblConetnt />
  <ExploreProducts />
  <Arrival />
  <AdvantureComponent />
  <Footer />
  <!-- <RouterView /> -->
</template>
<script>
// import { RouterLink, RouterView } from 'vue-router'
import TopNav from './components/TopBoard.vue';
import NavBar from '@/components/NavBar.vue'
import MainContent from './components/MainContent.vue';
import FlashSales from './components/FlashSales.vue';
import BbCotigory from './components/BbCotigory.vue';
import BestProducts from './components/BestProducts.vue';
import JblConetnt from './components/JblConetnt.vue';
import ExploreProducts from './components/ExploreProducts.vue';
import Arrival from './components/Arrival.vue';
import AdvantureComponent from './components/AdvantureComponent.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    TopNav,
    NavBar,
    MainContent,
    FlashSales,
    BbCotigory,
    BestProducts,
    JblConetnt,
    ExploreProducts,
    Arrival,
    AdvantureComponent,
    Footer


  }
}
</script>
<style>
a {
  text-decoration: none;
}
</style>
