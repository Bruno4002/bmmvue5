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
 const rawHtml = '<span style="color: red">Este é um texto em vermelho</span>'

 const numero = 1
    const ok = true
    const mensagem = 'programar'

    const mensagem2 = 'programar'

function inverter(texto) {
    return texto.split('').reverse().join('')
}
</script>

<template>
  <button @click="incrementar">+FLA</button>
  <button @click="decrementar">MENGO-</button>
  <button @click="resetar">MAIORC</button>
  <p>Valor do contador: {{ contador }}</p>
  <p>Usando interpolação de textos: {{rawHtml}}</p>
    <p>Usando v-html: <span v-html="rawHtml"></span></p>
    {{ numero + 1 }}
{{ ok ? 'Sim' : 'Não' }}
{{ mensagem.split('').reverse().join('') }}
<p>{{ inverter(mensagem2) }}</p>
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
