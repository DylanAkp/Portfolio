<template>
  <router-view />
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
});
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Sofia+Sans:wght@300;400&display=swap');


div, body {
  font-family: 'Sofia Sans', sans-serif;
  font-size: large
}
</style>
