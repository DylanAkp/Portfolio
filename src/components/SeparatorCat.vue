<template>
  <div>
    <h3 class="title">{{ name }}</h3>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
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
  font-weight: 800;
}
</style>
