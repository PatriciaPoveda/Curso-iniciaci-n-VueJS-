<template>
  <h2>Pasar Props</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Power: {{ power }}</p>
  <!-- <button @click="testPower">Aumentar</button> -->
  <button @click="upPower">Aumentar</button>
  <button @click="downPowerFn">Disminuir</button>
</template>

<script>
  export default {
    props: {
      power: {
        type: Number,
        default: 60,
      },
      // power: Number,
      upPower: Function,
    },
    emits: ["downPower"],
    setup(props, context) {
      const brand = "Audi";
      const model = "A4";

      // console.log(props.power);
      // console.log(props);

      // const testPower = () => {
      //   props.upPower();
      // };
      const downPowerFn = () => {
        context.emit("downPower");
      };
      return {
        brand,
        model,
        downPowerFn,
        // testPower,
      };
    },
  };
</script>

<style></style>
