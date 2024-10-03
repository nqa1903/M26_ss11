<template>
    <div>
        Component Mounted
    </div>
</template>

<script setup>
import { onBeforeMount, onMounted } from 'vue';

    onBeforeMount(()=>{
        console.log("Component bắt đầu mount");
    })
    onMounted(()=>{
        console.log("Component được mounted");
    })
</script>

<style scoped>

</style>