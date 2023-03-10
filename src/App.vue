<script setup>
import {ref} from 'vue'
const nome = 'Bruno'
    const idade = 16
    function inverter1(texto) {
        return texto.split('').reverse().join('')
    }

    function inverter(texto) {
        return texto.split('').reverse().join('').toUpperCase()
    }

    function saudacao() {
        return `Olá, ${nome}!`
    }

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
  <div class="info">
        <h1>Exemplo 1 - Mostrando informações na tela</h1>
        <p>Nome: {{ nome }} </p>
        <p>Idade: {{ idade }}  anos</p>
        <hr />
        <p>Para completar 50 anos faltam: {{ 50 - idade }}  anos</p>
        <p>O nome tem {{ nome.length }}  caracteres</p>
        <p>O nome invertido é: {{ inverter1(nome) }} </p>
        <p>O nome invertido em maiusculo é: {{ inverter(nome) }} </p>
        <hr />
        <p> Exemplo de saudação usando função</p>
        <p> {{ saudacao() }}  </p>
    </div>
  <button @click="incrementar">+FLA</button>
  <button @click="decrementar">MENGO-</button>
  <button @click="resetar">MAIORC</button>
  <p>Valor do contador: {{ contador }}</p>
  <p v-if="contador > 10" class="maior">Contador é maior que 10</p>
  <p v-else class="menor">Contador é menor que 10</p>
  
</template>

<style scoped>
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
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
.maior{
  background-color: green;
}
.menor{
  background-color: red;
}
</style>