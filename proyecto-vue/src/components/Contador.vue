<template> <!--codigo HTML-->
  <h1>Bienvenido a QM Manager</h1>
  <p>{{ contador }}</p>
  <button @click="incrementar">Incrementar</button>
  <button @click="decrementar">Incrementar</button>
</template>



<script setup>//logica de java script
import { ref } from 'vue';
const contador= ref(0);
const incrementar = () => {contador.value++}
const decrementar = () => {contador.value--}
</script>



<style scoped>/*codigo CSS*/
p{color: blue;}
</style>
