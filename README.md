# WiFi Portal PWA - tebudiv3.net

Progressive Web App sederhana untuk akses cepat ke portal WiFi tebudiv3.net

## 📱 Fitur
- ✅ Bisa diinstall seperti aplikasi native
- ✅ Muncul di launcher/home screen
- ✅ Berjalan dalam mode standalone (fullscreen)
- ✅ Offline-ready dengan Service Worker
- ✅ Icon kustom untuk aplikasi
- ✅ Ringan dan cepat

## 🚀 Cara Deploy

### Opsi 1: Deploy ke GitHub Pages (GRATIS)

1. **Buat repository baru di GitHub**
   - Pergi ke https://github.com/new
   - Nama repository: `wifi-portal-pwa`
   - Public repository
   - Klik "Create repository"

2. **Upload semua file**
   - Upload file-file ini ke repository:
     - index.html
     - manifest.json
     - service-worker.js
     - icon-192.png
     - icon-512.png

3. **Aktifkan GitHub Pages**
   - Pergi ke Settings > Pages
   - Source: Deploy from a branch
   - Branch: main / root
   - Klik Save

4. **Akses PWA**
   - URL: `https://username.github.io/wifi-portal-pwa/`
   - Ganti `username` dengan username GitHub Anda

### Opsi 2: Deploy ke Netlify (GRATIS)

1. **Drag & Drop**
   - Pergi ke https://app.netlify.com/drop
   - Drag semua file (index.html, manifest.json, dll)
   - Tunggu hingga deploy selesai

2. **Akses PWA**
   - URL akan diberikan otomatis
   - Format: `https://random-name.netlify.app`

### Opsi 3: Deploy ke Vercel (GRATIS)

1. **Install Vercel CLI**
   ```bash
   npm i -g vercel
   ```

2. **Deploy**
   ```bash
   cd folder-pwa
   vercel
   ```

3. **Akses PWA**
   - URL akan diberikan setelah deploy

### Opsi 4: Hosting Sendiri (Server/HP)

Jika punya server atau ingin host di HP:

1. **Install web server** (misal: Python)
   ```bash
   python3 -m http.server 8080
   ```

2. **Akses dari browser**
   - Buka: `http://localhost:8080`
   - Atau dari HP lain di jaringan yang sama: `http://IP-SERVER:8080`

**PENTING:** PWA harus diakses via HTTPS (kecuali localhost)!

## 📲 Cara Install PWA di HP

### Android - Chrome

1. Buka URL PWA di Chrome
2. Klik menu (⋮) > "Add to Home screen" atau "Install app"
3. Klik "Install" atau "Add"
4. Aplikasi akan muncul di launcher

### Android - Samsung Internet

1. Buka URL PWA
2. Klik menu (☰) > "Add page to" > "Home screen"
3. Aplikasi akan muncul di launcher

### iOS - Safari

1. Buka URL PWA di Safari
2. Klik tombol Share (kotak dengan panah)
3. Scroll dan pilih "Add to Home Screen"
4. Klik "Add"

## 🔧 Kustomisasi

### Ubah URL Portal

Edit file `index.html`, cari baris:
```javascript
window.location.href = 'http://tebudiv3.net/login';
```

Ganti dengan URL portal yang sesuai.

### Ubah Nama Aplikasi

Edit file `manifest.json`:
```json
{
  "name": "WiFi Portal - tebudiv3.net",
  "short_name": "WiFi Portal"
}
```

### Ubah Warna Tema

Edit `manifest.json`:
```json
{
  "background_color": "#667eea",
  "theme_color": "#667eea"
}
```

## ⚠️ Troubleshooting

### PWA tidak bisa diinstall?
- Pastikan diakses via HTTPS (atau localhost)
- Pastikan semua file (manifest.json, icon, service-worker.js) ada
- Coba clear cache browser dan reload

### Tidak muncul di launcher setelah install?
- Coba restart HP
- Cek di App Drawer
- Pastikan installer tidak diblok oleh StrictLauncher

### Icon tidak muncul?
- Pastikan file icon-192.png dan icon-512.png sudah diupload
- Path di manifest.json harus benar
- Coba reinstall PWA

## 📝 Struktur File

```
wifi-portal-pwa/
├── index.html           # Halaman utama
├── manifest.json        # PWA configuration
├── service-worker.js    # Offline support
├── icon-192.png        # Icon 192x192
├── icon-512.png        # Icon 512x512
└── README.md           # Dokumentasi ini
```

## 💡 Tips

1. **Bookmark dulu** sebelum install untuk testing
2. **Test di browser** dulu sebelum install sebagai PWA
3. **Gunakan HTTPS** untuk fitur PWA lengkap
4. **Update cache** dengan increment versi di service-worker.js

## 🌐 Rekomendasi Hosting Gratis

1. **GitHub Pages** - Paling mudah, support custom domain
2. **Netlify** - Drag & drop, auto HTTPS
3. **Vercel** - Cepat, cocok untuk developer
4. **Firebase Hosting** - Google, reliable
5. **Cloudflare Pages** - Global CDN, gratis unlimited

Semua opsi di atas support HTTPS otomatis! ✅

## 📞 Support

Jika ada masalah, pastikan:
- Browser sudah support PWA (Chrome, Edge, Samsung Internet)
- File manifest.json dan service-worker.js accessible
- URL diakses via HTTPS (wajib untuk PWA)
