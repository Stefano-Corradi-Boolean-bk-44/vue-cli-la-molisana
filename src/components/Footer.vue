<template>
  <footer>
    <div class="container cols">
      <div class="logo">
       <img src="../assets/img/la-molisana-logo.png" alt="logo">
      </div>
      <div class="footer-links">
        <h4>pastificio</h4>
        <ul>
          <li><a href="#">Il pastificio</a></li>
          <li><a href="#">Grano</a></li>
          <li><a href="#">Filiera</a></li>
          <li><a href="#">100 anni di pasta</a></li>
          <li><a href="#">Storia della pasta</a></li>
        </ul>
      </div>
      <div class="footer-links">
        <h4>prodotti</h4>
        <ul>
          <li><a href="#">Le Classiche</a></li>
          <li><a href="#">Le Integrali</a></li>
          <li><a href="#">Le speciali</a></li>
          <li><a href="#">Le Biologiche</a></li>
          <li><a href="#">Le Glutin-free</a></li>
        </ul>
      </div>
    </div>
    <img src="../assets/img/footer-montagne-bottom.jpg" alt="logo">
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data(){
    return{
      
    }
  }
}
</script>

<style lang="scss">

@import "../assets/style/vars.scss";

footer{
  margin-top: 3rem;
  .cols{
    display: flex;
    .logo,
    .footer-links{
      flex-basis: calc(100%/3);
      h4{
        color: $primary-color;
        text-transform: uppercase;
        margin-bottom: 1rem;
      }
    }
    ul{
      list-style: none;
      a {
        text-decoration: none;
        display: inline-block;
        font-size: 0.9rem;
        margin-bottom: 0.25rem;
        &:hover{
          color: $primary-color;
        }
      }
    }
  }
}

</style>