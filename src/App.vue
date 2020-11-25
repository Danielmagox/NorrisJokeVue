<template>
  <div>
    <NorrisJoke />
  </div>
</template>

<script>
import NorrisJoke from "./components/NorrisJoke";

export default {
  name: "App",
  components: { NorrisJoke },
  data() {
    return {
      title: "hola"
    };
  }
};
</script>

<style></style>
