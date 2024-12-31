<template>
  <div class="results">
    <h1>Your got Results...</h1>
    <p>{{ numberOfCorrectAnswers }} / {{ quizQuestionLength }}</p>
    <RouterLink to="/">Go Back</RouterLink>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';
import { RouterLink } from 'vue-router';

const { quizQuestionLength, numberOfCorrectAnswers } = defineProps({
  quizQuestionLength: {
    type: Number,
    required: true
  },
  numberOfCorrectAnswers: {
    type: Number,
    required: true
  }
});
</script>

<style scoped>
.results {
  text-align: center;
  padding: 100px 0;
}

p {
  font-size: 25px;
}

h1 {
  font-size: 80px;
}
</style>
