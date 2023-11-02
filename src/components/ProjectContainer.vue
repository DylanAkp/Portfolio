<script setup>
import { defineProps } from 'vue';

defineProps({
  project: {
    type: Object,
    required: true,
  },
  methods: {
    goToGithub() {
      window.open(project.link);
    },
  },
});
</script>

<template>
  <div class="bubble no-select clickable" @click="goToGithub">
    <img :src="project.image" />
    <div class="side">
      <h4>{{ project.name }}</h4>
      <p>{{ project.description }}</p>
    </div>
  </div>
</template>

<style scoped>
.bubble {
  display: flex;
  flex-direction: row;
  width: fit-content;
  max-width: 600px;
  padding: 30px;
}

p {
  opacity: 0.8;
  text-wrap: wrap;
}

img {
  width: 100px;
  height: 100px;
  border-radius: 15px;
  margin-right: 20px;
}

.side {
  display: flex;
  flex-direction: column;
}
</style>
