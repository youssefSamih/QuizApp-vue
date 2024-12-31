<template>
  <header>
    <h4>Question {{ questionStatus }}</h4>
    <div class="bar">
      <div class="completion"></div>
    </div>
  </header>
</template>

<script setup>
import { defineProps } from 'vue';

const { questionStatus, barPercentage } = defineProps({
  questionStatus: {
    type: String,
    required: true
  },
  barPercentage: {
    type: String,
    required: true
  }
});
</script>

<style scoped>
header {
  margin-top: 20px;
}

header h4 {
  font-size: 30px;
}

.bar {
  width: 300px;
  height: 50px;
  border: 1px solid bisque;
}

.completion {
  height: 100%;
  width: v-bind(barPercentage);
  background-color: bisque;
}
</style>

