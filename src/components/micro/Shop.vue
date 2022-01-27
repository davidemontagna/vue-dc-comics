<template>
  <div class="container">
    <div class="merch">
      <div v-for="(element, index) in merchElement" :key="index" >
        <img :src="element.img" alt="">
        <a href="">{{element.text}}</a>
      </div>
    </div> 
  </div>
   
</template>

<script>
export default {
    name: 'Shop',
    data(){
      return{
        merchElement: [
          {
            img: './src/assets/img/buy-comics-digital-comics.png',
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

<style scoped lang="scss">

.merch{
  width: 1000px;
  display: flex;
  justify-content: space-between;

  div a{
    text-decoration: none;
    text-transform: uppercase;
    color: #fff;
    font-size: 15px;
  }
}

img{
  width: 50px;
  height: 50px;
  background-color: #fff;
}
</style>