<script setup>
const model = defineModel()
defineEmits(['adicionar']);
</script>

<template>
    <section>
        <h2>Adicione uma nova tarefa</h2>
        <input type="text" v-model="model" @keyup.enter="$emit('adicionar')" />
        <button @click="$emit('adicionar')">Adicionar</button>
    </section>
</template>

<style scoped>
input {
    width: 50%;
    padding: 5px;
    margin: 5px 0;
}

button {
    padding: 5px;
    margin: 5px 0;
}
</style>