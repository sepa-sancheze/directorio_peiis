<script>
import { ref } from 'vue'
import { axios } from 'axios';

export default {
  data() {
    return {
      posts: [],
      info: null
    };
  },
  mounted() {
    fetch('http://localhost:5000/actor')
    .then(response => response.json())
    .then(data => this.info = data);
  }
};

</script>

<template>

  <div class="container">
    <div v-for="post in info" v-bind:key="post.id" class="card">
      <h2>{{ post.name }}</h2>
      <p>{{ post.bio }}</p>
      <p>{{ post.born_date }}</p>
    </div>
    <button><router-link style="text-decoration: none; color: inherit;" to="/">Regresar</router-link></button>
  </div>
</template>

<style scoped>
.container{
  position: relative;
  background-image: linear-gradient(rgba(255,255,255,0.5), rgba(255,255,255,0.5)), url("../assets/cintas.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: 100%;
  height: 100vh;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}

.card{
  position: relative;
  margin-left: 5%;
  margin-right: 5%;
  margin-top: 5%;
  height: 25%;
  width: 20%;
  background-color: gray;
}

button{
  position: relative;
  height: 50px;
  width: 10%;
  background-color: #256CF5;
  color: white;
  border: 0px;
  margin-left: 40%;
  margin-top: 0%;
}

</style>
