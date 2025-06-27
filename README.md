# eas-javala

LINK WEB : https://naufalhumam24.github.io/eas-javala/

# JAVALA — Pelestarian Cerita Rakyat Nusantara melalui Translasi dan TTS Bahasa Jawa

JAVALA adalah aplikasi web edukatif yang bertujuan melestarikan cerita rakyat Indonesia dengan menerjemahkannya ke dalam Bahasa Jawa dan mengubahnya menjadi suara (Text-to-Speech). Proyek ini menggabungkan **Frontend Web**, **Backend NLP**, dan **Teknologi TTS Bahasa Jawa**.

## 📌 Fitur Utama

- 🌍 Translasi otomatis cerita rakyat dari Bahasa Indonesia ke Bahasa Jawa menggunakan model NLP.
- 🔊 Pembacaan otomatis hasil cerita menggunakan TTS (Text-to-Speech) Bahasa Jawa.
- 🖼️ Antarmuka web interaktif yang menampilkan cerita dan audio.
- 📖 Halaman khusus untuk tiap cerita rakyat.
- 📁 Sistem modular untuk menambahkan cerita baru secara mudah.

---

## 🖥️ Teknologi yang Digunakan

### Frontend
- HTML5, CSS3, JavaScript (Vanilla)
- Responsive Web Design
- Gradio UI (opsional untuk integrasi demo AI)

### Backend (NLP & TTS)
- Python + FastAPI
- Translasi Bahasa Indonesia → Bahasa Jawa menggunakan model fine-tuned MarianMT atau IndoNLG.
- TTS Bahasa Jawa menggunakan model Facebook `facebook/mms-tts-ind` atau `Coqui TTS` fine-tuned untuk Bahasa Jawa.
- Hugging Face Transformers, Coqui TTS, Torch

---

## 📁 Struktur Proyek

```

eas-javala/
├── frontend/
│   ├── index.html
│   ├── cerita.html
│   ├── tentang.html
│   ├── style.css
│   └── script.js
│
├── backend/
│   ├── app.py               # API server 
│   ├── translator.py        # Modul translasi Indo → Jawa
│   ├── tts\_engine.py        # Modul TTS Bahasa Jawa
│   ├── models/
│   │   ├── tts\_model/       # Model TTS (jika lokal)
│   │   └── translator/      # Model translasi (jika lokal)
│   └── requirements.txt     # Dependency Python
│
└── README.md

---



## 📡 Endpoint API

| Endpoint     | Method | Fungsi                                     |
| ------------ | ------ | ------------------------------------------ |
| `/translate` | POST   | Menerjemahkan teks Indo → Jawa             |
| `/tts`       | POST   | Mengubah teks Bahasa Jawa jadi audio (WAV) |
| `/cerita`    | GET    | Mengambil daftar cerita (jika di-database) |

Contoh payload:

```json
POST /translate
{
  "text": "Pada zaman dahulu ada seekor harimau..."
}
```

---

## 📚 Contoh Studi Kasus

* Cerita rakyat *Timun Mas* diterjemahkan otomatis ke Bahasa Jawa dan disuarakan sebagai audio agar anak-anak atau peneliti budaya bisa mendengarkan versi lokal.
* Edukasi interaktif untuk sekolah dasar mengenai kearifan lokal dengan bantuan AI.

---

## 🔮 Pengembangan Selanjutnya

* Penambahan pilihan dialek Bahasa Jawa (Ngoko, Krama, dll).
* Deteksi otomatis Bahasa Indonesia pada input.
* Fitur bookmark & favoriting cerita favorit.
* Deploy ke Hugging Face Spaces untuk demo publik.

---
