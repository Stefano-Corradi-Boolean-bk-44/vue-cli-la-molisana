<template>
  <header>
    <a href="#">
      <img src="../assets/img/la-molisana-logo.png" alt="logo">
    </a>
    <nav>
        <ul>
          <li v-for="(item, index) in links" :key="index">
            <a :class="{active: item.current}" :href="item.url">{{item.text}}</a>
          </li>
        </ul>
      </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return{
      links:[
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
  }

}
</script>

<style lang="scss">

@import '../assets/style/mixins.scss';

header{
  text-align: center;
  margin-bottom: 3rem;

  ul{
    @include center();
    list-style: none;
    li a{
      display: inline-block;
      text-decoration: none;
      padding: 1rem;
      &:hover,
      &.active {
        background-color: cadetblue;
      }
    }
  }
}

</style>