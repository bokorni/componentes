<script setup>
import { ref, computed } from 'vue'
const showContent = ref(false)
const textoBotao = computed(
    () => showContent.value ? 'Esconder' : 'Mostrar'

)
const props = defineProps({
    title: {
        type: String,
        required: true,
    },
    content: {
        type: String,
        default: 'Conteúdo da caixa de expansão',
    },
    qtde: {
        type: Number,
        default: 1,

    },
});


</script>


<template>
    <button @click="showContent = !showContent">{{ textoBotao }}</button>
    <div v-if="showContent" class="expand-box">
        <h1>{{ props.title }}</h1>
        <p>
            {{ props.content }}
        </p>
        <p>
            Quantidade: {{ props.qtde }}
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