<template>
  <div>
    <!-- Hero -->
    <section class="hero">
      <div class="wrap">
        <div class="eyebrow">DETROIT, MICHIGAN</div>
        <h1 class="hero-head">MAKE STUFF.</h1>
        <div class="hero-head2">MEET PEOPLE.</div>
        <p class="hero-copy">
          A metro Detroit community organization focused on building in-person connection and community in the digital age through leftist values and crafting.<br/>All skill levels and crafts are welcome.
        </p>
        <div class="hero-ctas">
          <router-link to="/events" class="btn-solid">SEE UPCOMING EVENTS →</router-link>
          <a href="#" class="btn-outline">JOIN THE DISCORD</a>
        </div>
      </div>
    </section>

    <!-- Up next -->
    <section class="upnext">
      <div class="wrap">
        <div class="section-label">COMING UP NEXT</div>
        <div class="home-events-grid">
          <div v-for="(ev, i) in allEvents.slice(0, 3)" :key="i" class="event-card">
            <span v-if="ev.volunteerLed" class="vol-badge">VOLUNTEER-LED</span>
            <div class="event-date">{{ ev.date }} · {{ ev.time }}</div>
            <div class="event-title">{{ ev.title }}</div>
            <div class="event-venue">{{ ev.venue }} · {{ ev.city }}</div>
            <a :href="ev.link" class="rsvp-sm">RSVP</a>
          </div>
        </div>
        <div class="see-all">
          <router-link to="/events" class="see-all-link">SEE ALL EVENTS →</router-link>
        </div>
      </div>
    </section>

    <!-- Find us elsewhere -->
    <section class="elsewhere">
      <div class="wrap elsewhere-inner">
        <div class="elsewhere-label">FIND US ELSEWHERE</div>
        <div class="chips">
          <a v-for="(s, i) in socials" :key="i" :href="s.url" target="_blank" rel="noopener" class="chip">
            <span class="chip-icon" v-html="s.icon"></span>{{ s.label }}
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { allEvents } from '../data.js'

const socials = [
  { label: 'INSTAGRAM', url: 'https://instagram.com/YOUR_HANDLE', icon: '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="#F7F5EF" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="5"></rect><circle cx="12" cy="12" r="4"></circle><circle cx="17.5" cy="6.5" r="1" fill="#F7F5EF" stroke="none"></circle></svg>' },
  { label: 'TIKTOK', url: 'https://tiktok.com/@YOUR_HANDLE', icon: '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="#F7F5EF" stroke-width="2"><path d="M16 4v9a4 4 0 1 1-4-4"></path><path d="M16 4c0 2.5 2 4 4 4"></path></svg>' },
  { label: 'PARTIFUL', url: 'https://partiful.com/YOUR_HANDLE', icon: '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="#F7F5EF" stroke-width="2"><circle cx="12" cy="9" r="6"></circle><path d="M12 15v6"></path></svg>' },
  { label: 'DISCORD', url: 'https://discord.gg/YOUR_INVITE', icon: '<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#F7F5EF" stroke-width="2"><rect x="3" y="7" width="18" height="12" rx="3"></rect><circle cx="8.5" cy="13" r="1.5" fill="#F7F5EF" stroke="none"></circle><circle cx="15.5" cy="13" r="1.5" fill="#F7F5EF" stroke="none"></circle></svg>' },
  { label: 'SUBSTACK', url: 'https://YOUR_NAME.substack.com', icon: '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="#F7F5EF" stroke-width="2"><rect x="3" y="4" width="18" height="16" rx="2"></rect><path d="M3 8l9 6 9-6"></path></svg>' },
]
</script>

<style scoped>
.hero {
  background: #274249;
  padding: 40px 0 72px;
  text-align: center;
}
.eyebrow {
  font-family: 'Space Mono', monospace;
  font-size: 16px;
  color: #759a79;
  letter-spacing: 3px;
  margin-bottom: 28px;
}
.hero-head {
  font-family: 'Hello Imperfect', sans-serif;
  font-weight: 400;
  font-size: 104px;
  line-height: 0.9;
  color: #fdf8e9;
  margin: 0 0 8px;
  letter-spacing: -3px;
}
.hero-head2 {
  font-family: 'Hello Imperfect', sans-serif;
  font-weight: 400;
  font-size: 104px;
  line-height: 0.9;
  color: #759a79;
  margin: 0 0 32px;
  letter-spacing: -3px;
}
.hero-copy {
  font-size: 20px;
  line-height: 1.55;
  color: #fdf8e9;
  max-width: 560px;
  margin: 0 auto 36px;
  font-weight: 500;
}
.hero-ctas {
  display: flex;
  gap: 16px;
  justify-content: center;
  flex-wrap: wrap;
}
.btn-solid {
  display: inline-block;
  background: #fdf8e9;
  color: #274249;
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 16px;
  padding: 18px 34px;
  text-decoration: none;
}
.btn-outline {
  display: inline-block;
  border: 2px solid #fdf8e9;
  color: #fdf8e9;
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 16px;
  padding: 16px 34px;
  text-decoration: none;
}

.upnext {
  background: #fdf8e9;
  padding: 44px 0;
}
.section-label {
  font-family: 'Hello Imperfect', sans-serif;
  color: #274249;
  font-size: 18px;
  letter-spacing: 2px;
  margin-bottom: 22px;
}
.home-events-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}
.event-card {
  position: relative;
  border: 2px solid #274249;
  padding: 22px;
  display: flex;
  flex-direction: column;
  gap: 6px;
}
.vol-badge {
  position: absolute;
  top: 0;
  right: 0;
  background: #c1714a;
  color: #fdf8e9;
  font-family: 'Archivo Black', sans-serif;
  font-size: 12px;
  letter-spacing: 0.5px;
  padding: 5px 10px;
}
.event-date {
  font-family: 'Space Mono', monospace;
  font-size: 14px;
  font-weight: 700;
  color: #C1714A;
}
.event-title {
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 19px;
  color: #274249;
}
.event-venue {
  font-size: 14px;
  color: #274249;
}
.rsvp-sm {
  text-decoration: none;
  margin-top: 10px;
  background: #274249;
  color: #fdf8e9;
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 16px;
  padding: 10px 16px;
  text-align: center;
}
.see-all {
  margin-top: 24px;
  text-align: center;
}
.see-all-link {
  display: inline-block;
  color: #274249;
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 18px;
  text-decoration: underline;
}

.elsewhere {
  padding: 56px 0;
  border-bottom: 3px solid #274249;
  background: #e4ece0;
}
.elsewhere-inner {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
.elsewhere-label {
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 18px;
  letter-spacing: 2px;
  color: #3f5f44;
  margin-bottom: 16px;
}
.chips {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  justify-content: center;
}
.chip {
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: 10px;
  border: 2px solid #274249;
  color: #274249;
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 15px;
  padding: 10px 18px 10px 10px;
  border-radius: 4px;
}
.chip-icon {
  width: 28px;
  height: 28px;
  background: #274249;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 6px;
  flex-shrink: 0;
}
</style>
