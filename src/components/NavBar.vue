<template>
  <nav class="nav">
    <div class="wrap nav-inner">
      <router-link to="/" class="logo">
        <div class="logo-badge">
          <img src="../assets/dcc_logo_primary_light_svg.svg" alt="Detroit Craft Club">
        </div>
      </router-link>
      <div class="links">
        <router-link to="/" class="link" active-class="active" exact-active-class="active">Home</router-link>
        <router-link to="/about" class="link" active-class="active">About</router-link>
        <router-link to="/events" class="link" active-class="active">Events</router-link>
      </div>
    </div>
  </nav>
</template>

<script setup></script>

<style scoped>
.nav {
  padding: 20px 0;
  border-bottom: 3px solid #274249;
  background: #274249;
}
.nav-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo {
  display: flex;
  align-items: center;
  gap: 14px;
  cursor: pointer;
}
.logo-badge {
  width: 60px;
  height: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  gap: 1px;
}
.logo-badge span {
  font-family: 'Archivo Black', sans-serif;
  color: #274249;
  font-size: 9px;
  letter-spacing: -0.2px;
  line-height: 1;
}
.links {
  display: flex;
  gap: 28px;
  font-size: 15px;
  font-weight: 600;
}
.link {
  cursor: pointer;
  text-decoration: none;
  color: #fdf8e9;
  opacity: 0.55;
}
.link.active {
  opacity: 1;
}
</style>
