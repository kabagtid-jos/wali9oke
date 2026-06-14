CARA PASANG DI GITHUB + VERCEL

1. Upload SEMUA file di folder ini ke ROOT repository GitHub, bukan di dalam folder lain.
   Struktur yang benar:
   /index.html
   /manifest.webmanifest
   /sw.js
   /pwa-icon.svg
   /vercel.json

2. Di Vercel:
   - Framework Preset: Other
   - Build Command: kosongkan
   - Output Directory: kosongkan atau isi titik: .
   - Root Directory: pilih folder yang berisi index.html. Jika index.html ada di root repo, biarkan default.

3. Deploy ulang.

4. Jika sebelumnya sudah install PWA dan masih tampil 404:
   - Uninstall aplikasi PWA lama.
   - Buka browser biasa ke https://domain-vercel-anda/
   - Tekan Ctrl + F5.
   - Install ulang PWA.

PENYEBAB 404:
Biasanya file HTML tidak bernama index.html, tidak berada di root project, atau Vercel membaca folder yang salah. File vercel.json di paket ini juga menambahkan rewrite agar route PWA selalu diarahkan ke index.html.
