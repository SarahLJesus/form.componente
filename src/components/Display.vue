<script setup>
import { defineProps } from 'vue';


</script>
<template>
   <div v-if="mostrarresultado" class="resultado">
        <h2>Dados do produto</h2>
        <p>Nome:{{ produto.nome }}</p>
        <p>data de nascimento: {{ produto.data }}</p>
        <p>cidade: {{ produto.cidade }}</p>
        <p>senha : {{ senha }}</p>
        <p> confime sua senha: {{ confirmaçãosenha }}</p>
        <p> estado: {{ produto.estado }}</p>
        <p>email:{{ produto.email }}</p>
        <p>linguagem escolhida:{{ produto.categoria }}</p>
        <p>bigrafia : {{ produto.biografia }}</p>
        <p> hobbies : {{ produto.hobbies }}
        </p>
        <span style='font-size:100px;'>&#127800;</span>
      </div>
</template>
<script scoped>
</script>