<script setup>
import { ref, computed } from 'vue'
const showContent = ref(false)
const textoBotao = computed(
    () => showContent.value ? 'Esconder' : 'Mostrar'

)
const props = defineProps(('title'))


</script>


<template>
    <button @click="showContent = !showContent">{{ textoBotao }}</button>
    <div v-if="showContent" class="expand-box">A
    <h1>{{ props.title }}</h1>
    <p>
        Texto da caixa
    </p>
    </div>
</template>
 
<style scoped> .expand-box {
     height: 100%;
     padding: 20px;
     border: 1px solid black;
     border-radius: 5px;
     box-shadow: 3px 3px 2px 2px crimson;
 }
</style>