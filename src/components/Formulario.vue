<script setup>
import { ref, reactive } from 'vue';
const emit = defineEmits(['salvar'])
const titulo = ref('Bem vindo')
const produto = reactive({
  nome: '',
  preco: 0,
  quantidade: 0,
  categoria: [],
  senha: '',
  confirmaçãosenha: ''
});
function salvar() {
    emit('salvar', { ...produto })
}
</script>

<template>

  <h1><span style='font-size:60px;'>&#127872;</span>{{ titulo }}</h1>
  <button @click="salvar">resultado</button>
  <div class="container">

    <div class="formulario">
      <h2> formulario </h2>
        <input type="text" v-model="titulo">
        <div class="row">
          <label for="nome">Nome</label>
          <input type="text" v-model="produto.nome">
        </div>

        <div class="row">
          <label for="nome">Email</label>
          <input type="text" v-model="produto.email">
        </div>


        <div class="row">
          <label for="nome">senha</label>
          <input type="text" v-model="produto.senha">
        </div>


        <div class="row">
          <label for="nome">confirme a senha </label>
          <input type="text" v-model="produto.confirmaçãosenha">
        </div>

        <div class="row">
          <label for="nome">data de nascimento</label>
          <input type="date" v-model="produto.data">
        </div>


        <div class="row">
          <label for="quantidade">endereço</label>
          <input type="text" v-model="produto.endereço">
        </div>

        <div class="row">
          <label for="quantidade">cidade</label>
          <input type="text" v-model="produto.cidade">
        </div>


        <div class="row">
          <label for="">estado</label>

          <select v-model="produto.estado">
            <input type="option">
            <option value="Acre">AC</option>
            <option value="Alagoas">AL</option>
            <option value="Amapa">AP</option>
            <option value="Amazona">AM</option>
            <option value="Bahia">BA</option>
            <option value="Ceara">CE</option>
            <option value="Distrito Federal">DF</option>
            <option value="Espirito santo">ES</option>
            <option value=" Goiás">GO</option>
            <option value="Maranhão">MA</option>
            <option value=" Mato Grosso">MT</option>
            <option value=" Mato Grosso do Sul">MS</option>
            <option value=" Minas Gerais">MG</option>
            <option value="Pará">PA</option>
            <option value=" Paraíba ">PB</option>
            <option value="Paraná">PR</option>
            <option value="Pernambuco">PE</option>
            <option value="Piauí">PI</option>
            <option value=" Rio de Janeiro">RJ</option>
            <option value=" Rio Grande do Norte">RN</option>
            <option value="Rio Grande do Sul ">RS</option>
            <option value="Rondônia">RO</option>
            <option value=" Roraima">RR</option>
            <option value=" Santa Catarina ">SC</option>
            <option value=" São Paulo ">SP</option>
            <option value="Sergipe">SE</option>
            <option value=" Tocantins">TO</option>
          </select>
        </div>


        <fieldset>
          <legend>linguagem de programação</legend>
          <div class="items-checkbox">
            <input type="checkbox" value="pyton" v-model="produto.categoria" /> pyton
            <input type="checkbox" value="java" v-model="produto.categoria" /> java
            <input type="checkbox" value="php" v-model="produto.categoria" /> php
          </div>
        </fieldset>


        <div class="row">
          <label for="biografia">biografia</label>
          <input type="text" v-model="produto.biografia">
        </div>

        <div class="row">
          <label for="hoppies">hobbies</label>
          <input type="text" v-model="produto.hobbies">
        </div>


    </div>
  </div>

</template>
<style scoped>
.container {
  display: flex;
  flex-direction: row;
  gap: 2rem;
  margin-top: 1rem;

}

.formulario{
  width: 50vw;
  min-height: 70vh;
  padding: 20px;
  border-radius: 20px;

}

.formulario {
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
  height: 100px;
  width: 90px;
  border-radius: 19px;

}
</style>