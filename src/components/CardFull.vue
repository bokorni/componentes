<script setup>

</script>
<template>
    <div class="card">
        <div class="header">
            <slot name="header"></slot>
        </div>

        <slot>Corpo padrão do card</slot>
        <div v-if="$slots.footer" class="footer">
            <slot name="footer"></slot>
        </div>
    </div>
</template>

<style scoped>
.card {
    height: 200px;
    width: 400px;
    box-shadow: 2px 2px 3px 3px black;
    border-radius: 20px;
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.header {
    background-color: greenyellow;
    height: 60px;
    border-radius: 20px;
    width: 100%;
}

.footer {
    background-color: greenyellow;
    height: 60px;
    border-radius: 20px;
    width: 100%;

}
</style>