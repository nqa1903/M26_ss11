<template>
    <div>
        <p>Giá trị count = {{ count }}</p>
        <button @click="handleClick">Increase</button>
    </div>
</template>

<script setup>
import { ref, watch } from 'vue';

    const count = ref(0)
    const handleClick = () =>{
        return count.value++;
    }
    watch(count , (newValue) => {
        document.title = `Count : ${newValue}`
    })
</script>

<style scoped>

</style>