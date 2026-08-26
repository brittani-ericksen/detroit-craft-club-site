<template>
  <div>
    <section class="intro">
      <div class="wrap">
        <div class="kicker">ABOUT US</div>
        <h1 class="title">YOUR LOCAL RADICAL LEFTIST CRAFTERS.</h1>
        <p class="body">
          About us coming soon.
        </p>
      </div>
    </section>

    <section class="team">
      <div class="wrap">
        <div class="team-label">RUN BY</div>
        <div class="admins-grid">
          <div v-for="(a, i) in admins" :key="i" class="admin-card">
            <div class="admin-photo">
              <span>photo placeholder</span>
            </div>
            <div class="admin-name">{{ a.name }}</div>
            <div class="admin-role">{{ a.role }}</div>
            <div class="admin-blurb">{{ a.blurb }}</div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { admins } from '../data.js'
</script>

<style scoped>
.intro {
  padding: 64px 0 48px;
}
.kicker {
  font-family: 'Space Mono', monospace;
  font-size: 16px;
  color: #759a79;
  margin-bottom: 14px;
  letter-spacing: 1px;
}
.title {
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 48px;
  line-height: 1.05;
  color: #274249;
  margin: 0 0 24px;
  max-width: 680px;
  letter-spacing: -1px;
}
.body {
  font-size: 18px;
  line-height: 1.65;
  color: #274249;
  max-width: 600px;
  font-weight: 500;
}

.team {
  background: #759a79;
  padding: 56px 0;
}
.team-label {
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 22px;
  letter-spacing: 2px;
  color: #274249;
  margin-bottom: 28px;
}
.admins-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
.admin-card {
  background: #fdf8e9;
  border-radius: 4px;
  padding: 24px;
}
.admin-photo {
  width: 100%;
  aspect-ratio: 1;
  background: repeating-linear-gradient(135deg, #e3ddce, #e3ddce 10px, #dbd4c2 10px, #dbd4c2 20px);
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 16px;
}
.admin-photo span {
  font-family: 'Space Mono', monospace;
  font-size: 12px;
  color: #274249;
  opacity: 0.6;
}
.admin-name {
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 18px;
  color: #274249;
}
.admin-role {
  font-family: 'Space Mono', monospace;
  font-size: 12px;
  color: #c1714a;
  margin: 6px 0 10px;
  font-weight: 700;
}
.admin-blurb {
  font-size: 14px;
  color: #274249;
  line-height: 1.5;
}
</style>
