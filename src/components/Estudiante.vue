<template>
  <div class="container">
    <label for="id_nombre">Nombre:</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
    <label for="id_apellido">Apellido:</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />
    <label for="id_cedula">Cedula:</label>
    <input v-model="nuevoCedula" id="id_cedula" type="text" />
    <label for="id_telefono">Tel. Celular:</label>
    <input v-model="nuevoTelefono" id="id_telefono" type="text" />
    <label for="id_direccion">Dirección:</label>
    <input v-model="nuevoDireccion" id="id_direccion" type="text" />
    <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
    {{ nuevoNombre }}
    <ul>
      <!--El error es porque pide un identificador (ej.: cedula)-->
      <li v-for="{ nombre, apellido, cedula, telefono, direccion } in lista" :key="nombre">
        Nombre: {{ nombre }} - Apellido: {{ apellido }} - Cedula: {{ cedula }} -
        Telefono: {{ telefono }} - Direccion: {{ direccion }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "",
      nuevoApellido: "",
      nuevoCedula: "",
      nuevoTelefono: "",
      nuevoDireccion: "",
      lista: [
        {
          nombre: "Fátima",
          apellido: "Fiallos",
          cedula: "123456789",
          telefono: "0987654321",
          direccion: "Calle 123",
        },
        {
          nombre: "Daniel",
          apellido: "Fiallos",
          cedula: "087654321",
          telefono: "0987654321",
          direccion: "Calle 456",
        },
        {
          nombre: "Pedro",
          apellido: "Teran",
          cedula: "123456789",
          telefono: "0987654321",
          direccion: "Calle 789",
        },
        {
          nombre: "Andrea",
          apellido: "Fiallos",
          cedula: "123456789",
          telefono: "0987654321",
          direccion: "Calle 101",
        },
        {
          nombre: "Carlos",
          apellido: "Castillo",
          cedula: "123456789",
          telefono: "0987654321",
          direccion: "Calle 102",
        },
        {
          nombre: "Ana",
          apellido: "Tobar",
          cedula: "123456789",
          telefono: "0987654321",
          direccion: "Calle 103",
        },
        {
          nombre: "Viviana",
          apellido: "Lopez",
          cedula: "123456789",
          telefono: "0987654321",
          direccion: "Calle 104",
        },
      ],
    };
  },
  methods: {
    agregarEstudiante() {
      /**this.lista.unshift(nuevo);agrega al inicio */
      this.lista.push({
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
        cedula: this.nuevoCedula,
        telefono: this.nuevoTelefono,
        direccion: this.nuevoDireccion,
      }); //agrega al final
    },
  },
};
</script>

<style>
</style>