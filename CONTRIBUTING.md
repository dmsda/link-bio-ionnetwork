# 🤝 Panduan Kontribusi - ION Network Link in Bio

Terima kasih atas minat Anda untuk berkontribusi pada pengembangan repositori resmi **ION Network Link in Bio & Showcase**! Proyek ini terbuka bagi seluruh developer, desainer UI/UX, dan staf internal untuk memelihara dan meningkatkan kualitas antarmuka profil digital perusahaan.

---

## 🛠️ Persiapan Lingkungan Kerja Lokal (Local Setup)

### 1. Prasyarat
- **Node.js**: Versi 16 atau lebih tinggi (disarankan versi LTS terbaru).
- **Git**: Terpasang di komputer lokal.
- **Peramban Web Modern**: Chrome, Firefox, Safari, atau Edge.

### 2. Langkah Instalasi & Menjalankan Proyek
```bash
# 1. Clone repository dari GitHub
git clone https://github.com/dmsda/link-bio-ionnetwork.git

# 2. Masuk ke direktori proyek
cd link-bio-ionnetwork

# 3. Jalankan server lokal
npm start
# atau
node server.js
```

Setelah server aktif, buka peramban Anda pada alamat:
- **Link in Bio Utama**: `http://localhost:3000/`
- **Product Showcase & Simulator**: `http://localhost:3000/showcase.html`

> Proyek ini **tidak membutuhkan instalasi paket eksternal (Zero NPM dependencies)**, sehingga proses *bootstrapping* instan tanpa perlu menjalankan `npm install`.

---

## 📐 Standar Koding & Pedoman Desain

### 1. Standar HTML & Aksesibilitas (A11y)
* Gunakan elemen semantik HTML5 (`<main>`, `<header>`, `<nav>`, `<section>`, `<footer>`, `<article>`).
* Pastikan seluruh tautan eksternal menyertakan atribut `target="_blank"`, `rel="noopener noreferrer"`, dan `aria-label` yang deskriptif.
* Pertahankan dimensi gambar eksplisit (`width="92" height="92"`) guna mencegah *Cumulative Layout Shift* (CLS).
* Semua ikon SVG dekoratif wajib memiliki `aria-hidden="true"`.

### 2. Standar CSS & Token Desain
* **Gunakan Token Warna Resmi**: Dilarang menggunakan nilai warna *hardcoded* secara sembarangan. Gunakan selalu variabel CSS yang didefinisikan pada `:root`:
  - `--color-primary`: `#1974d2`
  - `--color-secondary`: `#212322`
  - `--color-tertiary`: `#000000`
  - `--color-accent`: `#fed809`
* Gunakan format font resmi **Inter** dari Google Fonts.
* Pastikan target sentuh mobile memenuhi standar $\ge 48\text{px}$.

---

## 💡 Tutorial: Cara Menambahkan Kartu Tautan Baru

Untuk menambahkan tautan baru ke dalam halaman utama (`index.html`), ikuti struktur komponen kartu berikut di dalam kontainer `<nav class="social-links">`:

```html
<!-- Contoh: Menambahkan Tautan Saluran Telegram Resmi -->
<a href="https://t.me/ionnetwork_official" 
   class="social-link" 
   target="_blank" 
   rel="noopener noreferrer"
   aria-label="Bergabung ke Saluran Telegram Resmi ION Network">  
    <div class="link-left">
        <div class="icon-box" aria-hidden="true">
            <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm4.64 6.8l-1.6 7.53c-.12.54-.44.67-.89.42l-2.46-1.81-1.19 1.15c-.13.13-.24.24-.49.24l.18-2.5 4.56-4.12c.2-.18-.04-.27-.31-.1l-5.63 3.55-2.43-.76c-.53-.16-.54-.53.11-.78l9.49-3.66c.44-.16.82.1.66.84z"/>
            </svg>
        </div>
        <div class="link-text-group">
            <span class="link-title">Telegram Resmi</span>
            <span class="link-subtitle">@ionnetwork_official</span>
        </div>
    </div>
    <div class="link-right">
        <!-- Opsional: Tambahkan badge jika perlu -->
        <!-- <span class="badge badge-primary">Baru</span> -->
        <svg class="link-chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <path d="M9 18l6-6-6-6"/>
        </svg>
    </div>
</a>
```

Jika tautan tersebut merupakan akun media sosial resmi korporat, pastikan juga memperbarui array `sameAs` di dalam tag `<script type="application/ld+json">` pada bagian bawah `index.html`.

---

## 🔀 Konvensi Pesan Commit (Conventional Commits)

Kami menggunakan format commit konvensional untuk mempermudah pelacakan riwayat pembaruan:

* `feat:` Penambahan fitur baru (misal: `feat: add telegram channel card`).
* `fix:` Perbaikan bug atau kesalahan tata letak (misal: `fix: avatar verification badge positioning`).
* `docs:` Pembaruan atau penambahan dokumentasi (misal: `docs: update ARCHITECTURE.md and SHOWCASE.md`).
* `style:` Penyesuaian tampilan, spasi, CSS tanpa mengubah fungsionalitas (misal: `style: refine hover glow on action cards`).
* `perf:` Optimasi kinerja muat halaman atau kompresi aset (misal: `perf: optimize svg icon rendering`).
* `chore:` Pemeliharaan dependensi, package.json, atau server script (misal: `chore: update server.js MIME types`).

---

## 📋 Checklist Sebelum Mengirim Pull Request (PR)

Sebelum melakukan `git push` dan membuat Pull Request:
- [ ] Kode HTML valid dan terformat rapi.
- [ ] Tautan eksternal berfungsi dengan baik dan memiliki `aria-label`.
- [ ] Tidak ada error di browser console.
- [ ] Tampilan telah diuji pada layar mobile kecil ($\le 360\text{px}$) dan desktop.
- [ ] Dokumen `README.md` atau `SHOWCASE.md` telah diperbarui jika ada perubahan fitur atau struktur penting.
