<template>
  <section class="section store-section" id="lokasi">
    <div class="container">
      <div class="two-column-layout align-center">
        <!-- Store Visual -->
        <div class="column-visual">
          <div class="visual-wrap">
            <img src="/images/store-cakung.png" alt="Toko PoRoRo Cakung Jakarta Timur" class="rounded-img" loading="lazy">
            <div class="floating-badge badge-location">
              <span class="location-name">Cakung, Jakarta Timur</span>
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="pin-icon">
                <path d="M20 10c0 4.993-5.539 10.193-7.399 11.799a1 1 0 0 1-1.202 0C9.539 20.193 4 14.993 4 10a8 8 0 0 1 16 0"/>
                <circle cx="12" cy="10" r="3"/>
              </svg>
            </div>
          </div>
        </div>

        <!-- Store Details -->
        <div class="column-copy">
          <div class="eyebrow">
            <span class="dot"></span>
            <span class="eyebrow-text">MAMPIR, YUK!</span>
          </div>
          <h2 class="section-title">Satu sudut manis di tengah Cakung</h2>
          <p class="section-description">
            Duduk santai di teras, lihat gelato dibuat dari dapur terbuka, atau ambil cepat untuk perjalanan pulang.
          </p>

          <div class="store-info-blocks">
            <!-- Address -->
            <div class="info-block">
              <div class="info-icon icon-lavender">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <polygon points="3 11 22 2 13 21 11 13 3 11"/>
                </svg>
              </div>
              <div class="info-content">
                <span class="info-label">Alamat</span>
                <span class="info-value">Jl. Dr. KRT Radjiman Widoyodiningrat, Cakung, Jakarta Timur</span>
              </div>
            </div>

            <!-- Hours -->
            <div class="info-block">
              <div class="info-icon icon-yellow">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <circle cx="12" cy="12" r="10"/>
                  <polyline points="12 6 12 12 16.5 12"/>
                </svg>
              </div>
              <div class="info-content">
                <span class="info-label">Jam buka</span>
                <div class="hours-rows">
                  <div class="hours-row">
                    <span class="hours-days">Senin–Jumat</span>
                    <span class="hours-time">11.00–22.00</span>
                  </div>
                  <div class="hours-row">
                    <span class="hours-days">Sabtu–Minggu</span>
                    <span class="hours-time">10.00–23.00</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="store-actions">
            <a href="https://maps.google.com" target="_blank" rel="noopener noreferrer" class="btn btn-primary">
              <span>Buka di Maps</span>
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="m8 6 4-4 4 4"/>
                <path d="M12 2v10.3a4 4 0 0 1-1.172 2.872L4 22"/>
                <path d="m20 22-5-5"/>
              </svg>
            </a>
            <a href="https://wa.me/" target="_blank" rel="noopener noreferrer" class="btn btn-outline">
              <span>Hubungi Toko</span>
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/>
              </svg>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
