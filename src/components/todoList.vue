<script setup>
import { ref } from 'vue'
import todoListForm from '../components/todoListForm.vue'

const tasks = ref([
  { id: 1, description: 'Take Kennah to school' },
  { id: 2, description: 'Do a refresher course on software development' },
  { id: 3, description: 'Catch up on your choas' },
  { id: 4, description: 'Go to Tatu City for work' }
])
</script>

<template>
  <div class="list">
    <todoListForm :tasks="tasks" />
  </div>
</template>
