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
const produto = reactive({
  nome: '',
  preco: 0,
  quantidade: 0,
  categoria: [],
})

</script>
<template>

<Formulario/>

</template>
<style scoped>
.container {
  display: flex;
  flex-direction: row;

  gap: 2rem;
  margin-top: 1rem;

}

.formulario,
.resultado {
  width: 50vw;
  min-height: 70vh;
  padding: 20px;
  border-radius: 20px;

}

.formulario {
  background-color: rgb(255, 167, 167);

}

.resultado {
  background-color: rgb(255, 167, 167);
}

.formulario .row {
  width: 80%;
  margin: 1.3rem 0;
  display: grid;
  justify-content: 1fr 3fr;
}

.formulario .items-checkbox {
  display: grid;
  grid-template-columns: auto 1fr;
  align-items: center;
}

fieldset {
  border-image-repeat: 10px;
  background-color: rgb(255, 255, 255);

}

span {
  text-align: left;
}

button {
  background-color: deeppink;

}
</style>
