<script setup>
import { defineProps } from "vue";
const { status } = defineProps(["status"]);
</script>
<template>
  <header>
    <h1>Question {{ status }}</h1>
    <div class="bar">
      <div class="completion"></div>
    </div>
  </header>
</template>

<style scoped>
header {
  margin-top: 20px;
}

header h1 {
  font-family: Arial, Helvetica, sans-serif;
}

.bar {
  width: 300px;
  height: 50px;
  border: 3 px solid bisque;
}
.completion {
  height: 100%;
  width: 0%;
  background-color: bisque;
}
</style>
