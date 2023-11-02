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
@font-face {
  font-family: 'Lunasima', sans-serif;
  src: url('https://fonts.googleapis.com/css2?family=Lunasima:wght@700&family=Nunito+Sans:opsz,wght@6..12,300&display=swap');
}

div {
  font-family: 'Lunasima', sans-serif;
}
</style>
