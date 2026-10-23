<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const isMobileMenuOpen = ref(false)
const navbarRef = ref<HTMLElement | null>(null)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}

const handleClickOutside = (event: MouseEvent) => {
  if (navbarRef.value && !navbarRef.value.contains(event.target as Node)) {
    closeMobileMenu()
  }
}

const handleKeyDown = (event: KeyboardEvent) => {
  if (event.key === 'Escape') {
    closeMobileMenu()
  }
}

onMounted(() => {
  document.addEventListener('click', handleClickOutside)
  document.addEventListener('keydown', handleKeyDown)
})

onUnmounted(() => {
  document.removeEventListener('click', handleClickOutside)
  document.removeEventListener('keydown', handleKeyDown)
})
</script>

<template>
  <div class="navbar-wrapper">
    <nav ref="navbarRef" class="navbar" id="navbar">
      <!-- Brand Logo -->
      <a href="#beranda" class="brand" @click="closeMobileMenu">
        <div class="brand-mark">
          <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="m7 11 4.08 10.35a1 1 0 0 0 1.84 0L17 11"/>
            <path d="M17 7A5 5 0 0 0 7 7"/>
            <path d="M17 7a2 2 0 0 1 0 4H7a2 2 0 0 1 0-4"/>
          </svg>
        </div>
        <span class="brand-name">PoRoRo Ice Cream</span>
      </a>

      <!-- Desktop Centered Navigation Links -->
      <div class="nav-links">
        <a href="#rasa" class="nav-link active">Rasa</a>
        <a href="#cerita" class="nav-link">Cerita Kami</a>
        <a href="#lokasi" class="nav-link">Lokasi</a>
        <a href="#pesan" class="nav-link">Pesan Online</a>
      </div>

      <!-- Right Side Actions & Mobile Toggle -->
      <div class="nav-actions">
        <a href="#pesan" class="btn btn-primary nav-cta">
          <span>Ambil Satu Scoop</span>
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M7 7h10v10"/>
            <path d="M7 17 17 7"/>
          </svg>
        </a>

        <!-- Mobile Hamburger Button -->
        <button
          class="mobile-toggle"
          :class="{ 'is-active': isMobileMenuOpen }"
          @click.stop="toggleMobileMenu"
          aria-label="Buka Menu Navigasi"
          :aria-expanded="isMobileMenuOpen"
        >
          <span class="hamburger-line"></span>
          <span class="hamburger-line"></span>
          <span class="hamburger-line"></span>
        </button>
      </div>

      <!-- Mobile Navigation Drawer Menu -->
      <div class="mobile-menu" :class="{ 'is-active': isMobileMenuOpen }">
        <div class="mobile-nav-links">
          <a href="#rasa" class="mobile-nav-link active" @click="closeMobileMenu">
            <span>Rasa</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
          </a>
          <a href="#cerita" class="mobile-nav-link" @click="closeMobileMenu">
            <span>Cerita Kami</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
          </a>
          <a href="#lokasi" class="mobile-nav-link" @click="closeMobileMenu">
            <span>Lokasi</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
          </a>
          <a href="#pesan" class="mobile-nav-link" @click="closeMobileMenu">
            <span>Pesan Online</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
          </a>
        </div>

        <div class="mobile-menu-footer">
          <a href="#pesan" class="btn btn-primary mobile-cta" @click="closeMobileMenu">
            <span>Ambil Satu Scoop</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M7 7h10v10"/>
              <path d="M7 17 17 7"/>
            </svg>
          </a>
        </div>
      </div>
    </nav>
  </div>
</template>
