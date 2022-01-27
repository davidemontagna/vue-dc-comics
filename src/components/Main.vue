<template>
  <main>
    <div class="container">
      <div class="main-container">
        <span> -- Content goes here -- </span>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
  props: {
    msg: String
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/partials/variables.scss';

  main{
    
    background-color: #1c1c1c;

    .main-container{
      display: flex;
      align-items: center;
      height: 100px;

      span{
        font-size: 20px;
        color: #fff;
      }
    }
  }
</style>
