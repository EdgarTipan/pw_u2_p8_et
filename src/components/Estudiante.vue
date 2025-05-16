<template>
  <div class="container">
    <label for="id_nombre">Nombre: </label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
    <label for="id_apellido">Apellido: </label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />
    <button v-on:click="agregarEstudiante()">Agregar estudiante</button>
    {{ nuevoNombre }}
    {{ nuevoApellido }}
    <ul>
      <li v-for="{ nombre, apellido } in lista" :key="nombre">
        Nombre: {{ nombre }} - Apellido: {{ apellido }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "Nuevo",
      nuevoApellido: "Estudiante",
      lista: [
        { nombre: "Edgar", apellido: "Tipan" },
        { nombre: "Daniel", apellido: "Tipan" },
        { nombre: "Pedro", apellido: "Teran" },
        { nombre: "Andrea", apellido: "Tipan" },
        { nombre: "Carlos", apellido: "Castillo" },
        { nombre: "Ana", apellido: "Tobar" },
        { nombre: "Viviana", apellido: "Lopez" },
      ],
    };
  },
  methods: {
    agregarEstudiante() {
      const nuevo = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
      };
      //this.lista.unshift(nuevo);
      this.lista.push(nuevo);
    },
  },
};
</script>

<style>
</style>