<template>
  <div class="container">
    <label for="id_nombre">Nombre: </label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" /> <hr>
    <label for="id_apellido">Apellido: </label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" /> <hr>
    <label for="id_edad">Edad: </label>
    <input v-model="nuevaEdad" id="id_edad" type="number" /> <hr>
    <label for="id_genero">Genero: </label>
    <input v-model="nuevoGenero" id="id_genero" type="text" /> <hr>
    <label for="id_semestre">Semestre: </label>
    <input v-model="nuevoSemestre" id="id_semestre" type="number" /> <hr>
    <button v-on:click="agregarEstudiante()">Agregar estudiante</button>
    {{ nuevoNombre }}
    {{ nuevoApellido }}
    {{ nuevaEdad }}
    {{ nuevoGenero }}
    {{ nuevoSemestre }}
    <ul>
      <li v-for="{ nombre, apellido, edad, genero, semestre } in lista" :key="nombre">
        Nombre: {{ nombre }} - Apellido: {{ apellido }} - Edad: {{ edad }} - Genero: {{ genero }} - Semestre: {{ semestre }}
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
      nuevaEdad: 0,
      nuevoGenero: "-",
      nuevoSemestre: 0,
      lista: [
        { nombre: "Edgar", apellido: "Tipan", edad: 18, genero: "Masculino", semestre: 8 },
        { nombre: "Daniel", apellido: "Tipan", edad: 21, genero: "Masculino", semestre: 7 },
        { nombre: "Pedro", apellido: "Teran", edad: 23, genero: "Masculino", semestre: 9 },
        { nombre: "Andrea", apellido: "Tipan", edad: 19, genero: "Femenino", semestre: 6 },
        { nombre: "Carlos", apellido: "Castillo", edad: 20, genero: "Masculino", semestre: 8 },
        { nombre: "Ana", apellido: "Tobar", edad: 22, genero: "Femenino", semestre: 7 },
        { nombre: "Viviana", apellido: "Lopez", edad: 21, genero: "Femenino", semestre: 8 },
      ],
    };
  },
  methods: {
    agregarEstudiante() {
      const nuevo = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
        edad: this.nuevaEdad,
        genero: this.nuevoGenero,
        semestre: this.nuevoSemestre,
      };
      //this.lista.unshift(nuevo);
      this.lista.push(nuevo);
    },
  },
};
</script>

<style>
</style>