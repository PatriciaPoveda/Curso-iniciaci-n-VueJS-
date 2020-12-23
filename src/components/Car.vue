<template>
    <h2>Coche</h2>
    <p>Modelo: {{ brand }}</p>
    <p>Color: {{ colors[1] }}</p>
    <p>
      Color:
      <ul>
       <li v-for="(color, i) in colors" :key="i">{{ i }}: {{ color }}</li>
      </ul>
    </p>
    <p>Potencias:
      <ul>
       <template v-for="(power, i) in powers" :key="i">
         <li v-if="power<280">Urbana: {{power}}</li>
         <li v-else-if="power === 280">Híbrido {{power}}</li>
         <li v-else>Carrera: {{power}}</li>
        <!-- Este if es una sentencia diferente y por eso se renderiza 2 veces  -->
         <li v-if="power===540">Super: {{power}}</li>
       </template>
      </ul>
    </p>

    <p>Precio: {{ price }} €</p>
    {{ mensaje.title }} - {{ mensaje.text }}

</template>

<script>
export default {
  //VARIABLES

  /*VUE 2: Options API*/

  // data() {
  //   return {
  //     brand: "audi",
  //     color: ["Azul", "Rojo", "Verde"],
  //     price: 38000,
  //     mensaje: {
  //       title: "Hola mundo",
  //       text: "Adios",
  //     },
  //   };
  // },

  /*VUE 3: Composition API*/

  setup() {
    const brand = "Audi";
    const colors = ["Azul", "Rojo", "Verde", "negro"];
    const price = 38000;
    const powers=[60, 80, 120, 160, 200, 280, 300, 390, 540,]
    const mensaje = {
      title: "Hola mundo",
      text: "Adios",
    };
    return {
      brand,
      colors,
      price,
      powers,
      mensaje,
    };
  },
};
</script>

<style>
</style>