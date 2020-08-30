<template>
  <div id="app">
    <h2>Countdown</h2>
    <span>{{contadorSeg }} seg</span>
    <span>{{contadorSeg2 }} seg</span>
    <span>{{contadorSeg3 }} seg</span>
    <span>{{contadorSeg4 }} seg</span>
    <div class="botones">
      <button @click="iniciar1(60)">60 Segs</button>
      <button @click="iniciar2(30)">30 Segs</button>
      <button @click="iniciar3(10)">10 Segs</button>
      <button @click="iniciar4(5)">5 Segs</button>



    </div>
  </div>
</template>

<script>
export default {
  name: "Wla",

  data() {
    return {
      // contadorMin: 0,
      contadorSeg: 60,
      contadorSeg2:30,
      contadorSeg3:10,
      contadorSeg4:5,
      myIntervalo: null,
    };
  },

  methods: {
    iniciar1(time) {
      this.contadorSeg = time;
      clearInterval(this.myIntervalo);
      this.myIntervalo = setInterval(() => {
        this.contadorSeg > 0 ? this.contadorSeg-- : false;
        console.log("Soy el intervalo >:-)");
      }, 1000);
    },
    iniciar2(time) {
      this.contadorSeg2 = time;
      clearInterval(this.myIntervalo);
      this.myIntervalo = setInterval(() => {
        this.contadorSeg2 > 0 ? this.contadorSeg2-- : false;
        console.log("Soy el intervalo >:-)");
      }, 1000);
    },
    iniciar3(time) {
      this.contadorSeg3 = time;
      clearInterval(this.myIntervalo);
      this.myIntervalo = setInterval(() => {
        this.contadorSeg3 > 0 ? this.contadorSeg3-- : false;
        console.log("Soy el intervalo >:-)");
      }, 1000);
    },
    iniciar4(time) {
      this.contadorSeg4 = time;
      clearInterval(this.myIntervalo);
      this.myIntervalo = setInterval(() => {
        this.contadorSeg4 > 0 ? this.contadorSeg4-- : false;
        console.log("Soy el intervalo >:-)");
      }, 1000);
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #83add8;
  margin-top: 60px;
  background-image:url(assets/bg.jpg);
  width: 60%;
  margin: 10rem auto;
  padding: 3rem 0;

  h2 {
    color: blue;
    font-size: 2em;
  }
  button {
    padding: 0.4rem 0.9rem;
    border-radius: 0.3rem;
    font-weight: 700;;
  }
  
}
</style>
