<template>
  <div>
    <section class="intro">
      <div class="wrap">
        <div class="kicker">WHAT'S COMING UP</div>
        <h1 class="title">EVENTS</h1>
        <p class="body">We host most events on Partiful — tap through to RSVP.</p>
      </div>
    </section>

    <div class="events-list-wrap">
      <div v-for="(ev, i) in allEvents" :key="i" class="event-card">
        <span v-if="ev.volunteerLed" class="vol-badge">VOLUNTEER-LED</span>
        <div class="event-date">{{ ev.date }} · {{ ev.time }}</div>
        <div class="event-title">{{ ev.title }}</div>
        <div class="event-venue">{{ ev.venue }} · {{ ev.city }}</div>
        <div v-if="ev.masks" class="event-masks">😷 Masks required</div>
        <div v-else class="event-masks">Masks optional</div>
        <a :href="ev.link" class="rsvp">RSVP ON PARTIFUL</a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { allEvents } from '../data.js'
</script>

<style scoped>
.intro {
  padding: 64px 0 40px;
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
  font-size: 52px;
  line-height: 1.02;
  color: #274249;
  margin: 0 0 16px;
  max-width: 680px;
  letter-spacing: -1px;
}
.body {
  font-size: 17px;
  color: #274249;
  max-width: 560px;
  font-weight: 500;
}

.events-list-wrap {
  padding: 0 80px 56px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  width: 60%;
  margin: 0 auto;
}
.event-card {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 14px;
  background: #fdf8e9;
  border: 3px solid #274249;
  border-radius: 4px;
  padding: 26px 28px;
}
.vol-badge {
  position: absolute;
  top: 0;
  right: 0;
  background: #c1714a;
  color: #fdf8e9;
  font-family: 'Archivo Black', sans-serif;
  font-size: 11px;
  letter-spacing: 0.5px;
  padding: 6px 12px;
}
.event-date {
  font-family: 'Space Mono', monospace;
  font-size: 16px;
  font-weight: 700;
  color: #C1714A;
}
.event-title {
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 24px;
  color: #274249;
}
.event-venue {
  font-size: 16px;
  color: #274249;
}
.event-masks {
  font-size: 14px;
  color: #3f5f44;
  font-weight: 600;
}
.rsvp {
  text-decoration: none;
  background: #274249;
  color: #f7f5ef;
  font-family: 'Hello Imperfect', sans-serif;
  font-size: 18px;
  padding: 12px 20px;
  border-radius: 4px;
  text-align: center;
}
</style>
