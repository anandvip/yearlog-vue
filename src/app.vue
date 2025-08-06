<template>
  <div class="container">
    <HeaderBar />
    
    <main class="main">
      <EntryCard
        v-for="entry in entries"
        :key="entry.id"
        :entry="entry"
      />
    </main>
    
    <FooterBar />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import HeaderBar from './components/HeaderBar.vue'
import EntryCard from './components/EntryCard.vue'
import FooterBar from './components/FooterBar.vue'

const entries = ref([
  { id: 1, title: 'First Entry', description: 'This is just a test.' },
  { id: 2, title: 'Second Entry', description: 'Vue is reactive!' },
  { id: 3, title: 'Third Entry', description: 'visit https://anandvip.github.io/yearlog-vue/dev' }
])
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.main {
  padding: 2rem;
}
</style>
