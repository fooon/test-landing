<template>
  <div class="content">
    <Header />
    <Services />
    <Advantages />
    <HowItsWork />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Advantages from "./components/Advantages.vue";
import Services from './components/Services.vue'
import HowItsWork from './components/HowItsWork.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Services,
    Advantages,
    HowItsWork,
    Footer
  }
}
</script>

<style lang="scss">
.content {
  background: url("./assets/main-bg.png") no-repeat;
  background-size: contain;
  background-color: #1B1843;
  padding: 0 120px 0 120px;
  
  @media(max-width: 768px){
    padding: 0 30px 0 30px;
  }
}

</style>
