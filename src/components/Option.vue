<script setup>
import { defineProps } from "vue";
const { question } = defineProps(["question"]);
</script>

<template>
  <div class="options-container">
    <div v-for="option in question.options" :key="option.id" class="option">
      <p class="option-label">{{ option.label }}</p>
      <div class="option-value">
        <p>{{ option.text }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.option {
  display: flex;
  cursor: pointer;
  font-family: Arial, Helvetica, sans-serif;
  align-items: center;
}

.option-label {
  background-color: bisque;
  width: 50px;
  height: 50px;
  font-size: 30px;
  font-family: Arial, Helvetica, sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
}

.option-value {
  background-color: rgb(244, 239, 239);
  width: 100%;
  font-size: 30px;
  height: 50px;
  display: flex;
  align-items: center;
  padding-left: 15px;
}
</style>
