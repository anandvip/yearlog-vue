<template>
  <header class="header">
    <span class="divider">|</span>
    <span class="date-info">Day 208</span>
    <span class="date-info">157 days left</span>
    <span class="date-info">Week 31</span>
    <span class="date-info">{{ currentDate }}</span>
  </header>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const currentDate = ref('')

onMounted(() => {
  const now = new Date()
  currentDate.value = now.toLocaleDateString()
})
</script>

<style scoped>
.header {
  padding: 20px 20px 20px 30px;
  background-color: white;
  border-bottom: 1px solid #eee;
  display: flex;
  align-items: center;
  gap: 20px;
  flex-wrap: wrap;
}
.divider {
  color: red;
  font-weight: bold;
  margin-left: -10px;
}
.date-info {
  font-size: 14px;
  color: #333;
}
</style>
