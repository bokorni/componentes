<script setup>
import ExpandBox from './components/ExpandBox.vue';
const title = 'Titulo da caixa de expansão';
const qtde = 2

</script>

<template>
  <expand-box title="Caixa 1" content="Conteúdo Caixa 1" :qtde="qtde" />
  <expand-box title="Caixa 2" content="Conteúdo Caixa 2" />
  <expand-box title="Caixa 3" content="Conteúdo Caixa 3" />
</template>

<style scoped></style>
 