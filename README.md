# PoRoRo Ice Cream - Nuxt Frontend (Project MKK Kel 6)

Proyek frontend website **PoRoRo Ice Cream** berbasis **Nuxt 3** dan **Vue 3**, diimplementasikan secara modular dan presisi berdasarkan desain Figma `beranda.fig` bagian *PoRoRo Ice Cream Design*.

---

## 🚀 Cara Menjalankan Proyek

Pastikan Node.js (v18+) sudah terpasang di komputer Anda.

### 1. Install Dependencies
```bash
npm install
```

### 2. Jalankan Server Pengembangan (Dev Mode)
```bash
npm run dev
```
Buka browser dan akses alamat yang tertera (biasanya `http://localhost:3000`).

### 3. Build untuk Produksi (SSR / Node Server)
```bash
npm run build
npm run preview
```

### 4. Generate Static Site (SSG / Jamstack)
```bash
npm run generate
```
Output hasil generate statis berada di folder `.output/public`.

---

## 📁 Struktur Direktori

```
C:/Project MKK Kel 6/
├── components/                     # Komponen modular Vue 3 (Auto-imported oleh Nuxt)
│   ├── Navbar.vue                  # Centered floating sticky pill navbar + mobile drawer
│   ├── HeroSection.vue             # Hero section, value proposition, headline, visual
│   ├── FavoriteFlavors.vue         # 4 kartu rasa favorit dengan tag dan harga
│   ├── IngredientPromise.vue       # Dapur & keunggulan bahan (susu lokal, buah asli)
│   ├── WeekendPromotion.vue        # Banner promo weekend 3=2 scoop ceria
│   ├── CraftProcess.vue            # 4 kartu proses pembuatan pastel (01 - 04)
│   ├── CustomerStories.vue         # Rating 4.9/5, ulasan pelanggan, tagar komunitas
│   ├── StoreLocation.vue           # Foto toko Cakung, alamat, jam buka, tombol maps
│   ├── OrderCta.vue                # Call-to-action delivery 30 menit
│   └── SiteFooter.vue              # Brand statement, navigasi, form newsletter, halal
├── public/
│   └── images/                     # 10 aset gambar resolusi tinggi asli dari Figma
│       ├── hero-gelato.jpg
│       ├── flavor-pistachio.jpg
│       ├── flavor-cheesecake.jpg
│       ├── flavor-caramel.jpg
│       ├── flavor-mango.jpg
│       ├── ingredient-promise.jpg
│       ├── promo-sundae.jpg
│       ├── community-stories.jpg
│       ├── store-cakung.png
│       └── delivery-collection.png
├── assets/
│   └── css/
│       └── main.css                # Master styling, variabel warna, tipografi & layout
├── app.vue                         # Root Vue layout yang merangkai seluruh section
├── nuxt.config.ts                  # Konfigurasi Nuxt 3 (Google Fonts, SEO metadata, CSS)
├── package.json                    # Konfigurasi dependensi dan scripts npm
├── index.html                      # Versi HTML & CSS statis asli
└── index.static.html               # Backup versi statis
```

---

## 🎨 Fitur Utama

1. **Komponen Modular**: Setiap section dipecah menjadi komponen tersendiri di folder `components/` yang mudah dirawat dan dikembangkan.
2. **Centered Floating Navbar**: Navigasi sticky berbentuk kapsul melayang yang posisinya persis di tengah layar dengan efek glassmorphism (`backdrop-filter: blur(16px)`).
3. **Responsive Mobile Navigation**: Dilengkapi hamburger toggle animasi dan drawer menu interaktif untuk perangkat tablet dan smartphone.
4. **Data-Driven Flavor List**: Daftar menu es krim favorit menggunakan reactive array Vue 3 (`v-for`) sehingga mudah dihubungkan ke API / CMS di masa mendatang.
5. **Tipografi & Desain Asli Figma**: Menggunakan Google Fonts *Fraunces* (display serif) dan *DM Sans* (geometric sans), dengan warna khas pastel (Lavender, Peach, Sky Blue, Yellow, Mint) dan brand pink.
