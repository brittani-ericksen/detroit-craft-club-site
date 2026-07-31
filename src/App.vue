<template>
  <div class="site-shell">
    <NavBar />
    <router-view />
    <SiteFooter />
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import SiteFooter from './components/SiteFooter.vue'
</script>

<style scoped>
.site-shell {
  width: 100%;
  background: #e4ece0;
  font-family: 'Work Sans', sans-serif;
  position: relative;
  overflow: hidden;
}
</style>
