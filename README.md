# 🏦 Simulasi Sistem Antrian Customer Service Bank  
## 📊 Analisis Kinerja, Perilaku Sistem, dan Optimasi Layanan Menggunakan Discrete Event Simulation

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue.svg"/>
  <img src="https://img.shields.io/badge/Simulation-Discrete%20Event-orange.svg"/>
  <img src="https://img.shields.io/badge/Library-SimPy-green.svg"/>
  <img src="https://img.shields.io/badge/Analysis-Queueing%20System-success.svg"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen.svg"/>
</p>

<p align="center">
  ⏱️ Queueing Theory &nbsp;•&nbsp; 👩‍💼 Customer Service &nbsp;•&nbsp; 📈 Data-Driven Simulation
</p>

---

## 📌 Deskripsi Umum Proyek

Repository ini menyajikan **simulasi sistem antrian Customer Service (CS) pada bank** menggunakan pendekatan **Discrete Event Simulation (DES)** dengan bantuan pustaka **SimPy** pada Python.  
Simulasi dirancang untuk **merepresentasikan kondisi operasional nyata** pada layanan perbankan, di mana pelanggan datang secara acak, menunggu dalam antrian, dilayani oleh CS, dan kemudian meninggalkan sistem.

Pendekatan simulasi dipilih karena:
- sistem antrian bersifat dinamis dan stokastik,
- sulit dianalisis hanya dengan perhitungan matematis sederhana,
- perubahan parameter operasional (jumlah CS, tingkat kedatangan, durasi layanan) dapat diuji tanpa risiko pada sistem nyata.

Melalui simulasi ini, dilakukan **eksperimen terkontrol** untuk memahami perilaku sistem, mengukur kinerjanya, dan mengevaluasi berbagai skenario peningkatan layanan.

---

## 👤 Identitas Mahasiswa

| Keterangan | Informasi |
|-----------|----------|
| **Nama** | Maylani Kusuma Wardhani |
| **NIM** | 202210370311123 |
| **Kelas** | Pemodelan dan Simulasi Data C |

📓 **Google Colab (Kode Lengkap, Output, & Visualisasi)**  
👉 https://colab.research.google.com/drive/1gS63C9T1QkQ54_4qyUEfodXppGFhd4-_?usp=sharing  

---

## 📘 Latar Belakang Teoritis

### Sistem Antrian dalam Layanan Perbankan

Dalam dunia perbankan, Customer Service berperan sebagai **gerbang utama interaksi antara bank dan nasabah**. Sistem antrian yang tidak optimal dapat menyebabkan:
- waktu tunggu yang panjang,
- penurunan kepuasan pelanggan,
- kelelahan pegawai,
- serta inefisiensi operasional.

Sebaliknya, sistem dengan kapasitas layanan berlebih dapat menyebabkan **pemborosan sumber daya** dan biaya operasional yang tidak perlu.

Oleh karena itu, dibutuhkan pendekatan analitis yang mampu:
- memodelkan ketidakpastian kedatangan pelanggan,
- merepresentasikan variasi waktu layanan,
- serta mengevaluasi performa sistem secara menyeluruh.

---

## 🎯 Tujuan dan Ruang Lingkup Simulasi

### Tujuan Umum
Menganalisis dan mengevaluasi kinerja sistem antrian Customer Service bank menggunakan simulasi berbasis peristiwa diskrit.

### Tujuan Khusus
1. Mengukur waktu tunggu pelanggan pada berbagai kondisi sistem.
2. Menganalisis tingkat utilisasi Customer Service.
3. Mengidentifikasi ketidakseimbangan beban kerja antar CS.
4. Membandingkan efektivitas beberapa skenario operasional.
5. Memberikan rekomendasi peningkatan layanan berbasis hasil simulasi.

---

## ⚙️ Pendekatan dan Metodologi Simulasi

### Discrete Event Simulation (DES)

Simulasi ini menggunakan konsep **Discrete Event Simulation**, di mana perubahan status sistem hanya terjadi pada waktu tertentu (event), seperti:
- kedatangan pelanggan,
- dimulainya layanan,
- selesainya layanan.

Setiap pelanggan dimodelkan sebagai **entitas independen** yang berinteraksi dengan sumber daya terbatas, yaitu Customer Service.

### Alur Proses Simulasi
1. Pelanggan datang ke sistem berdasarkan distribusi waktu antar kedatangan.
2. Jika CS tersedia, pelanggan langsung dilayani.
3. Jika CS sibuk, pelanggan masuk ke dalam antrian.
4. Setelah layanan selesai, pelanggan keluar dari sistem.
5. Proses berulang hingga seluruh pelanggan selesai dilayani.

---

## 🔧 Parameter Sistem

| Parameter | Nilai |
|---------|------|
| Jumlah pelanggan default | 150 |
| Jumlah Customer Service | 2 |
| Rata-rata waktu layanan | 5 menit |
| Deviasi standar layanan | 2 menit |
| Waktu mulai simulasi | 07.00 WIB |
| Random seed | 42 |

Parameter ini dipilih untuk merepresentasikan kondisi operasional bank skala menengah.

---

## 🔄 Skenario Eksperimen

### 🔹 Skenario Default
Sistem dijalankan dengan 2 CS dan 150 pelanggan menggunakan variasi waktu kedatangan rata-rata:
- 1 menit (sangat padat),
- 2 menit (sedang),
- 3 menit (relatif longgar).

Tujuan skenario ini adalah untuk mengamati sensitivitas sistem terhadap perubahan tingkat kedatangan.

---

### 🔹 Scenario 1 – Penambahan Customer Service
Jumlah CS ditambah menjadi 3 dengan parameter lain tetap.  
Skenario ini bertujuan untuk:
- mengevaluasi dampak peningkatan kapasitas layanan,
- membandingkan waktu tunggu sebelum dan sesudah penambahan CS,
- menganalisis perubahan utilisasi sistem.

---

### 🔹 Scenario 2 – Lonjakan Pelanggan
Jumlah pelanggan ditingkatkan menjadi 300 orang dengan tingkat kedatangan tinggi.  
Skenario ini mensimulasikan kondisi ekstrem seperti:
- jam sibuk,
- hari gajian,
- atau gangguan sistem digital.

---

### 🔹 Scenario 3 – Variasi Waktu Layanan
Rata-rata waktu layanan diperpanjang menjadi 7 menit dengan deviasi standar 4 menit.  
Skenario ini digunakan untuk melihat dampak kompleksitas layanan terhadap panjang antrian.

---

## 📊 Indikator Kinerja Sistem

Selama simulasi, beberapa metrik utama dikumpulkan dan dianalisis:

- Waktu tunggu rata-rata pelanggan
- Utilisasi Customer Service
- Waktu sibuk dan waktu idle CS
- Distribusi jumlah pelanggan yang dilayani tiap CS
- Total durasi simulasi

Data hasil simulasi disimpan dalam format **CSV dan XLSX** untuk kemudahan analisis lanjutan.

---

## 📈 Hasil Simulasi dan Interpretasi

Hasil simulasi menunjukkan bahwa **waktu tunggu pelanggan meningkat drastis ketika tingkat kedatangan mendekati atau melebihi kapasitas layanan**.  
Pada skenario kedatangan cepat (1 menit), sistem dengan 2 CS mengalami overload, ditandai dengan:
- waktu tunggu sangat panjang,
- utilisasi CS mendekati 100%,
- serta antrian yang terus bertambah.

Penambahan CS pada Scenario 1 secara signifikan menurunkan waktu tunggu dan mempercepat penyelesaian sistem, namun pada tingkat kedatangan rendah menyebabkan utilisasi menurun, menunjukkan adanya kelebihan kapasitas.

Scenario 2 memperlihatkan batas kemampuan sistem, di mana lonjakan pelanggan tanpa penyesuaian kapasitas menyebabkan kegagalan layanan secara operasional.

Scenario 3 menegaskan bahwa durasi layanan memiliki pengaruh yang sama pentingnya dengan jumlah CS dan tingkat kedatangan.

---

## 🔍 Analisis Kritis

- Sistem paling stabil ketika utilisasi berada di kisaran 85–95%.
- Overutilization menyebabkan antrian panjang dan kelelahan sumber daya.
- Underutilization menunjukkan pemborosan kapasitas.
- Ketidakseimbangan beban kerja muncul pada hampir semua skenario ekstrem.

---

## ✅ Kesimpulan Akhir

Simulasi ini membuktikan bahwa **pengelolaan sistem antrian Customer Service memerlukan keseimbangan antara kapasitas layanan dan tingkat permintaan**.  
Pendekatan simulasi memberikan alat yang kuat untuk:
- memahami perilaku sistem secara mendalam,
- menguji skenario tanpa risiko nyata,
- serta merancang layanan bank yang lebih efisien dan adaptif.

---

## 🛠️ Teknologi dan Tools

- Python  
- SimPy  
- Pandas & NumPy  
- Matplotlib  
- Google Colab  

---

## ⭐ Penutup

Repository ini disusun sebagai dokumentasi akademik sekaligus media pembelajaran mengenai **Simulasi Sistem Antrian Customer Service Bank**.  
Diharapkan proyek ini dapat menjadi referensi dalam mata kuliah pemodelan dan simulasi serta pengambilan keputusan berbasis data.

⭐ Beri **Star** jika repository ini bermanfaat  
🍴 **Fork** untuk pengembangan lanjutan  

Terima kasih.
