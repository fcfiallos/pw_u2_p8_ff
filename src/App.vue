<template>
  <!--<HolaMundoView/>-->
  <!--<ContadorView/>-->
  <EstudianteView />
</template>

<script>
import HolaMundoView from "@/views/HolaMundoView.vue";
import ContadorView from "@/views/ContadorView.vue";
import EstudianteView from "@/views/EstudianteView.vue";

export default {
  name: "App",
  components: {
    HolaMundoView,
    ContadorView,
    EstudianteView,
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