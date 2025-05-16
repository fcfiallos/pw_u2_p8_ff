<template>
  <div class="container">
    <label for="id_nombre">Nombre:</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
    <label for="id_apellido">Nombre:</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />
    <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
    {{ nuevoNombre }}
    <ul>
      <!--El error es porque pide un identificador (ej.: cedula)-->
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
      nuevoApellido: "nuevo",
      lista: [
        {
          nombre: "Fátima",
          apellido: "Fiallos",
        },
        {
          nombre: "Daniel",
          apellido: "Fiallos",
        },
        {
          nombre: "Pedro",
          apellido: "Teran",
        },
        {
          nombre: "Andrea",
          apellido: "Fiallos",
        },
        {
          nombre: "Carlos",
          apellido: "Castillo",
        },
        {
          nombre: "Ana",
          apellido: "Tobar",
        },
        {
          nombre: "Viviana",
          apellido: "Lopez",
        },
      ],
    };
  },
  methods:{
    agregarEstudiante(){
        const nuevo = {
            nombre: this.nuevoNombre,
            apellido: this.nuevoApellido,
        }
        /**this.lista.unshift(nuevo);agrega al inicio */
        this.lista.push(nuevo); //agrega al final
    }
  }
};
</script>

<style>
</style>