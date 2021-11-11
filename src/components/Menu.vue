<script setup>
import { ref } from 'vue'



const count = ref(0)
</script>

<template>
  <div class="container" >
    <div class="menus">
      <router-link style="text-decoration: none; color: inherit;" to="/search"><div class="elementos" id="actores"><p>Actores</p></div></router-link>
      <div class="elementos" id="peliculas"><p>Películas</p></div>
      <div class="elementos" id="elencos"><p>Elencos</p></div>
    </div>
    
  </div>
</template>

<style scoped>
.container{
  position: relative;
  background-color: white;
  height: 100vh;
  width: 100%;
}

.menus{
  position: relative;
}

.elementos{
  position: relative;
  margin-left: 10%;
  margin-top: 10vh;
  height: 80vh;
  width: 20%;
  background-color: tomato;
  float: left;
}

p{
  font-size: 24px;
  font-weight: bold;
  text-align: center;
  margin-top: 70vh;
}

#actores{
  background-image: linear-gradient(rgba(255,255,255,0), rgba(255,255,255,1)),url("../assets/actores.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

#actores:hover{
  background-image: linear-gradient(rgba(255,255,255,0), rgba(255,255,255,0)),url("../assets/actores.jpg");
  cursor: pointer;
}

#peliculas{
  background-image: linear-gradient(rgba(255,255,255,0), rgba(255,255,255,1)),url("../assets/movies.jpg");
  background-repeat: no-repeat;
  background-position: top;
  background-size: 150%;
}

#peliculas:hover{
  background-image: linear-gradient(rgba(255,255,255,0), rgba(255,255,255,0)),url("../assets/movies.jpg");
  cursor: pointer;
}

#elencos{
  background-image: linear-gradient(rgba(255,255,255,0), rgba(255,255,255,1)),url("../assets/cast.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

#elencos:hover{
  background-image: linear-gradient(rgba(255,255,255,0), rgba(255,255,255,0)),url("../assets/cast.jpg");
  cursor: pointer;
}

</style>
