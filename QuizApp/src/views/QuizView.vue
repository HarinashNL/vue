<script setup>
import Question from "../components/Question.vue";
import QuizHeader from "../components/QuizHeader.vue";
import { useRoute } from "vue-router";
import { ref, watch } from "vue";
import quizes from "../data/quizes.json";

const route = useRoute();
const quizId = parseInt(route.params.id);
const quiz = quizes.find((q) => q.id === quizId);
const currentQuestionIndex = ref(0);

// const questionStatus = `${currentQuestionIndex.value}/${quiz.questions.length}`;
const questionStatus = ref("");

// watch(
//   () => currentQuestionIndex.value,
//   () => {
//     questionStatus.value = `${currentQuestionIndex.value}/${quiz.questions.length}`;
//   }
// );
watch(
  currentQuestionIndex,
  () => {
    questionStatus.value = `${currentQuestionIndex.value + 1}/${
      quiz.questions.length
    }`;
  },

  { immediate: true }
);
</script>

<template>
  <div>
    <QuizHeader :questionStatus="questionStatus" />
    <div><Question :question="quiz.questions[currentQuestionIndex]" /></div>
    <button @click="currentQuestionIndex++">Next Question</button>
  </div>
</template>
