<template>
  <h2>Coche - ApiComposition</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Power: {{ power }}</p>
  <button @click="upPower(20)">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
  import { ref } from "vue";
  export default {
    setup() {
      const brand = "Audi";
      const model = "A4";
      let power = ref(40);
      const upPower = (newPower) => {
        power.value = newPower + power.value;
        // console.log("aumentar " + power.value);
      };
      const downPower = () => {
        power.value--;
        // console.log("disminuir " + power.value);
      };

      return {
        brand,
        model,
        power,
        upPower,
        downPower,
      };
    },
  };
</script>

<style></style>
