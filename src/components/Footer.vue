<template>
  <footer>
        <div class="shop-merch-container">
            <Shop/>
        </div>
        <div class="foot-mid">
                <div class="foot-links">
                    <div class="left-links">

                        <div class="dc-comics">
                            DC Comics
                            <a v-for="(link, index) in dcComicsLinks" :key="index" href="#">{{link.text}}</a>
                        </div>
                        <div class="dc-shop">
                            Shop
                            <a v-for="(link, index) in shopLinks" :key="index" href="#">{{link.text}}</a>
                        </div>
                    </div>

                    <div class="mid-links">
                        <div class="dc">
                            Dc
                            <a v-for="(link, index) in dcLinks" :key="index" href="#">{{link.text}}</a>
                        </div>            
                    </div>

                    <div class="right-links">
                        <div class="sites">
                            Sites
                            <a v-for="(link, index) in sitesLinks" :key="index" href="#">{{link.text}}</a>
                        </div>                  
                    </div>

                </div>
                <div>
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>            
        </div>
        <div class="foot-bottom">
            <div class="sign-up">
                sign-up now!
            </div>
            <div class="socials">
                FOLLOW US
                <img :src="image.img" v-for="(image, index) in socialsLogo" :key="index">
            </div>
        </div>
  </footer>
</template>

<script>
import Shop from './micro/Shop.vue';

export default {
    name: 'Footer',
    components:{
        Shop,
    },
    data(){
        return{
            dcComicsLinks: [
                {
                    text: 'Characters'
                },
                {
                    text: 'Comics'
                },
                {
                    text: 'Movies'
                },
                {
                    text: 'TV'
                },
                {
                    text: 'Games'
                },
                {
                    text: 'Videos'
                },
                {
                    text: 'News'
                },
            ],
            shopLinks:[
               {
                   text: 'Shop DC'
               }, 
               {
                   text: 'Shop DC Collectibles'
               }
            ],
            dcLinks: [
                {
                    text: 'Terms Of Use'
                },
                {
                    text: 'Privacy Policy (New)'
                },
                {
                    text: 'Ad Choices'
                },
                {
                    text: 'Advertising'
                },
                {
                    text: 'Jobs'
                },
                {
                    text: 'Subscriptions'
                },
                {
                    text: 'Talent Workshops'
                },
                {
                    text: 'CPSC Certificates'
                },
                {
                    text: 'Ratings'
                },
                {
                    text: 'Shop Help'
                },
                {
                    text: 'Contact Us'
                },
            ],
            sitesLinks: [
                {
                    text: 'DC'
                },
                {
                    text: 'MAD Magazine'
                },
                {
                    text: 'DC Kids'
                },
                {
                    text: 'DC Universe'
                },
                {
                    text: 'DC Power Visa'
                },
            ],
            socialsLogo: [
                {
                    img: require('../assets/img/footer-facebook.png')
                },
                {
                    img: require('../assets/img/footer-twitter.png')
                },
                {
                    img: require('../assets/img/footer-youtube.png')
                },
                {
                    img: require('../assets/img/footer-pinterest.png')
                },
                {
                    img: require('../assets/img/footer-periscope.png')
                },
            ]
        }
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
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.foot-mid{
    overflow: hidden;
    height: 300px;
    background-image: url(../assets/img/footer-bg.jpg);
    display: flex;
    justify-content: space-around;
    align-items: center;


    .foot-links{
        display: flex;
        justify-content: space-between;
        width: 35%;
        margin-left: 45px;

        

        .dc-comics, .dc-shop, .dc, .sites{
            display: flex;
            flex-direction: column;
            color: #fff;
            font-weight: bold;
            font-size: 18px;
            margin-top: 5px;
            
            

            a{
                text-decoration: none;
                margin: 3px 0;
                color: grey;
                font-weight: lighter;
                font-size: 13px;

                &:hover{
                    text-decoration: underline;
                }
            }
            
        }
    }
}

.foot-bottom{
    padding: 0 200px;
    height: 100px;
    background-color: #303030;
    display: flex;
    justify-content: space-between;
    align-items: center;


    .socials{
        width: 25%;
        font-weight: bold;
        color: #fff;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .sign-up{
        color: #fff;
        padding: 10px;
        width: 130px;
        text-transform: uppercase;
        border: 2px solid $navcolor;
    }
}
</style>