<template>
    <div>
        <p>Giá trị của age : {{ ageParent }}</p>
        <button @click="handleIncrease">Increase age</button>
        <Ex4Child :ageChild="ageParent"></Ex4Child>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    import Ex4Child from './Ex4Child.vue';

    const ageParent = ref(0);
    const handleIncrease = () =>{
        return ageParent.value++;
    }

</script>

<style scoped>

</style>