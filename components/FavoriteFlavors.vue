<script setup lang="ts">
interface Flavor {
  name: string
  price: string
  note: string
  tag: string
  image: string
}

const flavors: Flavor[] = [
  {
    name: 'Pistachio Sicilia',
    price: 'Rp42k',
    note: 'Nutty, lembut, sedikit asin',
    tag: 'Terlaris',
    image: '/images/flavor-pistachio.jpg'
  },
  {
    name: 'Berry Cheesecake',
    price: 'Rp39k',
    note: 'Tangy, creamy, swirl beri',
    tag: 'Favorit',
    image: '/images/flavor-cheesecake.jpg'
  },
  {
    name: 'Sea Salt Caramel',
    price: 'Rp39k',
    note: 'Manis-karamel, sentuhan laut',
    tag: 'Signature',
    image: '/images/flavor-caramel.jpg'
  },
  {
    name: 'Mango Sorbet',
    price: 'Rp36k',
    note: 'Segar, juicy, bebas dairy',
    tag: 'Vegan',
    image: '/images/flavor-mango.jpg'
  }
]
</script>

<template>
  <section class="section flavors-section" id="rasa">
    <div class="container">
      <div class="section-header">
        <div class="header-left">
          <div class="eyebrow">
            <span class="dot"></span>
            <span class="eyebrow-text">FAVORIT MINGGU INI</span>
          </div>
          <h2 class="section-title">Rasa yang paling sering bikin senyum.</h2>
          <p class="section-description">
            Dari pistachio kaya rasa hingga sorbet buah segar—ini empat varian yang paling cepat habis di display kami.
          </p>
        </div>
        <div class="header-right">
          <a href="#pesan" class="btn btn-outline btn-pill">
            <span>Jelajahi 18 Rasa</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M7 7h10v10"/>
              <path d="M7 17 17 7"/>
            </svg>
          </a>
        </div>
      </div>

      <div class="flavors-grid">
        <article v-for="flavor in flavors" :key="flavor.name" class="flavor-card">
          <div class="flavor-media">
            <span class="flavor-tag">{{ flavor.tag }}</span>
            <img :src="flavor.image" :alt="flavor.name" class="flavor-img" loading="lazy">
          </div>
          <div class="flavor-details">
            <div class="name-price-row">
              <h3 class="flavor-name">{{ flavor.name }}</h3>
              <span class="flavor-price">{{ flavor.price }}</span>
            </div>
            <p class="flavor-note">{{ flavor.note }}</p>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>
