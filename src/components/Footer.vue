<template>
  <footer>
      <div class="shop-merch-container">
          <Shop/>
      </div>
      
  </footer>
</template>

<script>
import Shop from './micro/Shop.vue';

export default {
    name: 'Footer',
    components:{
        Shop,
    }
}
</script>

<style scoped lang="scss">
@import '../assets/style/partials/variables.scss';

footer{
    height: 500px;
}

.shop-merch-container{
    height: 150px;
    background-color: $navcolor;
}
</style>