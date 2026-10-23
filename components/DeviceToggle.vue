<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const isMobileMode = ref(false)

const toggleMode = () => {
  isMobileMode.value = !isMobileMode.value
  if (process.client) {
    if (isMobileMode.value) {
      document.body.classList.add('device-mobile-mode')
    } else {
      document.body.classList.remove('device-mobile-mode')
    }
  }
}

onUnmounted(() => {
  if (process.client) {
    document.body.classList.remove('device-mobile-mode')
  }
})
</script>

<template>
  <button
    class="device-toggle-btn"
    :class="{ 'is-active': isMobileMode }"
    @click="toggleMode"
    :title="isMobileMode ? 'Kembali ke tampilan Desktop' : 'Simulasi tampilan layar Smartphone'"
    aria-label="Toggle Mode Tampilan"
  >
    <span class="toggle-pulse"></span>
    <svg v-if="!isMobileMode" xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <rect width="14" height="20" x="5" y="2" rx="2" ry="2"/>
      <path d="M12 18h.01"/>
    </svg>
    <svg v-else xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <rect width="20" height="14" x="2" y="3" rx="2"/>
      <line x1="8" x2="16" y1="21" y2="21"/>
      <line x1="12" x2="12" y1="17" y2="21"/>
    </svg>
    <span>{{ isMobileMode ? 'Mode Desktop' : 'Mode Smartphone' }}</span>
  </button>
</template>
