# backend-api
Created by :
1. Azam Azri Ahmad - Universitas Ahmad Dahlan

# 🌐 HiTeman Backend API

**HiTeman API** adalah backend RESTful API berbasis **FastAPI** yang melayani permintaan pengguna untuk menghasilkan narasi dan audio (Text-to-Speech) secara otomatis.

API ini mengintegrasikan modul `HiTeman TTS` untuk menghasilkan narasi menggunakan **Gemini 1.5 Flash** dan audio menggunakan **TTS Native Gemini (gemini-2.5-flash-preview-tts)**.

---

## 🧰 Teknologi yang Digunakan

- **FastAPI** — Framework web berbasis Python.
- **Gemini 1.5 Flash** — untuk generate teks/narasi otomatis.
- **TTS Native Gemini (gemini-2.5-flash-preview-tts)** — untuk mengonversi teks ke audio.
- **Uvicorn** — server asynchronous untuk menjalankan FastAPI.

---

## 🚀 Fitur

- `POST /generate` — Endpoint untuk menghasilkan narasi dan audio dari prompt pengguna.
- 🔁 Integrasi penuh dengan `hitemanTTS`.
- 🧾 Dokumentasi API otomatis via Swagger.
- ⚙️ Logging dan struktur modular.
- Ngrok (Free Tier) Untuk expose API secara publik.

---

## 📦 Endpoint API

### `GET /`
Memeriksa status API HiTeman.
- **Response:** `"API HiTeman berjalan dengan baik."`

### `POST /generate_therapy_audio`
Menghasilkan audio terapi berdasarkan input label emosi.
- **Request JSON:**
```json
{
  "emotion": "stress"
}
```
- **Response:** File audio terapi `.wav` untuk diunduh.

## 📌 Cara Menjalankan Lokal
```bash
uvicorn main:app --reload
```

## 🛠️ Deployment
Layanan ini dideploy menggunakan **Ngrok Free Tier** untuk testing.
Contoh URL:
```
https://3f9f-35-201-146-89.ngrok-free.app
```

## 📄 Dokumentasi Swagger
Akses dokumentasi interaktif:
```
https://3f9f-35-201-146-89.ngrok-free.app/docs
```

## 📦 Requirements

- Python ≥ 3.9
- `fastapi`
- `uvicorn`
- `openai` (untuk akses Gemini)
- `pydantic`



## 🔐 Konfigurasi API Key

Pastikan Anda menyertakan API key Gemini di variabel lingkungan atau langsung dalam kode.

---

## 🤝 Integrasi

Gunakan endpoint ini sebagai backend dari aplikasi web atau chatbot Anda. Untuk generate narasi & audio, backend ini akan memanggil `hitemanTTS`.

---

## 📄 Lisensi

MIT License © HiTeman Dev

