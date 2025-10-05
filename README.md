# README — Analisis Sentimen

**File sumber:** `project_analisis_sentimen.ipynb`

> README ini dibuat berdasarkan analisis menyeluruh terhadap notebook `project_analisis_sentimen.ipynb`. Tujuannya: memberi ringkasan proyek, panduan reproduksi, analisis mendalam terhadap isi notebook, temuan penting, dan rekomendasi perbaikan.

---

## Ringkasan singkat

Notebook ini adalah sebuah pipeline analisis sentimen yang bertujuan memproses data hasil *crawl* (platform X), membersihkan teks, melakukan ekstraksi fitur, menjalankan inferensi/klasifikasi sentimen menggunakan model instruksi (disebutkan `ibm-granite/granite-3.3-8b-instruct`), serta menampilkan visualisasi dan keluaran analisis.

---

## Berkas dataset yang direferensikan (ditemukan di kode)

Notebook mereferensikan beberapa nama file yang tampaknya berisi data mentah/hasil preprocessing:

* `data_mentah_bbm.csv`
* `tweet_bersih.csv`
* `tweets-data/data_mentah_bbm.csv
---

## Model & dependensi AI

* Notebook menyebutkan/menunjukkan penggunaan **IBM** model instruksi: `ibm-granite/granite-3.3-8b-instruct.
* Cara pemanggilan model (API/SDK) tidak sepenuhnya tereksekusi di environment ini — pastikan kredensial/API key IBM Granite tersedia jika inferensi dilakukan terhadap layanan eksternal.

---

## Gambaran alur (struktur umum notebook)

Berdasarkan isi notebook, alur kerjanya terlihat seperti berikut:

1. **Pengumpulan data** — data hasil crawl (platform X). (Telah dilakukan sebelumnya menurut keterangan.)
2. **Pemuatan dataset** — membaca CSV/JSON/Excel (file path disebutkan di beberapa sel kode).
3. **Pembersihan & pra-pemrosesan teks** — lowercasing, hapus URL/mention/angka/karakter khusus, tokenisasi, hapus stopwords, normalisasi (disebutkan/terlihat dari fungsi yang ada).
4. **Pelatihan / Inferensi** — pemanggilan model instruksi (IBM Granite) untuk klasifikasi sentimen atau menggunakan model lokal (tergantung implementasi sel).
5. **Penyimpanan output** — menyimpan grafik/hasil (beberapa gambar output berhasil diekstrak).

---

**Terima kasih.** 
