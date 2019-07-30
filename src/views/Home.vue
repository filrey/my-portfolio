<template>
  <div class="home">
    <v-container fluid fill-height>
      <v-layout align-center justify-left>
        <v-flex xs12 sm12 md7>
          <v-card class="cardSlide">
          <v-sheet class="elevation-12">

            <v-img src="../assets/png/bg3.png"></v-img>

          </v-sheet>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    Current Screen: {{this.calculateScreen()}}
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  components: {},
  methods: {
    calculateScreen() {
      var w = window,
        d = document,
        e = d.documentElement,
        g = d.getElementsByTagName("body")[0],
        x = w.innerWidth || e.clientWidth || g.clientWidth,
        y = w.innerHeight || e.clientHeight || g.clientHeight;
      return x + " × " + y;
    }
  },
  computed: {
    screen() {
      var w = window,
        d = document,
        e = d.documentElement,
        g = d.getElementsByTagName("body")[0],
        x = w.innerWidth || e.clientWidth || g.clientWidth,
        y = w.innerHeight || e.clientHeight || g.clientHeight;
      return x + " × " + y;
    }
  }
};
</script>
<style lang="scss">
.homeCard {
  background-color: #e1e1e1;
  background: url(../assets/png/bg2.png);
  background-size: 1366px 768px;
  width: 100%;
  padding-bottom: 50%;

  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
}

.cardSlide{
  -webkit-animation: mymove 1s infinite; /* Safari 4.0 - 8.0 */
  animation: slideIn 1s infinite;
}
@keyframes slideIn {
  from {left: -1000px;}
  to {left: 0px;}
}

</style>