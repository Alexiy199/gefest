<script setup>
//import { RouterLink, RouterView } from 'vue-router'
//import { i } from 'vite/dist/node/types.d-aGj9QkWt';
import HeaderBlock from './components/HeaderBlock.vue'
import StartPage from './components/StartPage.vue'
import CasePage from './components/CasePage.vue'
import ContactsPage from './components/ContactsPage.vue'
</script>

<template>
  <HeaderBlock />
  <main class="main">
    <StartPage />
    <CasePage />
    <ContactsPage />
  </main>
</template>

<style scoped>
.main {
  width: 100vw;
  height: 100vh;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
  overflow-y: auto;
  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
}
</style>
