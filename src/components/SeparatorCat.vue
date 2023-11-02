<template>
  <div>
    <div class="title">{{ name }}</div>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true, // Si la chaîne est requise
    },
  },
};
</script>

<style scoped>
.title {
  width: 100%;
  text-align: center;
  margin-top: 50px;
  margin-bottom: 50px;
  text-align: center;
  font-size: 30px;
}
</style>
