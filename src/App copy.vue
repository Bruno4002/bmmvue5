<script setup>
import {ref} from 'vue'
const contador = ref(10)
 function incrementar() {
  contador.value++
 }
 function decrementar() {
  if(contador.value > 0)
  contador.value--
 }
 function resetar() {
  contador.value = 0
 }

</script>

<template>
  <button @click="incrementar">+FLA</button>
  <button @click="decrementar">MENGO-</button>
  <button @click="resetar">MAIORC</button>
  <p>Valor do contador: {{ contador }}</p>
</template>

<style scoped>
button {
  width:200px;
  height: 200px;
  background-image:linear-gradient(black,red,black,red,black,red,black);
  color: black;
  border-radius: 45%;
  font-size: 50px;
  border: none;
  margin-left: 20px;
  margin-bottom: 20px;
}

</style>
