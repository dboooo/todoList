<script setup lang="ts">
import ToDoTop from './components/ToDoTop.vue'
import ToDoFooter from "./components/ToDoFooter.vue";
</script>

<template>
  <h1>To Do List</h1>
  <ToDoTop />
  <ToDoFooter/>

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
