# Paper Collage Studio — versi Streamlit

## Deploy ke Streamlit Community Cloud
1. Upload isi folder ini ke repo GitHub (app.py, paper_collage.py, requirements.txt, .streamlit/, assets/).
2. https://share.streamlit.io → *New app* → pilih repo → Main file: `app.py` → Deploy.
3. Selesai. ffmpeg ikut terpasang lewat paket `imageio-ffmpeg` (tidak perlu packages.txt).

## Jalankan di komputer sendiri
    pip install -r requirements.txt
    streamlit run app.py
Untuk membuka 2K/4K: set `PCS_MAX_RES=4K` (Windows: `set PCS_MAX_RES=4K`) sebelum `streamlit run`.

## Batasan di cloud gratis
- CPU/RAM bersama dan tanpa GPU: pakai HD/FHD, video 30–60 detik. 4K tidak realistis.
- Render berjalan selama sesi browser terbuka; jangan tutup tab / ubah isian saat berjalan.
- Hasil tidak disimpan permanen: unduh MP4 setelah selesai.
- API naskah menghitung limit per IP; IP server cloud bisa dipakai bersama banyak aplikasi, jadi sesekali kena 429/503 (otomatis di-retry).
- Voice-over (edge-tts) dan foto Wikipedia butuh internet keluar; bila diblokir, video tetap jadi tanpa itu.
- Font bawaan: Anton, Archivo Black, Poppins (lisensi OFL). Emoji diambil dari OpenMoji (CC BY-SA 4.0), kreditnya otomatis ada di file .txt.
