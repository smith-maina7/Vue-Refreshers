<script setup>
const props = defineProps({
  counter: Function,
  number: Number,
  deduction: Function,
  error: String
})
</script>
<template>
  <div>Hello World!</div>
  <button @click="props.counter">+</button>
  <div>{{ props.number }}</div>
  <button @click="props.deduction">-</button>
  <div>{{ props.error }}</div>
</template>
<style scoped></style>
