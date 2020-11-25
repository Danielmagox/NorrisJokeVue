<template>
  <div class="container">
    <img :src="icon" alt="Chuck" />
    <div>
      <p>{{ text }}</p>
      <span>{{ date }}</span>
    </div>
  </div>
</template>

<script>
const URL = "https://api.chucknorris.io/jokes/random";
export default {
  name: "Norris Joke",
  created() {
    //when component is created fetchApi is executed
    this.fetchApi();
  },
  methods: {
    fetchApi() {
      fetch(URL)
        .then(res => res.json())
        .then(data => {
          this.icon = data.icon_url;
          this.text = data.value;
          this.date = data.updated_at;
        });
    }
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
