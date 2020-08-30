<template>
  <div id="app">
    <h2>Countdown</h2>
    <!-- se insertan span por cada contador a mostrar -->
    <span>{{contadorSeg }} s</span>
    <span>{{contadorSeg2 }} s</span>
    <span>{{contadorSeg3 }} s</span>
    <span>{{contadorSeg4 }} s</span>
    <!-- se sgrupan en una div los botones  -->
    <div class="botones">
      <button @click="iniciar1(60)">« </button>
      <button @click="iniciar2(30)">« </button>
      <button @click="iniciar3(10)">«</button>
      <button @click="iniciar4(5)"> « </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Wla",

  data() {
    return {
      // return por cada contador,
      contadorSeg: 60,
      contadorSeg2: 30,
      contadorSeg3: 10,
      contadorSeg4: 5,
      myIntervalo: null,
    };
  },
    // se crean metodos por cada boton 
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
      // estilos css personales 
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #83add8;
  margin-top: 60px;
  background-image: url(assets/bg.jpg);
  width: 60%;
  height: 15rem;
  margin: 10rem auto;
  padding: 3rem 0;
  border-radius: 0.4rem;

  h2 {
    color: blue;
    font-size: 2em;
  }
  button {
    margin-top: 0.6rem;
    margin-right: 0.9rem;
    padding: 0.4rem 0.9rem;
    border-radius: 0.3rem;
    font-weight: 700;
  }
  span {
    margin-right: 1.7rem;
    // padding: .2rem;
    color: aqua;
    font-weight: 600;
  }
}
</style>
