# Murottal 9:16 Maker – Proyek APK Android

Aplikasi ini membungkus file `murottal-916-v16.html` Anda dalam WebView Android.
Fitur HTML tetap sama; tambahan: hasil video/JSON disimpan ke **Download/Murottal**.

## Cara 1 – Tanpa install apa pun (GitHub Actions, paling mudah)
1. Buat repositori baru di github.com, unggah **seluruh isi** folder ini
   (pastikan folder `.github` ikut terunggah).
2. Buka tab **Actions** → workflow **Build APK** → tunggu hijau (±3–5 menit).
3. Buka run tersebut → bagian **Artifacts** → unduh `Murottal-APK` (isinya `app-debug.apk`).
4. Kirim APK ke HP, buka, izinkan "Install dari sumber tidak dikenal".

## Cara 2 – Android Studio
1. Buka folder ini di Android Studio (versi terbaru), tunggu Gradle sync.
2. Menu **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
3. APK ada di `app/build/outputs/apk/debug/app-debug.apk`.

## Catatan
- Butuh internet (API Quran, audio, dan pustaka mp4-muxer/JSZip dimuat dari CDN).
- Mode "Cepat → MP4" memakai WebCodecs; butuh Android System WebView / Chrome terbaru.
- Memilih folder font QCF (`webkitdirectory`) tidak didukung di Android; gunakan opsi ZIP.
- Untuk mengganti HTML: timpa `app/src/main/assets/www/index.html`
  (sisipkan lagi blok `<script>` shim di awal `<head>` bila perlu).
- APK ini bertanda tangan debug (cukup untuk dipasang sendiri, bukan untuk Play Store).
