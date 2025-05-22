<template>
  <div class="container">
    <img
      src="https://yesno.wtf/assets/no/19-2062f4c91189b1f88a9e809c10a5b0f0.gif"
      alt="No se pudo cargar"
    />
    <div class="container-2"></div>
    <div class="pregunta-container">
      <input v-model="pregunta"
        type="text"
        placeholder="Hazme una pregunta"
      /><!--una idea de que se debe poner en el input-->
      <p>Recuerda terminar con un signo de pregunta (?)</p>
      <h2>{{ pregunta }}</h2>
      <h1>{{respuesta}}</h1>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            pregunta: null, //pregunta 
            respuesta: null, //api
        }
    },
    watch:{ //permite observar los cambio de mi propiedad reactiva 
        pregunta(value, oldValue){
            console.log("valor actual: "+ value);
            console.log("valor anterior: "+ oldValue);
        }
    }
};
</script>

<style scoped>
.container-2,
img {
  height: 100vh; /*El anho y alto */
  left: 0px;
  max-width: 100%;
  max-height: 100%;
  position: fixed; /**no respeta la posicion y pasa a ser una marca de agua y el resto de elemmento no tiene efecto */
  top: 0px;
  width: 100vw; /**todo el ancho y largo  */
}

.container-2 {
  background-color: rgba(0, 0, 0, 0.5);
}

.pregunta-container {
  position: relative; /**indpendiente a los elementos que existan el la pagina web los va poner en primero posicion  */
}

input {
  width: 250px;
  padding: 10px 15px;
  border-radius: 5px;
  border: none;
  margin: 70px;
}

input:focus {
  outline: none;
}
p {
  color: white;
  font-size: 25px;
}
h1,
h2 {
  color: white;
}
h2 {
  margin-top: 160px;
}
</style>