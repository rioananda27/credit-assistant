# CREDIT ASSISTANT
### AI Agent Skills untuk Membantu Administrasi Pengajuan Kredit Bank

**Studi kasus:** Magang di bank, bagian kredit  
**Tujuan:** Membantu petugas kredit menjalankan pekerjaan administratif dan analisis awal secara lebih cepat, terstruktur, dan konsisten.

> CREDIT ASSISTANT adalah alat bantu kerja. Sistem ini tidak menggantikan petugas bank, tidak memberikan keputusan persetujuan/penolakan kredit, dan tidak boleh menjadi satu-satunya dasar penilaian kelayakan calon debitur.

## 1. Latar Belakang
Bagian kredit bank menangani berbagai pekerjaan, seperti menerima berkas pengajuan, memeriksa kelengkapan dokumen, memasukkan data, menghitung estimasi angsuran, menjawab pertanyaan umum, dan menyusun rekap administrasi. Sebagian pekerjaan tersebut berulang dan mengikuti format tertentu.

CREDIT ASSISTANT dirancang untuk membantu pekerjaan administratif tersebut. Pemeriksaan yang membutuhkan validasi sumber resmi, penilaian risiko, verifikasi lapangan, serta keputusan kredit tetap dilakukan oleh petugas yang berwenang sesuai kebijakan bank.

## 2. Tujuan
1. Membantu pemeriksaan awal kelengkapan dokumen.
2. Mengekstrak dan merapikan data yang diberikan pengguna.
3. Menghitung estimasi angsuran berdasarkan asumsi yang dinyatakan secara jelas.
4. Menjawab pertanyaan umum tentang alur dan persyaratan kredit berdasarkan informasi yang tersedia.
5. Membuat rekap dan laporan administrasi pengajuan.

## 3. Identifikasi Jobdesk dan Aktivitas Repetitif

| No. | Jobdesk bagian kredit | Aktivitas berulang | Dukungan AI Agent |
|---|---|---|---|
| 1 | Menerima berkas pengajuan | Memeriksa daftar dokumen satu per satu | Checklist kelengkapan |
| 2 | Memeriksa dokumen | Mencatat dokumen tersedia/tidak tersedia | Ringkasan hasil pemeriksaan |
| 3 | Input data nasabah | Menyalin nama, tanggal, nominal, dan informasi lain | Ekstraksi data dari teks/dokumen yang diberikan |
| 4 | Menghitung angsuran | Menghitung cicilan berdasarkan pokok, bunga, dan tenor | Kalkulator estimasi angsuran |
| 5 | Melayani pertanyaan | Menjawab pertanyaan yang sering diajukan | Asisten informasi kredit |
| 6 | Membuat rekap | Menggabungkan status beberapa pengajuan | Rekap tabel |
| 7 | Menyusun laporan | Menulis ringkasan administrasi | Pembuat laporan |

## 4. Fitur
- **Document Checker:** mencocokkan dokumen yang disebutkan pengguna dengan checklist yang diberikan.
- **Customer Data Extractor:** menyusun data yang tersedia menjadi format terstruktur dan menandai bagian yang belum diketahui.
- **Installment Calculator:** menghitung simulasi angsuran dengan metode yang dipilih dan menjelaskan asumsi.
- **Credit Information Assistant:** menjawab pertanyaan umum hanya berdasarkan kebijakan/produk yang disediakan atau informasi yang telah diverifikasi.
- **Report Generator:** membuat ringkasan administrasi tanpa mengarang data.

## 5. Struktur Repository
```text
CREDIT-ASSISTANT/
├── README.md
├── LICENSE
├── .gitignore
├── skills/
│   └── credit-assistant/
│       └── SKILL.md
├── examples/
│   ├── contoh-pemeriksaan-dokumen.md
│   ├── contoh-simulasi-angsuran.md
│   └── contoh-laporan.md
└── tests/
    └── test-cases.md
```

## 6. Cara Menggunakan
1. Buka file `skills/credit-assistant/SKILL.md`.
2. Salin instruksi skill ke konfigurasi AI Agent/platform yang digunakan, atau unggah file tersebut jika platform mendukung file skill.
3. Berikan tugas yang jelas, misalnya: "Periksa kelengkapan dokumen berdasarkan checklist berikut".
4. Berikan data contoh/fiktif untuk pengujian.
5. Periksa kembali hasil AI sebelum digunakan dalam pekerjaan nyata.

## 7. Batasan dan Keamanan
- Gunakan data dummy untuk demonstrasi praktikum.
- Jangan memasukkan NIK, nomor rekening, alamat lengkap, nomor telepon, slip gaji, atau dokumen identitas nasabah nyata ke layanan AI publik.
- Jangan meminta atau menyimpan PIN, password, OTP, CVV, atau kredensial perbankan.
- AI tidak memverifikasi keaslian dokumen hanya dari teks/gambar yang diberikan.
- AI tidak melakukan BI Checking/SLIK, akses rekening, pemeriksaan blacklist, atau verifikasi identitas ke sistem bank.
- AI tidak menetapkan skor kredit atau menyetujui/menolak pinjaman.
- Persyaratan, bunga, biaya, tenor, dan kebijakan produk harus berasal dari dokumen resmi bank yang berlaku. Jika tidak tersedia, AI wajib menyatakan belum memiliki informasi.
- Hasil perhitungan merupakan simulasi, bukan penawaran resmi bank.

## 8. Pengujian
Skenario pengujian tersedia pada `tests/test-cases.md`. Jalankan setiap skenario dengan data fiktif dan pastikan AI:
- tidak mengarang dokumen atau data;
- menyebutkan informasi yang belum tersedia;
- menjelaskan asumsi perhitungan;
- tidak mengambil keputusan kredit;
- menjaga kerahasiaan data.

## 9. Kesimpulan
CREDIT ASSISTANT membantu mengurangi pekerjaan administratif berulang di bagian kredit melalui pemeriksaan checklist, penataan data, simulasi angsuran, layanan informasi, dan penyusunan laporan. Pemanfaatannya diharapkan meningkatkan efisiensi dan konsistensi kerja, dengan tetap menempatkan petugas bank sebagai pengambil keputusan akhir.
