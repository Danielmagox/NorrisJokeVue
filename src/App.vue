<template>
  <div>
    <NorrisJoke type="chuck" />
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
