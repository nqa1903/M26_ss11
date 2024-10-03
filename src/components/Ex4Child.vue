<template>
    <div>

    </div>
</template>

<script setup>
import { onMounted, watch } from 'vue';

    const props = defineProps(["ageChild"])
    onMounted(()=>{
        console.log("Component con được mounted");
    })
    watch(()=>props.ageChild, (newValue , oldValue) =>{
        if(oldValue != undefined){
            alert("giá trị biến age đã thay đổi")
        }
    })
</script>

<style scoped>

</style>