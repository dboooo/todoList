<template>
  <div>
    <li>
      <a> {{ item }} </a>
      <input type="checkbox" v-model="check">
    </li>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
defineProps<
{
  item: String
}
>()

const check = ref(false)
</script>

<style scoped>

</style>