# Dashboard Pencapaian Area Hasan Basri · 19 Toko

Dashboard statis (1 file `index.html`) untuk **GitHub Pages**, membaca langsung Google Spreadsheet
(tab `Tgl_01` … `Tgl_31` dari template *Monitoring Toko Area Hasan*). Tanpa framework, tanpa server.

## Deploy ke GitHub Pages
1. Upload `index.html` + `README.md` ke root repository (timpa file lama).
2. **Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.**
3. Tunggu ±1 menit, lalu buka link publik. Jika tampilan lama masih muncul, tekan **Ctrl+F5**.

> Spreadsheet wajib **Share → Anyone with the link → Viewer**.

## Yang baru di versi ini
- **Tema poster**: biru navy, aksen kuning-emas & merah, judul miring ala poster, kartu 5 terbawah bergaya poster.
- **Grafik modern vs target**
  - Cincin pencapaian (11 indikator) terhadap target.
  - Batang *Aktual vs Target per Toko* (pilih PSM/SERTIS/PWP/SEGER/CEBAN/NEW MBR/FOKUS 4/MEMBER); bayangan putus-putus = target, warna hijau/kuning/merah menurut %.
  - Tren harian area vs target (area chart) dan Skor Rank bergradasi.
- **Poster otomatis**: tombol **⬇ Download Poster** langsung membuat JPG (1620×2508) seperti contoh: judul, total sales, toko terjelek,
  5 terbawah per indikator (11 kartu), Top 5 ranking, Telepon AC, footer. **👁 Pratinjau Poster** menampilkan dulu + tombol **Bagikan (WA)** di HP.
  Poster mengikuti **Tanggal** dan **Jam** yang dipilih. Tombol 📷 per bagian tetap ada.

## Konfigurasi (`index.html`, blok `CFG`, `STORES`, `IND`)
- `SHEET_ID` · `REFRESH_SEC` (auto refresh, default 30 dtk) · `STORES` (19 toko) · `IND` (target PSM 150, SERTIS 30, PWP 50, SEGER 50, CEBAN 10) · `NM_TARGET` 2 · `MEMBER_TARGET` 70%

## Aturan hitung
- Data harian = jumlah 4 blok jam (10, 15, 19, 23). Skor Rank = jumlah rank 5 indikator (kecil = bagus); seri dipecah total sales.
- Member = Pakai ÷ (Pakai + Tidak). New Member = actual ÷ 2. Fokus 1-3 = Redeem ÷ (Redeem + Lost). Fokus 4 = Aktual ÷ Target.
- Font Montserrat dimuat dari Google Fonts; jika offline otomatis memakai font sistem.
