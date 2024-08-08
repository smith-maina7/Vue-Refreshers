<script setup>
import { ref } from 'vue'
const props = defineProps({
  tasks: Array
})

const completed = ref(false)
</script>

<template>
  <div>
    <ul>
      <li v-for="{ id, description } in props.tasks" :key="id">
        {{ id }} {{ description }}
        <label>
          Completed
          <input type="checkbox" v-model="completed" /> // fixing the checking one box issues
        </label>
      </li>
    </ul>
    Hello!!!
  </div>
</template>
