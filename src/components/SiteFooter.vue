<template>
  <footer class="footer">
    <div class="wrap footer-inner">
      <div class="copy">© Detroit Craft Club</div>
      <div class="socials">
        <a v-for="(s, i) in socials" :key="i" :href="s.url" target="_blank" rel="noopener" class="social" v-html="s.icon"></a>
      </div>
    </div>
  </footer>
</template>

<script setup>
const socials = [
  { url: 'https://instagram.com/YOUR_HANDLE', icon: '<svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="#FDF8E9" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="5"></rect><circle cx="12" cy="12" r="4"></circle><circle cx="17.5" cy="6.5" r="1" fill="#FDF8E9" stroke="none"></circle></svg>' },
  { url: 'https://tiktok.com/@YOUR_HANDLE', icon: '<svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="#FDF8E9" stroke-width="2"><path d="M16 4v9a4 4 0 1 1-4-4"></path><path d="M16 4c0 2.5 2 4 4 4"></path></svg>' },
  { url: 'https://partiful.com/YOUR_HANDLE', icon: '<svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="#FDF8E9" stroke-width="2"><circle cx="12" cy="9" r="6"></circle><path d="M12 15v6"></path></svg>' },
  { url: 'https://discord.gg/YOUR_INVITE', icon: '<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#FDF8E9" stroke-width="2"><rect x="3" y="7" width="18" height="12" rx="3"></rect><circle cx="8.5" cy="13" r="1.5" fill="#FDF8E9" stroke="none"></circle><circle cx="15.5" cy="13" r="1.5" fill="#FDF8E9" stroke="none"></circle></svg>' },
  { url: 'https://YOUR_NAME.substack.com', icon: '<svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="#FDF8E9" stroke-width="2"><rect x="3" y="4" width="18" height="16" rx="2"></rect><path d="M3 8l9 6 9-6"></path></svg>' },
]
</script>

<style scoped>
.footer {
  padding: 32px 0;
  background: #274249;
  border-top: 3px solid #274249;
}
.footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.copy {
  font-family: 'Space Mono', monospace;
  font-size: 13px;
  color: #fdf8e9;
}
.socials {
  display: flex;
  gap: 14px;
  align-items: center;
}
.social {
  display: flex;
}
</style>
