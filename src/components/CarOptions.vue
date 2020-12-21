<template>
  <h2>Coche - ApiOptions</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Power: {{ power }}</p>
  <button @click="upPower(1000)">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
  export default {
    data() {
      return {
        brand: "Seat",
        model: "Leon",
        power: 50,
      };
    },
    methods: {
      upPower(newPower) {
        console.log("aumentando potencia --> " + newPower);
      },
      downPower() {
        console.log("disminuyendo");
      },
    },
  };
</script>

<style></style>
