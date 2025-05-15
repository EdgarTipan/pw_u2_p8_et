<template>
  <div class="container">
    <h1>Contador</h1>
    <p>{{ this.numero }}<sup>2</sup> = {{ calCuadrado }}</p>
    <div>
      <button v-on:click="incrementar()">+ 1</button>
      <button v-on:click="decrementar()">- 1</button>
    </div>
    <!--
    <p>{{ numero + 1 }}</p>
    <p>{{ texto }}</p>
    <p>{{ activo }}</p>
    <p>{{ usuario.edad }}</p>
    <p>{{ arreglo }}</p>
    1+1
    {{ 1 + 1 }}
    true?'Es verdadero':'Es falso'
    {{ false ? "Es verdadero" : "Es falso" }}
    -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      numero: 5,
      texto: "Edgar Tipan",
      activo: true,
      usuario: {
        nombre: "Edgar",
        edad: 23,
        genero: "M",
      },
      arreglo: ["Amarillo", "Azul"],
    };
  },
  methods: {
    calcularCuadrado() {
      console.log("Entro al metodo");
      return this.numero * this.numero;
    },
    incrementar() {
      this.numero++;
    },
    decrementar() {
      this.numero--;
    },
  },
  computed: {
    calCuadrado() {
      console.log("Entro a la propiedad computada");
      return this.numero * this.numero;
    },
  },
};
</script>

<style>
</style>