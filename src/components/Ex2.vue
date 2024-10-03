<template>
    <div>
        <p>Giá trị Counter {{ count }}</p>
        <button @click="handleIncrease">Increase</button>
    </div>
</template>

<script setup>
    import { onBeforeUpdate, onUpdated, ref } from 'vue';

    const count = ref(0);
    const handleIncrease = () =>{
        return count.value++; 
    }
    onBeforeUpdate(()=>{
        console.log("Dữ liệu đang được thay đổi");
    })
    onUpdated(()=>{
        console.log("Dữ liệu đã được thay đổi");
    })
</script>

<style scoped>

</style>