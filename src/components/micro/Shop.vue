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
            img: require('../../assets/img/buy-comics-digital-comics.png'),
            text: 'digital comics'
          },
           {
            img: require('../../assets/img/buy-comics-merchandise.png'),
            text: 'dc merchandise'
          },
           {
            img: require('../../assets/img/buy-comics-subscriptions.png'),
            text: 'subscription'
          },
           {
            img: require('../../assets/img/buy-comics-shop-locator.png'),
            text: 'comic shop locator'
          },
           {
            img: require('../../assets/img/buy-dc-power-visa.svg'),
            text: 'dc power visa'
          }
        ]
      }
    }
}
</script>

<style scoped lang="scss">
.container{
  margin: 0 auto;
  width: 100%;
}

.merch{
  width: 100%;
  display: flex;
  justify-content: space-around;
  

  div{
    width: 15%;
    display: flex;
    justify-content: start;
    align-items: center;

    a{
      margin-left: 10px;
      text-decoration: none;
      text-transform: uppercase;
      color: #fff;
      font-size: 15px;

      &:hover{
        text-decoration: underline;
      }
    }
  }

  
}

img{
  height: 40px;  
}
</style>