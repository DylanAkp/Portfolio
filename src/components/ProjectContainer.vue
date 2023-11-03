<script>
export default {
  name: 'ProjectContainer',
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
  methods: {
    goToGithub(link) {
      window.open(link);
    },
  },
};
</script>

<template>
  <div class="bubble no-select clickable" @click="goToGithub(project.link)">
    <img :src="project.image" />
    <div class="side">
      <h4>{{ project.name }}</h4>
      <p>{{ project.description }}</p>
    </div>
  </div>
</template>

<style scoped>
.bubble {
  margin-top: 5px;
  display: flex;
  flex-direction: row;
  height: 300px;
  width: 600px;
  padding: 30px;
}

.bubble:hover {
  transform: translate(0, -3px);
  transition-duration: 700ms;
  background-color: #d8d8d9;
}

.bubble:not(:hover) {
  transform: translate(0, 3px);
  transition-duration: 700ms;
}

p {
  opacity: 0.8;
  text-wrap: wrap;
  font-size: large;
}

img {
  width: 120px;
  height: 120px;
  border-radius: 15px;
  margin-right: 20px;
}

.side {
  display: flex;
  flex-direction: column;
}
</style>
