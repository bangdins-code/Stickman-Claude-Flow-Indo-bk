---
name: stickman-flow-indo
description: Buat video Shorts stickman 2D bahasa Indonesia di Google Flow dengan tokoh tetap Rizur, Pak Bos, Indah: naskah, klip AI konsisten, suara, rakit MP4. Pakai saat diminta video stickman.
---

# Stickman Flow Indo

User cukup mengetik **"Buat video stickman: <topik>"**. Kamu yang mengerjakan semuanya. Bagian user hanya **menyetujui naskah**, **mengirim/menyetujui suara**, dan **melampirkan klip yang terunduh** (kalau kamu tidak bisa membaca folder Download user). Semua komunikasi dengan user memakai Bahasa Indonesia yang santai dan singkat. **Prompt ke Flow selalu berbahasa Inggris**, karena hasilnya lebih stabil.

**Yang dibutuhkan:** Claude in Chrome (user sudah login Google, langganan Google AI Plus/Pro/Ultra dengan akses Flow) dan ffmpeg di workspace.

## Aturan keras
1. **Konsistensi wajah adalah nomor satu.** Setiap tokoh harus terlihat sama persis di semua adegan: bentuk kepala, mata, alis, kumis, kerudung, dan proporsi. Klip yang wajah tokohnya berubah, misalnya menjadi realistis, berbeda bentuk, atau berganti tokoh, **tidak boleh dipakai**. Lihat bagian 3.
2. Jangan pernah mengetik password. Kalau muncul layar login, pembayaran, error, atau "unusual activity", berhenti dan beri tahu user.
3. Kredit Flow terbatas. Sebelum generate, sebutkan biaya dan sisa kredit. Ulang klip **maksimal satu kali** per adegan.
4. Unduh file hanya setelah user mengizinkan.
5. Karakter dan cerita selalu orisinal. Jangan meniru karakter atau channel orang lain.

---

## 0. Pemeran tetap (TERKUNCI)

| Tokoh | Peran | Character di Flow |
|---|---|---|
| **Rizur** (laki-laki) | Pegawai polos yang sering apes, gampang panik | `Rizur` |
| **Pak Bos** (laki-laki) | Atasan sombong, santai, suka menyeringai | `PakBos` |
| **Indah** (perempuan) | Rekan kerja Rizur, cerdas, jahil, selalu memegang HP | `Indah` |

Gambar master ada di folder `karakter/` (`rizur.png`, `pakbos.png`, `indah.png`).

Deskripsi berikut ditempel **apa adanya** di prompt. Jangan diparafrasekan.
```
RIZUR: a simple hand-drawn stick figure man with a perfectly round pure paper-white head, two big expressive cartoon eyes with black pupils, thick expressive black eyebrows, thin black line arms and legs, small black hands. Default outfit: white long-sleeve office shirt, navy tie, black trousers, brown shoes, ID card lanyard.
PAK BOS: a simple hand-drawn stick figure man with a perfectly round pure paper-white head, simple flat cartoon face, big cartoon eyes with half-closed smug eyelids, thick black eyebrows, a small black moustache, slightly round belly, thin black line arms and legs. Default outfit: brown batik long-sleeve shirt, dark grey trousers, black shoes.
INDAH: a simple hand-drawn stick figure woman with a perfectly round pure paper-white face, two big expressive cartoon eyes with small eyelashes, thick black eyebrows, a simple pastel pink hijab, thin black line arms and legs, small black hands. Default outfit: mint green long-sleeve tunic blouse, long dark navy skirt, black flat shoes, smartphone.
```
Pakaian boleh diganti sesuai cerita, dengan menulis pakaian baru setelah deskripsi. Wajah, kepala, dan tubuh **tidak boleh** berubah.

**STYLE LINE** (akhiri setiap prompt dengan baris ini):
```
Hand-drawn ink cartoon, thick black outlines, flat soft colours, detailed warm painted background, soft cinematic light, exaggerated comedic expressions, vertical 9:16. All characters keep their exact simple flat cartoon faces from the references for the entire clip, never realistic, shaded or detailed human faces. The heads are pure paper-white, not skin coloured. Simple anatomy: one head, two arms, two legs per person. No text, no words, no letters, no subtitles, no logos.
```

### Lokasi tetap (ditempel sebagai teks, tanpa biaya kredit)
- **Kantor Pak Bos / ruang kantor**: `Indonesian government office: wooden desks, green filing cabinets, a wall clock without numbers, a ceiling fan, warm light.`
- **Rumah Rizur**: `simple Indonesian living room: brown sofa, old CRT television, cream walls, a small window with curtains.`
- **Jalan depan kantor**: `street in front of an Indonesian office: sidewalk, parked motorbikes, a small coffee stall, morning light.`

Lokasi lain bebas mengikuti cerita, tetap dengan STYLE LINE yang sama.

### Persiapan pertama kali (akun Flow baru)
Buka `https://flow.google.com` → **Project baru** → menu **Karakter** → **Karakter baru**. Untuk setiap tokoh:
1. Klik `+` atau **Upload**, lalu unggah `karakter/<nama>.png` dari folder skill. Ini cara paling konsisten. Kalau upload tidak bisa, ketik deskripsi terkunci + `Full body, front view, standing, plain cream background.` + STYLE LINE dengan model Nano Banana. Pembuatan karakter **gratis**.
2. Beri nama persis `Rizur`, `PakBos`, `Indah`. Isi **Info karakter** dengan sifat dan ciri tetap tokoh itu.
3. Klik **Selesai**. Langkah ini hanya dilakukan sekali.

---

## 1. Naskah = shot list (tunjukkan, lalu tunggu persetujuan)
- 3–6 adegan, 20–45 detik, dengan struktur: **hook di 0–2 detik** → konflik → eskalasi → **punchline/twist**.
- Dialog bahasa Indonesia sehari-hari, pendek, dan lucu (maksimal sekitar 6 detik ucapan per adegan).
- Maksimal **3 tokoh per adegan**, karena itu batas referensi yang bisa dijaga konsisten.
- Tampilkan sebagai tabel: **No | Tokoh & pakaian | Shot & gerakan kamera | Aksi & ekspresi | Dialog**.
- Sebutkan perkiraan kredit: jumlah adegan × biaya per klip.
- Tunggu user menjawab "oke".

## 2. Standar sinematografi (wajib)
- Variasi shot: close-up untuk reaksi, medium untuk dialog, over-the-shoulder untuk ketegangan, low angle untuk tokoh yang berkuasa, high angle untuk tokoh yang apes. **Dua adegan berurutan tidak boleh memakai shot yang sama.**
- Satu gerakan kamera per klip: push-in saat tegang, whip pan untuk kejutan, kamera goyang saat panik.
- Komposisi Shorts: wajah dan aksi di tengah sampai sepertiga atas layar. Bagian bawah dan kanan layar adalah zona tombol YouTube.
- Cahaya mengikuti emosi: hangat untuk komedi, lampu sorot untuk tegang, kebiruan untuk sedih.

## 3. Klip di Flow + PROTOKOL KONSISTENSI
**Pengaturan:** di kotak prompt, buka pengaturan → **Video**, **Bahan** (ingredients), **9:16**, model **Veo 3.1 - Lite** (paling hemat, sekitar 10 kredit per klip 8 detik; cek angka di panel), dan **x1**.

**Memasang tokoh:** di kotak prompt, ketik `@` + nama tokoh, pilih tokohnya, lalu klik **Tambahkan ke perintah**. Ulangi untuk **setiap tokoh yang terlihat** di adegan. Tokoh yang muncul tanpa referensi pasti akan berubah wajah.

**Cara paling konsisten (gunakan untuk close-up dan adegan penting):**
1. Buat dulu **gambar awal** adegan dengan mode **Gambar** (gratis), memakai referensi tokoh + prompt adegan.
2. Periksa wajah di gambar itu. Kalau berbeda dari master, buat ulang (tetap gratis).
3. Gunakan gambar itu sebagai **Frame awal** (mode **Frame**), lalu buat videonya. Video yang berangkat dari gambar yang sudah benar jauh lebih konsisten.

**Hindari pemicu perubahan wajah:**
- Tokoh menoleh dari belakang ke depan, atau berputar kepala dengan drastis.
- Close-up ekstrem tanpa frame awal (terutama Pak Bos).
- Terlalu banyak aksi dalam satu klip. Gunakan satu aksi sederhana per klip.
- Kata-kata seperti "realistic", "detailed face", atau "3D".

**Pemeriksaan wajib setiap klip:** buka klip, lalu lihat frame di detik ±1, ±4, dan ±7 (zoom pratinjau). Bandingkan dengan gambar master: bentuk kepala, mata, alis, kumis, kerudung, pakaian, dan **tokoh yang benar melakukan aksi yang benar**.
- Lolos: lanjut.
- Gagal di sebagian klip: tandai bagian yang bagus, lalu buang bagian yang berubah saat perakitan.
- Gagal total: ulang sekali dengan prompt yang lebih tegas atau dengan cara frame awal. Kalau masih gagal, beri tahu user dan susun ulang adegan dari potongan yang bagus.

**Unduh:** setelah user mengizinkan, buka klip → ikon unduh → **720p (Ukuran asli)**. File masuk ke folder Download user. Kalau kamu tidak bisa membaca folder itu, minta user melampirkan file-nya di chat.

## 4. Suara bahasa Indonesia
- Dialog bahasa Indonesia ditulis di prompt. Flow bisa saja menghasilkan suara, tapi **hasil audionya belum pasti**.
- Minta user mendengarkan. Kalau suaranya jelas dan berbahasa Indonesia, pakai suara asli Flow. Kalau tidak, matikan suara klip lalu minta rekaman atau TTS per baris dengan format:
```
S01 | PAK BOS | "Rizur... jam berapa ini?"
S02 | RIZUR   | "Maaf Pak! Macet parah, motor mogok, terus ban kempes!"
```
- Gunakan satu suara khas per tokoh: Rizur tinggi dan panik, Pak Bos berat dan santai, Indah ceria dan jahil.

## 5. Rakit (ffmpeg)
1. Potong setiap klip hanya pada bagian yang **lolos pemeriksaan konsistensi**. Durasi adegan = dialog + 0,3–0,5 detik.
2. Urutkan, lalu gunakan potongan langsung atau dissolve 0,2 detik. Untuk punchline, tambahkan zoom cepat ke wajah (`zoompan`) dan boleh tambahkan goyangan singkat.
3. Caption besar bahasa Indonesia: putih dengan outline hitam tebal, 2–4 kata per tampilan, **kata kunci berwarna kuning**, posisi di atas zona tombol YouTube (sekitar 70% tinggi layar).
4. Audio: pakai suara Flow atau rekaman user, tanpa tumpang tindih. Musik dan efek suara hanya dipakai kalau user menyediakan file.
5. Ekspor ke 1080x1920, 30 fps, H.264 (`-preset veryfast -crf 20`) dan AAC.

## 6. Cek akhir sebelum dikirim
- Buat lembar frame: `ffmpeg -i final.mp4 -vf fps=2,scale=200:-1,tile=8x4 sheet.png`. Lihat setiap frame: **tidak boleh ada wajah yang berubah**, kepala selalu putih, tidak ada tulisan aneh, dan caption terbaca.
- Pastikan hook kuat di 2 detik pertama, ada variasi shot, dan dialog tidak terpotong.

## 7. Laporan
Kirim `final.mp4`, lalu tulis singkat: durasi, kredit yang terpakai dan sisa, satu saran judul, dan satu saran caption Shorts. Kalau ada pakaian, lokasi, atau tokoh baru yang disukai user, tawarkan untuk menambahkannya ke bagian 0.
