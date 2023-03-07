<script>
export default{
data() {
  return{
    contador: 0
  }
},
methods: {
  Incrementar(){
    this.contador++
  } ,
  decrementar(){
    if(this.contador > 0){
    this.contador--
    }
  },
 resetar(){
  this.contador = 0
 }
}
}

 

</script>

<template>
  <button @click="Incrementar">+FLA</button>
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
