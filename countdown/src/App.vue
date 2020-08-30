<template>
  <div id="app">
    <h2>Countdown</h2>
    <h1>{{contadorSeg }} seg</h1>
    <div class="botones">
      <button @click="iniciar(59)">press me</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Wla",

  data() {
    return {
      contadorMin: 0,
      contadorSeg: 0,
      myIntervalo: null,
    };
  },

  methods: {
    iniciar(time) {
      this.contadorSeg = time;
      clearInterval(this.myIntervalo);
      this.myIntervalo = setInterval(() => {
        this.contadorSeg > 0 ? this.contadorSeg-- : false;
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
