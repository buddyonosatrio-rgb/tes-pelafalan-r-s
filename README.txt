WEBSITE TES PELAFALAN R & S DENGAN ANALISIS AUDIO AI

PENTING: Ini prototipe skrining awal, bukan alat diagnosis klinis. Model AI umum tidak dijamin akurat untuk menilai gangguan artikulasi. Hasil harus dikonfirmasi terapis wicara bila ada kekhawatiran.

CARA DEPLOY UNTUK PEMULA
1. Buat akun/login di https://app.netlify.com/ dan https://platform.openai.com/.
2. Buat API key di OpenAI API platform. API usage ditagih terpisah dari langganan ChatGPT; mungkin perlu menambahkan metode pembayaran/kredit. Periksa harga sebelum digunakan.
3. Jangan pernah menulis API key di index.html atau membagikannya. Simpan hanya di Netlify environment variables.
4. Upload project ini ke GitHub sebagai repository baru (semua isi ZIP diekstrak ke root repository), lalu di Netlify pilih Add new site > Import an existing project dan hubungkan repository tersebut.
5. Di Netlify: Site configuration > Environment variables, tambahkan key bernama OPENAI_API_KEY dengan value API key milikmu. Simpan lalu trigger deploy ulang.
6. Buka URL situs Netlify, izinkan mikrofon, rekam kalimat, lalu tekan Selesai & analisis.

CATATAN TEKNIS
- Fungsi server Netlify mengirim WAV ke endpoint Chat Completions dengan model audio gpt-audio-mini. Dukungan model/parameter dapat berubah; jika API mengembalikan error model/format, cek dokumentasi OpenAI API terkini dan sesuaikan model/endpoint.
- Penggunaan API dapat menimbulkan biaya. Set batas penggunaan di dashboard API jika tersedia.
- Audio dikirim ke layanan AI untuk analisis. Minta persetujuan pengguna sebelum merekam/mengirim audio, terutama anak-anak.
- Jangan gunakan hasil untuk keputusan klinis atau menyatakan seseorang “cadel” sebagai diagnosis.
