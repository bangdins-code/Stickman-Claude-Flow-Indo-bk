<div align="center">

# 🎬 Stickman Flow Indo

**Satu kalimat masuk, satu video Shorts stickman berbahasa Indonesia keluar.**

Skill Claude untuk membuat video komedi stickman 2D bergaya ilustrasi di **Google Flow**: naskah, klip AI dengan tokoh yang konsisten, suara bahasa Indonesia, lalu dirakit menjadi MP4 vertikal siap upload.

<img src="assets/pemeran.png" width="90%">

<sub>Pemeran tetap: Rizur, Pak Bos, dan Indah</sub>

<img src="assets/contoh-video.gif" width="240">

<sub>Contoh hasil: "Telat Ngantor" (video uji)</sub>

</div>

---

## 👥 Kenalan dengan pemeran

| | Tokoh | Sifat |
|---|---|---|
| <img src="skills/stickman-flow-indo/karakter/rizur.png" width="120"> | **Rizur** | Pegawai polos yang baik hati tapi selalu apes. Gampang panik, reaksinya heboh. |
| <img src="skills/stickman-flow-indo/karakter/pakbos.png" width="120"> | **Pak Bos** | Atasan yang sombong dan santai. Suka menyeringai dan bertolak pinggang. |
| <img src="skills/stickman-flow-indo/karakter/indah.png" width="120"> | **Indah** | Rekan kerja Rizur yang cerdas dan jahil. Selalu memegang HP dan hobi menggosip. |

Pakaian tokoh bisa berganti sesuai cerita (seragam, baju adat, kostum zaman kerajaan, dll.), tapi **wajah dan bentuk tubuhnya selalu sama**.

---

## ✨ Hasil yang didapat

Anda cukup mengetik:

```
Buat video stickman: pegawai telat ngantor gara-gara macet
```

Lalu Claude akan:

| No | Langkah | Siapa |
|---|---|---|
| 1 | Menulis naskah dan shot list (angle kamera, ekspresi, dialog) | Claude |
| 2 | Menyetujui naskah | **Anda** |
| 3 | Membuat klip satu per satu di Google Flow lewat Chrome Anda, lalu memeriksa konsistensi wajah setiap klip | Claude |
| 4 | Mendengarkan suara dari Flow, atau mengirim rekaman/TTS bahasa Indonesia | **Anda** |
| 5 | Memotong, menambahkan caption, zoom punchline, dan ekspor MP4 1080x1920 | Claude |

---

## 🧰 Yang dibutuhkan

- **Akun Claude** dengan fitur Skills aktif (paket Pro, Max, Team, atau Enterprise).
- **Langganan Google AI** (Plus, Pro, atau Ultra) untuk mengakses **Google Flow**.
- Ekstensi **Claude in Chrome** terpasang di Chrome, dengan Anda sudah login Google.
- (Opsional) Aplikasi untuk merekam suara atau TTS, misalnya CapCut atau ElevenLabs.

---

## 📥 Cara memasang skill (sekali saja)

1. Buka halaman **[Releases](../../releases)** di repo ini, lalu unduh file **`stickman-flow-indo.zip`**. Jangan diekstrak.
2. Di Claude, buka **Settings → Capabilities**, lalu pastikan **Code execution and file creation** aktif.
3. Buka **Customize → Skills**, klik **+**, pilih **Create skill**, lalu **Upload a skill**.
4. Pilih file `stickman-flow-indo.zip`, lalu tunggu sampai skill muncul di daftar dalam keadaan aktif.

> Kalau tidak ada halaman Releases, pakai file `stickman-flow-indo.zip` yang ada di folder utama repo ini.

---

## ▶️ Cara memakai

1. Buka Chrome dan pastikan Anda sudah login Google dan bisa membuka [Google Flow](https://flow.google.com).
2. Di percakapan baru Claude, ketik: **`Buat video stickman: <ide cerita Anda>`**
3. **Pemakaian pertama**: Claude otomatis menyiapkan Rizur, Pak Bos, dan Indah di akun Flow Anda (menu *Karakter*). Langkah ini **tidak memakai kredit**.
4. Baca naskah yang ditawarkan, lalu jawab **"oke"** atau minta revisi.
5. Claude membuat klip di Flow dan melaporkan kredit yang terpakai.
6. Izinkan Claude mengunduh klip. Kalau diminta, lampirkan file dari folder Download ke chat.
7. Urus suara: dengarkan suara bawaan Flow, atau kirim rekaman per baris sesuai naskah.
8. Terima **MP4 final** yang siap diunggah ke YouTube Shorts, TikTok, atau Reels.

### Contoh perintah lain
- `Buat video stickman: Rizur disuruh lembur pas malam minggu`
- `Buat video stickman: Indah bikin grup gosip kantor, ternyata Pak Bos ikut di dalamnya`
- `Buat video stickman: Rizur jadi prajurit Majapahit yang salah bawa senjata`

---

## 🎥 Standar kualitas yang dijaga skill

- **Konsistensi wajah**: setiap klip diperiksa di beberapa titik. Klip yang wajah tokohnya berubah tidak dipakai.
- **Variasi angle kamera**: close-up, medium, over-the-shoulder, low/high angle. Dua adegan berurutan tidak memakai shot yang sama.
- **Hook di 2 detik pertama** dan punchline dengan zoom cepat.
- **Caption besar** bahasa Indonesia dengan kata kunci berwarna kuning, di luar zona tombol YouTube.
- **Format vertikal** 9:16, 1080x1920.

---

## 💳 Soal kredit Google Flow

- Membuat **karakter dan gambar**: gratis.
- Membuat **klip video** dengan Veo 3.1 Lite (8 detik, 9:16): sekitar **10 kredit per klip**. Angka pastinya tampil di panel Flow sebelum generate.
- Satu video 3 adegan butuh sekitar **30 kredit**. Paket Google AI Plus mendapat 200 kredit per bulan.
- Klip yang gagal diulang maksimal satu kali. Selebihnya diperbaiki saat perakitan supaya kredit hemat.

---

## ❓ Tanya jawab

**Kenapa prompt ke Flow berbahasa Inggris?**
AI video Google lebih patuh dan lebih stabil dengan prompt bahasa Inggris. Anda tidak perlu menulisnya, karena Claude yang menyusunnya. Naskah, dialog, dan caption tetap bahasa Indonesia.

**Apakah suara Flow pasti berbahasa Indonesia?**
Belum tentu, karena fitur suara Flow masih berkembang. Kalau hasilnya kurang jelas, Anda bisa merekam suara sendiri atau memakai TTS. Skill ini mendukung keduanya.

**Bisa menambah tokoh atau pakaian baru?**
Bisa. Minta saja ke Claude, lalu simpan ke skill lewat pembaruan skill. Supaya konsisten, usahakan maksimal 3 tokoh dalam satu adegan.

**Wajah tokoh kadang berubah, kenapa?**
Itu keterbatasan AI video, terutama saat close-up atau tokoh menoleh drastis. Skill ini memakai cara "gambar awal dulu, baru video" dan pemeriksaan per klip untuk mencegahnya.

---

## 📁 Isi repo

```
stickman-flow-indo/
├── README.md                    ← halaman ini
├── stickman-flow-indo.zip       ← skill siap pasang
├── assets/
│   ├── pemeran.png              ← gambar pemeran untuk README
│   └── contoh-video.gif         ← cuplikan contoh video
└── skills/stickman-flow-indo/
    ├── SKILL.md                 ← instruksi lengkap yang diikuti Claude
    └── karakter/
        ├── rizur.png
        ├── pakbos.png
        └── indah.png
```

---

## 📜 Lisensi

MIT. Silakan dipakai, dimodifikasi, dan dibagikan.

Alur kerja terinspirasi dari [stickman-director](https://github.com/rocketmandrey/stickman-director) (MIT).
