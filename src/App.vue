<template>
  <!-- <HolaMundoView/> -->
  <!-- <ContadorView/> -->
  <!-- <EstudianteView/> -->
  <!-- <EstudianteTablaViewVue/> -->
  <!-- <LibroTablaView/> -->
  <PreguntaView/>
</template>

<script>
import HolaMundoView from "@/views/HolaMundoView.vue";
import ContadorView from "@/views/ContadorView.vue";
import EstudianteView from "@/views/EstudianteView.vue";
import EstudianteTablaViewVue from '@/views/EstudianteTablaView.vue';
import LibroTablaView from '@/views/LibroTablaView.vue';
import PreguntaView from '@/views/PreguntaView.vue';

export default {
  name: "App",
  components: {
    HolaMundoView,
    ContadorView,
    EstudianteView,
    EstudianteTablaViewVue,
    LibroTablaView,
    PreguntaView,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
