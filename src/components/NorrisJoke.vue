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

<style>
.container {
  display: inline-flex;
  max-width: 500px;
  border: 1px solid #999;
  padding: 5px;
  padding-right: 20px;
  border-radius: 10px;
  font-family: "Montserrat";
  background: #eee;
}
.container > div {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
img {
  width: 60px;
  height: 60px;
  margin-right: 10px;
}
p {
  margin: 0;
}
span {
  font-family: Arial;
  font-size: 12px;
  color: purple;
}
</style>
