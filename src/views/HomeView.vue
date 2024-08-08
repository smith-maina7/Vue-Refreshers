<script setup>
import { ref } from 'vue'
import AdditionCounter from '@/components/AdditionCounter.vue'
import todoList from '../components/todoList.vue'

const figure = ref(0)
const errorMessage = ref('')

const addition = () => {
  figure.value++
  errorMessage.value = ''
}
const subtraction = () => {
  if (figure.value > 0) {
    figure.value--
    errorMessage.value = ''
  } else {
    errorMessage.value = 'Value cannot be a negative number'
  }
}
</script>

<template>
  <main>
    <AdditionCounter
      :counter="addition"
      :number="figure"
      :deduction="subtraction"
      :error="errorMessage"
    />
    <todoList />
  </main>
</template>
