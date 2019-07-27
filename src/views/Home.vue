<template>
  <div class="home"> Current Screen: {{this.calculateScreen()}}
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div class="homeCard">
      <!-- <div class="triangle-right"></div> -->
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home',
  components: {

  },
  methods:{
    calculateScreen(){
      var w = window,
      d = document,
      e = d.documentElement,
      g = d.getElementsByTagName('body')[0],
      x = w.innerWidth || e.clientWidth || g.clientWidth,
      y = w.innerHeight|| e.clientHeight|| g.clientHeight;
      return (x + ' × ' + y);

    }
  },
  computed: {
    screen(){
      var w = window,
      d = document,
      e = d.documentElement,
      g = d.getElementsByTagName('body')[0],
      x = w.innerWidth || e.clientWidth || g.clientWidth,
      y = w.innerHeight|| e.clientHeight|| g.clientHeight;
      return (x + ' × ' + y);      
    }
  },
}
</script>

<style lang="scss">
.homeCard{
    background-color: #E1E1E1;
    background: url(../assets/png/bg2.png);
    background-size: 1366px 768px;
    width: 100%;
    padding-bottom: 50%;


      background-repeat: no-repeat;
      background-attachment: fixed;
      background-position: center; 
}

</style>
