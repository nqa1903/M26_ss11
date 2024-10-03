<template>
    <div>
        <p>Component Con</p>
    </div>
</template>

<script setup>
    import { onBeforeUnmount, onUnmounted } from 'vue';
    onBeforeUnmount(()=>{
        alert("Component is about to be unmounted");
    })
    onUnmounted(()=>{
        alert("Component has been unmounted");
    })
</script>

<style scoped>

</style>