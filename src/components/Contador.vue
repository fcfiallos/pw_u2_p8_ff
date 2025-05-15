<template>
  <div class="contanier">
    <h1>Contador</h1>
    <!--eleemnto html sub exponencial-->
    <p>{{ this.numero }} <sup>2</sup>= {{ calCuadrado }}</p>
    <div>
      <button v-on:click="incrementar()">+1</button>
      <button v-on:click="decrementar()">-1</button>
    </div>
    <!--<p>{{ this.numero }} <sup>2</sup>= {{calCuadrado}}</p>
    <p>{{ this.numero }} <sup>2</sup>= {{calCuadrado}}</p>
    <p>{{ this.numero }} <sup>2</sup>= {{calCuadrado}}</p>
    <p>{{ this.numero }} <sup>2</sup>= {{calCuadrado}}</p>
    <p>{{ numero + 1 }}</p>
    <p>{{ texto }}</p>
    <p>{{ activo }}</p>
    <p>{{ usuario.edad }}</p>
    <p>{{ arreglo }}</p>
    1+1
    {{ 1 + 1 }}
    true?'Es verdadero':'Es falso'
    {{ false ? "Es verdadero" : "Es falso" }}-->
  </div>
</template>

<script>
export default {
  /**esas opciones openvia son como metodos*/
  data() {
    /*propiedades reactivas */
    return {
      numero: 5,
      texto: "Fátima Fiallos",
      activo: true,
      usuario: {
        nombre: "Fátima",
        edad: "22",
        genero: "F",
      },
      arreglo: ["Azul", "Amarrillo"],
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
      console.log("Entro propiedad computada");
      return this.numero * this.numero;
    },
  },
};
</script>

<style>
.contanier {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>