<template>
  <header>
    <a href="#">
      <img src="../assets/img/la-molisana-logo.png" alt="logo">
    </a>
    <nav>
        <ul>
          <li v-for="(item, index) in menu" :key="index">
            <a :class="{active: item.current}" :href="item.url">{{item.text}}</a>
          </li>
        </ul>
      </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  // sintassi alternativa per le props
  //props:['menu'],

  // sintassi più specifica
  props:{
    menu: Array
  },
  data(){
    return{
    
    }
  }

}
</script>

<style lang="scss">

@import '../assets/style/mixins.scss';
@import '../assets/style/vars.scss';

header{
  text-align: center;
  margin-bottom: 3rem;

  ul{
    @include setupMunu();
    li a{
      display: inline-block;
      text-decoration: none;
      padding: 1rem;
      &:hover,
      &.active {
        background-color: lighten($primary-color, 60%);
      }
    }
  }
}

</style>