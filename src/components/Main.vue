<template>
  <main>
    <h1>Lista prodotti</h1>
    <div class="container boxes">

        <ProductCard 
          v-for="(product, index) in productsItems"  
          :key="index" 
          :product="product"
         />

    </div>

  </main>
</template>

<script>

import ProductCard from './ProductCard';
import productsItems from '../assets/data/productData.js';

export default {
  name: 'Main',
  components:{
    ProductCard
  },
  data(){
    return{
      productsItems,
      
    }
  }
}
</script>

<style lang="scss">

@import '../assets/style/mixins.scss';
@import '../assets/style/vars.scss';

  main{
    background-image: url('../assets/img/fondo-pag-speciali.jpg');
    padding: 3rem;
    text-align: center;
    h1{
      color: $primary-color;
      font-size: 20px;
      margin-bottom: 1rem;
    }
    .boxes{
      display: flex;
      flex-wrap: wrap;
    }
  }
</style>