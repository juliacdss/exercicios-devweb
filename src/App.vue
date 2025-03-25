<script setup>
import { ref } from 'vue'

const contador = ref(0)

function incrementar() {
  contador.value++
}

function decrementar() {
  if (contador.value > 0) {
    contador.value--
  } 
}

function reiniciar() {
  contador.value = 0
}
</script>

<template>
  <h1>Exercício contador - 2INFO1</h1>
  <p>Valor do contador: {{ contador }}</p>
  <button v-on:click="incrementar">+</button>
  <button @click="decrementar">-</button>
  <button @click="reiniciar">Reiniciar</button>
</template>

<style scoped>

</style>
