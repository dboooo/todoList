<template>
  <div>
    <input 
    type="text" 
    id="text_input" 
    v-model="state.value"
    @keyup.enter = "handClick"
    >
    <input type="button" value="提交" @click="handClick">
    <ToDoBody 
      v-if="items.length"
      v-for="item in items"
      :key = "item.id"
      :item="item.item"
    />
  </div>
</template>

<script setup lang="ts">
type Items = Array<
{
  id: number,
  item: String
}>

import { ref } from 'vue'
import ToDoBody from './ToDoBody.vue';

const state = ref({ value: '' })
const items = ref([
] as Items)
const id = ref(0)
console.log(items.value.length);

function handClick () {
  if(state.value.value == '') {
    alert('empty is not allowed')
    return true
  }
items.value.unshift({
id: id.value,
item: state.value.value
})
id.value++
  console.log(state.value);
}
</script>

<style scoped>

</style>