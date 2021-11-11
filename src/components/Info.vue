<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
  <div class="container" >
    <div class="info">
      <p class="titulo" style="font-size: 48.83px; font-weight: bold;">
        Busca tus películas
      </p>
      <p class="cuerpo" style="font-size: 20px;">
        Lorem ipsum dolor sit amet, consectetur adipiscing<br>
        elit. Donec purus diam, sagittis porttitor tincidunt<br>
        ac, rutrum quis risus. Nulla in arcu convallis, lacinia<br>
        urpis id, auctor lectus.
      </p>
    </div>
    <button class="vamos">Vamos!</button>
  </div>
</template>

<style scoped>
button{
  position: absolute;
  height: 50px;
  width: 180px;
  background-color: #256CF5;
  color: white;
  border: 0px;
  margin-left: 25%;
  margin-top: 25%;
}

.container{
  position: relative;
  background-image: url("../assets/claketa.jpg") ;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 100%;
  height: 100vh;
  width: 100%;
}

p{
  color: white;
  text-align: right;
}

.info{
  position: absolute;
  margin-left: 60%;
  margin-top: 5%;
}
</style>
