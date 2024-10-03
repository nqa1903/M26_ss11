<template>
    <div>
        <p>Current Company : {{ currentCompany }}</p>
        <p>Giá trị của age : {{ age }}</p>
        <button @click="handleRandom(1,10)">Random</button>
    </div>
</template>

<script setup>
    import { computed, ref } from 'vue';

    const age = ref(1);
    const companies = ref(["Rikkei Academy", "Rikkei Education", "Rikkei Fukuoka"]);
    const currentCompany = computed(()=>{
        const index = (age.value - 1) % companies.value.length;
        return companies.value[index];
    })
    const handleRandom = (min , max) =>{
        const minNumber = Math.ceil(min);
        const maxNumber = Math.floor(max);
        return age.value = Math.floor(Math.random() * (maxNumber - minNumber + 1) + minNumber);
    }

</script>

<style scoped>

</style>