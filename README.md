# ION Network - Official Link in Bio & Profile Page

Halaman profil tautan resmi (*Link in Bio*) untuk **ION Network**, perusahaan penyedia infrastruktur dan solusi digital terintegrasi di Indonesia yang menghadirkan layanan konektivitas, internet, Data Center & Cloud, serta solusi digital.

---

## 🎨 Design System & Color Palette

Mengusung gaya desain modern *Bento / Frosted Glassmorphism* dengan identitas warna resmi ION Network:

| Peran | Hex Code | Contoh Penggunaan |
| :--- | :--- | :--- |
| **Utama (Primary)** | `#1974d2` | Aksen brand, glow pencahayaan, border highlight, gradient tombol hover, ikon aktif. |
| **Sekunder (Secondary)** | `#212322` | Latar kartu kaca transparan (*frosted glass*), latar kartu tombol tautan. |
| **Tersier (Tertiary)** | `#000000` | Latar belakang dasar (*deep black*), kontras bayangan (*depth shadow*). |
| **Aksen (Accent)** | `#fed809` | Tagline hashtag `#TurnOnYourLife`, badge verifikasi resmi, highlight tombol Info LowKer. |

### Tipografi
* **Font Resmi**: [Inter](https://fonts.google.com/specimen/Inter) (Google Fonts)
* Bobot yang digunakan: 400 (Regular), 500 (Medium), 600 (Semi-bold), 700 (Bold), 800 (Extra-bold).

---

## 🚀 Fitur Utama & Struktur Halaman

1. **Header Profil**:
   * Avatar melingkar dengan border glow `#1974d2` dan badge verifikasi resmi menempel di sudut kanan bawah.
   * Judul **ION Network** dan tagline resmi: `For Better Life #TurnOnYourLife`.
2. **Deskripsi Profil Resmi**:
   * Copywriting representasi brand terkini mengenai ekosistem digital terintegrasi, Fiber Optik nasional, Broadband FTTH, Wholesale, serta Data Center & Cloud.
3. **Kartu Tautan Resmi (Link-in-Bio)**:
   * **Company Profile (PDF)**: Tautan langsung ke dokumen Company Profile resmi 2026.
   * **Website Resmi**: Portal informasi korporat ION Network (`ionnetwork.co.id`).
   * **Info LowKer**: Saluran resmi WhatsApp Channel karir & rekrutmen.
   * **Social Media Channels**: YouTube, LinkedIn, Instagram, Facebook, TikTok.
   * **Lokasi Kantor**: Titik navigasi Google Maps kantor pusat di Ragunan, Jakarta Selatan.
4. **Optimasi SEO & Aksesibilitas**:
   * Open Graph (Facebook, WhatsApp, LinkedIn) & Twitter Cards lengkap untuk pratinjau tautan (*rich link preview*).
   * Schema.org Structured Data (`Organization`) yang terhubung langsung ke Knowledge Graph dan akun media sosial resmi.
   * WCAG compliant touch targets (tinggi tombol $\ge 50\text{px}$) & atribut `aria-label`.
   * Desain ultra-responsif untuk berbagai resolusi layar (Mobile $\le 360\text{px}$, Smartphone, Tablet, hingga Desktop).

---

## 💻 Cara Menjalankan Secara Lokal

Proyek ini dibangun menggunakan HTML, CSS modern, dan didukung server lokal Node.js tanpa dependensi eksternal yang rumit:

```bash
# Clone repository
git clone https://github.com/dmsda/link-bio-ionnetwork.git
cd link-bio-ionnetwork

# Jalankan server lokal
npm start
# atau
node server.js
```

Akses melalui peramban: `http://localhost:3000/`

---

## 📝 Changelog & Riwayat Pembaruan

### [Versi 2.0.0] - Pembaruan Identitas Brand & Redesign Total
- **Pembaruan Teks Deskripsi Profil**:
  - Memperbarui narasi profil perusahaan dari NAP & ISP menjadi penyedia infrastruktur dan solusi digital terintegrasi (Konektivitas, Internet, Data Center & Cloud).
- **Penambahan Tautan Baru**:
  - Menambahkan tombol **Company Profile (PDF)** (`compro-ion-network-2026-juli.pdf.pdf`).
  - Menambahkan tombol saluran karir **Info LowKer** (WhatsApp Channel).
- **Redesign UI & Skema Warna**:
  - Menerapkan palet 4 warna utama: `#1974d2` (Utama), `#212322` (Sekunder), `#000000` (Tersier), dan `#fed809` (Aksen).
  - Standarisasi font resmi ke **Inter**.
  - Mengubah tombol teks polos menjadi komponen kartu modern dengan ikon vektor SVG resmi, sub-keterangan, badge tag, dan panah chevron interaktif.
- **Perbaikan Bug (Bug Fix)**:
  - Memperbaiki posisi badge verifikasi yang sebelumnya meregang ke sisi kanan kartu akibat kontainer block. Ditetapkan batas presisi `92px x 92px` pada kontainer avatar sehingga badge menempel sempurna di lingkar logo.
- **Optimasi SEO & Performa**:
  - Menambahkan meta tag SEO lengkap, Open Graph, Twitter Card, Canonical, dan Schema JSON-LD `Organization`.
  - Mengoptimalkan responsivitas untuk layar kecil ($\le 360\text{px}$) serta safe-area insets untuk perangkat smartphone berponi (*notch*).
