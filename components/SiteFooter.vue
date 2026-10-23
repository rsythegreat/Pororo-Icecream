<script setup lang="ts">
import { ref } from 'vue'

const email = ref('')

const handleNewsletterSubmit = () => {
  if (email.value) {
    alert(`Terima kasih telah berlangganan newsletter PoRoRo Ice Cream (${email.value})!`)
    email.value = ''
  }
}
</script>

<template>
  <footer class="site-footer" id="kontak">
    <div class="container">
      <div class="footer-main">
        <!-- Brand Info -->
        <div class="footer-brand">
          <a href="#beranda" class="brand brand-white">
            <div class="brand-mark">
              <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="m7 11 4.08 10.35a1 1 0 0 0 1.84 0L17 11"/>
                <path d="M17 7A5 5 0 0 0 7 7"/>
                <path d="M17 7a2 2 0 0 1 0 4H7a2 2 0 0 1 0-4"/>
              </svg>
            </div>
            <span class="brand-name">PoRoRo Ice Cream</span>
          </a>
          <p class="brand-statement">
            Gelato artisan yang dibuat segar setiap hari, untuk momen kecil yang terasa istimewa.
          </p>
          <div class="social-links">
            <a href="https://instagram.com" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="Instagram">
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <rect width="20" height="20" x="2" y="2" rx="5" ry="5"/>
                <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/>
                <line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/>
              </svg>
            </a>
            <a href="https://tiktok.com" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="TikTok">
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <circle cx="8" cy="18" r="4"/>
                <path d="M12 18V2l7 4"/>
              </svg>
            </a>
            <a href="https://wa.me/" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="WhatsApp">
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M7.9 20A9 9 0 1 0 4 16.1L2 22Z"/>
              </svg>
            </a>
          </div>
        </div>

        <!-- Footer Navigation Links -->
        <div class="footer-nav">
          <div class="link-group">
            <h4 class="link-heading heading-peach">Jelajahi</h4>
            <ul class="link-list">
              <li><a href="#rasa">Semua Rasa</a></li>
              <li><a href="#pesan">Gelato Cake</a></li>
              <li><a href="#cerita">Tentang Kami</a></li>
              <li><a href="#kontak">Karier</a></li>
            </ul>
          </div>

          <div class="link-group">
            <h4 class="link-heading heading-mint">Bantuan</h4>
            <ul class="link-list">
              <li><a href="#pesan">Pesan Online</a></li>
              <li><a href="#">FAQ</a></li>
              <li><a href="#">Catering & Event</a></li>
              <li><a href="#lokasi">Hubungi Kami</a></li>
            </ul>
          </div>

          <!-- Newsletter -->
          <div class="footer-newsletter">
            <h4 class="link-heading heading-yellow">Scoop letter</h4>
            <p class="newsletter-desc">Rasa baru, promo, dan cerita manis—langsung ke inbox.</p>
            <form class="email-form" @submit.prevent="handleNewsletterSubmit">
              <input
                v-model="email"
                type="email"
                placeholder="Email kamu"
                required
                class="email-input"
              >
              <button type="submit" class="submit-btn" aria-label="Kirim Email">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M5 12h14"/>
                  <path d="m12 5 7 7-7 7"/>
                </svg>
              </button>
            </form>
          </div>
        </div>
      </div>

      <div class="footer-divider"></div>

      <div class="footer-meta">
        <span class="copyright">© 2026 PoRoRo Ice Cream. Made fresh in Jakarta.</span>
        <div class="legal-links">
          <a href="#">Privasi</a>
          <a href="#">Syarat & Ketentuan</a>
          <span class="cert-halal">100% HALAL</span>
        </div>
      </div>
    </div>
  </footer>
</template>
