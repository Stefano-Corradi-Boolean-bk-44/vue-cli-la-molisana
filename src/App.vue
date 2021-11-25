<template>
  <div >
    <Header :menu="linksList" />
    <Main />
    <Footer />
  </div>
</template>

<script>

import Header from './components/Header';
import Main from './components/Main';
import Footer from './components/Footer';

export default {
  name: 'App',
  data(){
    return{
      linksList:[
        {
          url:'/',
          text: 'Home',
          current: false
        },
        {
          url:'/prodotti',
          text: 'Prodotti',
          current: true
        },
        {
          url:'/chi-siamo',
          text: 'Chi siamo',
          current: false
        },
        {
          url:'/contatti',
          text: 'Contatti',
          current: false
        },
      ]
    }
  },
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">

@import "./assets/style/vars.scss";
@import "./assets/style/generals.scss";
@import "./assets/style/utilities.scss";


</style>
