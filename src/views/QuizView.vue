<script setup>
import Question from "../components/Question.vue";
import Option from "../components/Option.vue";
import Header from "../components/Header.vue";
import { useRoute } from "vue-router";

import { ref, computed } from "vue";
import quizes from "../data/quizdata.json";
const route = useRoute();
const quizId = Number(route.params.id);

const currentQuestion = ref(1);
const quiz = quizes.find((q) => q.id === quizId);

const status = computed(() => {
  return `${currentQuestion.value}/${quiz.questions.length}`;
});
</script>

<template>
  <div>
    <Header :status="status" />
    <Question :question="quiz.questions[currentQuestion]" />
    <Option :question="quiz.questions[currentQuestion]" />
    <button @click="currentQuestion++">Next question</button>
  </div>
</template>

<style scoped></style>
