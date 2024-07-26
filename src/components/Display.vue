<script setup>
defineProps(['produto'])
</script>
<template>
   <div class="resultado">
        <h2>Dados do produt</h2>
        <p>Nome:{{ produto.nome }}</p>
        <p>data de nascimento: {{ produto.data }}</p>
        <p>cidade: {{ produto.cidade }}</p>
        <p>senha : {{ produto.senha }}</p>
        <p> confime sua senha: {{ produto.confirmaçãosenha }}</p>
        <p> estado: {{ produto.estado }}</p>
        <p>email:{{ produto.email }}</p>
        <p>linguagem escolhida:{{ produto.categoria }}</p>
        <p>bigrafia : {{ produto.biografia }}</p>
        <p> hobbies : {{ produto.hobbies }}
        </p>
        <span style='font-size:100px;'>&#127800;</span>
      </div>
</template>
<style scoped>
.resultado{
  width: 500px;
  height: 500px;
  padding: 20px;
  border-radius: 20px;
  background-color: rgb(255, 167, 167);
  margin: 10px;
}

</style>