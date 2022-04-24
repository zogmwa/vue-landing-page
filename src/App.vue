<script setup lang="ts">
import Header from './components/Header.vue'
import DropdownMenu from './components/DropdownMenu.vue'
import MainContent from './components/MainContent.vue'
</script>

<template>
  <Header />
  <DropdownMenu />
  <MainContent />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
