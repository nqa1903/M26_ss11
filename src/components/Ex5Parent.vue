<template>
    <div>
        <button @click="handleToggle">Toggle</button>
        <Ex5Child v-if="isShow"></Ex5Child>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import Ex5Child from './Ex5Child.vue';
const isShow = ref(true);
const handleToggle = () =>{
    return isShow.value = !isShow.value;
}
</script>

<style scoped>

</style>