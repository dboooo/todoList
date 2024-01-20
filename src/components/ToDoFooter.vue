<template>
  <div v-for="item in items">
    {{ item.message }}
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const items = ref([{message: 'foo'}, {message: 'sadsa'}]);

</script>

<style scoped>

</style>