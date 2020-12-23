<template>
  <div>
    <h1>VueJS</h1>
    <Car />
    <CarOptions />
    <hr />
    <CarComposition />
    <CarProps :power="power" :upPower="upPower" @downPower="downPower" />
  </div>
</template>

<script>
  import Car from "./components/Car";
  import CarComposition from "./components/CarComposition";
  import CarOptions from "./components/CarOptions";
  import CarProps from "./components/CarProps";
  import { ref } from "vue";
  export default {
    components: {
      Car,
      CarComposition,
      CarOptions,
      CarProps,
    },
    setup() {
      let power = ref(30);
      const upPower = () => {
        // console.log("aumentar power...");
        power.value++;
      };
      const downPower = () => {
        // console.log("disminuir power...");
        power.value--;
      };
      return {
        power,
        upPower,
        downPower,
      };
    },
  };
</script>

<style></style>
