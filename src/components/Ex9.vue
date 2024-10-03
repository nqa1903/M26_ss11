<template>
  <div>
    <p>Giá trị của Count: {{ count }}</p>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";

const count = ref(0);

let intervalId;

const incrementCount = () => {
  count.value++;
};

onMounted(() => {
  intervalId = setInterval(incrementCount, 1000);
});

onBeforeUnmount(() => {
  clearInterval(intervalId);
});
</script>

<style scoped></style>
