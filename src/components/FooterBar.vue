<template>
  <footer class="footer">
    <img src="/ylg.png" alt="YearLog Logo" class="footer-logo" />
    <span>© {{ year }}</span>
  </footer>
</template>

<script setup>
import { ref, onMounted } from 'vue'
const year = ref(new Date().getFullYear())
</script>

<style scoped>
.footer {
  background-color: white;
  border-top: 1px solid #eee;
  padding: 12px 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 12px;
  color: #666;
}
.footer-logo {
  height: 60px;
  opacity: 0.6;
}
</style>
