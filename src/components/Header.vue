<template>
  <header>
      <div class="container">
        <div class="logo-dc">
          <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <nav>
          <ul>
            <li v-for="(link, index) in links" :key="index" :class="{'active' : link.current}">
              <a href="#" >{{link.text}}</a>
            </li>
          </ul>
        </nav>
      </div>
  </header>
</template>

<script>
export default {
  name: 'Header',  
  data(){
    return {
      links: [
        {
          text: 'Characters',
          url: '#',
          current: false,
        },
        {
          text: 'Comics',
          url: '#',
          current: true,
        },
        {
          text: 'Movies',
          url: '#',
          current: false,
        },
        {
          text: 'TV',
          url: '#',
          current: false,
        },
        {
          text: 'Games',
          url: '#',
          current: false,
        },
        {
          text: 'Collectibles',
          url: '#',
          current: false,
        },
        {
          text: 'Fans',
          url: '#',
          current: false,
        },
        {
          text: 'News',
          url: '#',
          current: false,
        },
        {
          text: 'Shop',
          url: '#',
          current: false,
        },
      ]
    }   
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/partials/variables.scss';
  .container{
    height: 130px;
    max-width: 1500px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  nav{
    width: 70%;
    height: 100%;

    ul{
      padding: 0;
      width: 100%;
      display: flex;
      justify-content: space-between;
      list-style-type: none;

      li{
        text-align: center;
        width: 115px;
        font-size: 15px;
        text-transform: uppercase;
        font-weight: bold;
        height: 100%;
        line-height: 125px;

        &.active, &:hover{
          border-bottom: 5px solid $navcolor;
          color: $navcolor;
        }

        a{
        text-decoration: none;
        color: #000;

        
      }
      } 
    }
  }
</style>
