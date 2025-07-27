<template>
  <div class="entry">
    <div class="entry-title-wrapper">
      <span class="title-bar">|</span>
      <input class="entry-title" v-model="entry.title" />
    </div>
    <textarea class="entry-description" v-model="entry.description" />
    <div class="entry-timestamp">{{ timestamp }}</div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
const props = defineProps({ entry: Object })

const timestamp = computed(() => {
  return new Date(props.entry.timestamp || Date.now()).toLocaleString('en-US', {
    month: 'short',
    day: 'numeric',
    hour: 'numeric',
    minute: '2-digit',
    hour12: true
  })
})
</script>

<style scoped>
.entry {
  margin-bottom: 25px;
  position: relative;
}
.entry-title-wrapper {
  position: relative;
  margin-bottom: 5px;
}
.title-bar {
  position: absolute;
  left: 0;
  color: red;
  font-weight: bold;
}
.entry-title {
  padding-left: 15px;
  font-weight: bold;
  width: 100%;
}
.entry-description {
  width: 100%;
  min-height: 40px;
  font-family: inherit;
  border: none;
  background: #f9f9f9;
  padding: 5px;
}
.entry-timestamp {
  font-size: 10px;
  color: #999;
  margin-top: 8px;
  font-style: italic;
}
</style>
