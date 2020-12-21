<template>
  <div>
    <h1>Nuestro primer componente</h1>
    <Car />
    <CarOptions />
    <hr />
    <CarComposition />
  </div>
</template>

<script>
  import Car from "./components/Car";
  import CarComposition from "./components/CarComposition";
  import CarOptions from "./components/CarOptions";
  export default {
    components: {
      Car,
      CarComposition,
      CarOptions,
    },
  };
</script>

<style></style>
