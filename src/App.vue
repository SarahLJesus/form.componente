<script setup>
import { reactive, ref } from 'vue'
import Formulario from './components/Formulario.vue';
import Display from './components/Display.vue';

const titulo = ref('Bem vindo')

const mostrarresultado = ref(false)
const mostrasr = [{
  id: 1,
  nome: 'eletronicos'
},
{
  id: 2,
  nome: 'vestuario'

},]
const produto = ref({
  nome: 'dafdsf',
  preco: 0,
  quantidade: 0,
  categoria: [],
})

function salvar(item) {
  produto.value = item
}

</script>
<template>

<Formulario @salvar="salvar"/>
<Display :produto="produto"/>

</template>
<style scoped>

</style>
