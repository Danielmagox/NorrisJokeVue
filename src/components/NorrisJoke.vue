<template>
  <div>
    Norris Joke
  </div>
</template>

<script>
const URL = "https://api.chucknorris.io/jokes/random";
export default {
  name: "Norris Joke",
  methods: {
    fetchApi() {}
  },
  data() {
    return {
      icon: "",
      text: "",
      date: ""
    };
  }
};
</script>

<style></style>
