# Siaga Api — Dashboard Hotspot Kebakaran Indonesia

Aplikasi dashboard berbasis Python, Streamlit, Folium, dan Plotly untuk mengeksplorasi deteksi hotspot di Indonesia.

## Isi paket
- `app.py` — entrypoint aplikasi Streamlit.
- `requirements.txt` — dependensi yang dikenali Streamlit Community Cloud.

## Deploy ke Streamlit Community Cloud
1. Ekstrak ZIP ini.
2. Unggah kedua file (`app.py` dan `requirements.txt`) ke sebuah repository GitHub.
3. Buka https://share.streamlit.io/ dan masuk dengan akun yang memiliki akses ke repository tersebut.
4. Pilih **Create app** / **Deploy an app**, pilih repository dan branch, lalu set **Main file path** ke `app.py`.
5. Klik **Deploy** dan tunggu proses instalasi dependensi selesai.

## Menjalankan di komputer lokal
```bash
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows PowerShell: .venv\\Scripts\\Activate.ps1
pip install -r requirements.txt
streamlit run app.py
```

## Menggunakan data hotspot
- Secara default dashboard memakai data sintetis untuk demo. Data ini **bukan data hotspot aktual**.
- Pilih **NASA FIRMS API** dan masukkan MAP_KEY pada sidebar untuk mengambil data aktual, atau pilih **Impor CSV** untuk memuat data FIRMS.
- Jangan menyimpan MAP_KEY pribadi ke repository publik. Aplikasi memakai input MAP_KEY saat sesi dan tidak menuliskannya ke source code.
- Peta dasar dan sumber data eksternal memerlukan koneksi internet.

## Batasan
- Klasifikasi wilayah merupakan perkiraan geografis, bukan agregasi batas administratif resmi.
- Deteksi hotspot satelit bukan konfirmasi otomatis terjadinya kebakaran. Verifikasi sumber resmi/lapangan tetap diperlukan.
