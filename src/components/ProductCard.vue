<template>
  <div class="product-card">
    <img :src="product.src" :alt="product.titolo">
    <h3>{{product.titolo}}</h3>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props:{
    product: Object,
  }
}
</script>



<style lang="scss">
@import '../assets/style/mixins.scss';
@import '../assets/style/vars.scss';

.product-card{
  flex-basis: 25%;
  background-color: white;
  padding: 1rem;
  border: 2px solid lighten($primary-color, 70%);
  h3{
    color: $primary-color
  }
}

</style>