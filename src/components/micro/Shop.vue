<template>
  <div v-for="(element, index) in merchElement" :key="index" class="merch">
    <img :src="element.img" alt="">
    <span></span>
  </div>
</template>

<script>
export default {
    name: 'Shop',
    data(){
      return{
        merchElement: [
          {
            img: '../../assets/img/buy-comics-digital-comics.png',
            text: 'digital comics'
          },
           {
            img: '../../assets/img/buy-comics-merchandise.png',
            text: 'dc merchandise'
          },
           {
            img: '../../assets/img/buy-comics-subscription.png',
            text: 'subscription'
          },
           {
            img: '../../assets/img/buy-comics-shop-locator.png',
            text: 'comic shop locator'
          },
           {
            img: '../../assets/img/buy-dc-power-visa.svg',
            text: 'dc power visa'
          }
        ]
      }
    }
}
</script>

<style>

</style>