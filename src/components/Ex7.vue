<template>
    <div>
        <label for="title">Nhập tiêu đề cho web:</label>
        <input type="text" v-model="inputValue">
    </div>
</template>

<script setup>
import { onMounted, ref, watch } from 'vue';

const inputValue = ref("");

onMounted(() => {
    document.title = "Ban đầu";
});

watch(inputValue, (newValue) => {
    document.title = newValue || "Ban đầu"; 
});
</script>

<style scoped>

</style>
