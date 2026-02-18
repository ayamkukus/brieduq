# BRI EduQ Smart Queue – Deployment Guide

## File Structure
```
bri-eduq/
├── index.html        ← Microsite utama (PWA)
├── manifest.json     ← PWA manifest
├── sw.js             ← Service worker (offline)
├── qr-generator.html ← Generator QR Code untuk karcis
└── README.md         ← Panduan ini
```

## Cara Deploy (Gratis)

### Option 1: Vercel (Paling Mudah)
1. Buat akun di vercel.com
2. Install Vercel CLI: `npm i -g vercel`
3. Masuk folder ini: `cd bri-eduq`
4. Jalankan: `vercel`
5. URL otomatis: `https://bri-eduq.vercel.app`

### Option 2: Netlify
1. Buat akun di netlify.com
2. Drag & drop folder `bri-eduq` ke netlify.com/drop
3. URL otomatis jadi: `https://randomname.netlify.app`
4. Bisa custom domain

### Option 3: GitHub Pages
1. Push ke GitHub repo
2. Settings → Pages → Deploy from branch
3. URL: `https://username.github.io/bri-eduq`

### Option 4: Cloudflare Pages
1. Buat akun di pages.cloudflare.com
2. Connect GitHub repo atau upload manual
3. URL: `https://bri-eduq.pages.dev`

---

## Cara Generate QR Code

1. Buka `qr-generator.html` di browser
2. Masukkan URL deployment Anda (misal `https://bri-eduq.vercel.app`)
3. Klik **Generate**
4. Download PNG atau langsung Print
5. QR Code terintegrasi ke preview karcis

### Deep Link per Layanan
Anda bisa buat QR berbeda untuk tiap loket:
- `?s=rekening-baru` → Langsung ke checklist buka rekening
- `?s=tutup-rekening` → Langsung ke checklist tutup rekening
- `?s=ubah-data` → Langsung ke checklist ubah data
- `?s=digital-banking` → Langsung ke checklist digital banking
- `?s=kartu-atm` → Langsung ke checklist kartu ATM

Contoh: `https://bri-eduq.vercel.app?s=rekening-baru`

---

## Fitur Microsite

✅ **PWA** – Bisa di-install sebagai app dari browser HP (Add to Home Screen)
✅ **Offline** – Service worker cache agar tetap jalan tanpa internet
✅ **Zero Login** – Langsung bisa diakses dari QR scan
✅ **5 Checklist** – Buka rekening, tutup rekening, ubah data, digital banking, kartu ATM
✅ **PSA Keamanan** – Edukasi bahaya jual beli rekening
✅ **Animasi** – Smooth transitions, confetti, haptic feedback
✅ **Mobile First** – Dioptimalkan untuk layar HP

## Cara Akses dari HP via QR
1. Buka kamera HP
2. Arahkan ke QR Code di karcis
3. Tap notifikasi link yang muncul
4. Microsite langsung terbuka di browser
5. Bisa tambah ke home screen sebagai app

---

## Kontak & Pengembangan
KC MPH BRI · EduQ System 2025
