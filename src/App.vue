<script setup>
import ExpandBox from './components/ExpandBox.vue';
const title = 'Titulo da caixa de expansão';
const qtde = 2
const caixas= [
    {id: 1, title: 'Caixa 1'},
    {id: 2, title: 'Caixa 2', qtde:777},
    {id: 3, title: 'Caixa 3', content:'Conteudo secret', qtde:888},
    {id: 4, title: 'Caixa 4', content: 'Conteudo incrivel 4', qtde:666}
]
</script>

<template>
  <expand-box title="titulo"/>
  <expand-box v-for="caixa in caixas" :key="caixa.id" v-bind:="caixa" />
  
</template>

<style scoped></style>
 