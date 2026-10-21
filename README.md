# n8n Video Generator by Telegram

Workflow n8n untuk membuat prompt video promosi menggunakan AI berdasarkan pesan atau foto yang dikirim melalui Telegram, lalu mengirimkan hasil video kembali ke Telegram.

## Alur Workflow

1. Pengguna mengirim pesan atau foto melalui Telegram.
2. `Telegram Trigger` menerima pesan tersebut.
3. `AI Agent` mengubah ide promosi menjadi prompt video sinematik berdurasi 5 detik.
4. `OpenRouter Chat Model` memproses prompt menggunakan model AI.
5. `HTTP Request` mengirim prompt ke API fal.ai.
6. `Send a video` mengirim hasil video kembali ke chat Telegram.

## Kebutuhan

- n8n versi yang mendukung node AI Agent dan OpenRouter Chat Model
- Bot Telegram dan token bot
- Credential Telegram API di n8n
- Credential OpenRouter API di n8n
- Credential HTTP Header Auth untuk API fal.ai
- Akses API ke OpenRouter dan fal.ai

## Cara Import

1. Buka n8n.
2. Pilih **Import from File**.
3. Pilih file `n8n video generator by Telegram.json`.
4. Buka setiap node yang membutuhkan credential.
5. Pilih atau buat credential yang sesuai.
6. Simpan workflow.
7. Aktifkan workflow setelah pengujian berhasil.

## Konfigurasi Credential

Workflow menggunakan tiga jenis credential:

- **Telegram API** untuk menerima pesan dan mengirim video.
- **OpenRouter API** untuk menjalankan model AI.
- **HTTP Header Auth** untuk autentikasi API fal.ai.

Token dan API key tidak disimpan langsung di file workflow. Credential harus dikonfigurasi melalui menu Credentials di n8n.

## Catatan Penggunaan

- Prompt video dibuat dalam bahasa Inggris untuk instruksi visual dan teknis.
- Dialog, voice-over, dan teks di layar diarahkan menggunakan Bahasa Indonesia.
- Durasi video ditetapkan tepat 5 detik.
- Workflow saat ini mengharapkan input teks Telegram dan referensi foto jika tersedia.
- Pastikan endpoint dan format respons API fal.ai sesuai dengan konfigurasi workflow yang digunakan.

## Keamanan

Jangan commit atau membagikan file berikut ke repository publik:

- Token Telegram
- API key OpenRouter atau fal.ai
- File `.env`
- Export credential n8n
- Database atau backup n8n
- Data execution yang berisi pesan pengguna atau file pribadi

Gunakan `.gitignore` untuk mencegah file sensitif ikut ter-push.

## Lisensi

Tambahkan lisensi yang sesuai sebelum mendistribusikan workflow ini secara publik.
# n8n-Video-Promotion-Generator
