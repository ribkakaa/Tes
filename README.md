# NL2SQL 🤖🧠
NL2SQL adalah singkatan dari Natural Language to Structured Query Language. Sederhananya, ini adalah teknologi yang memungkinkan komputer untuk mengubah bahasa manusia sehari-hari (seperti Bahasa Indonesia atau Inggris) menjadi kode perintah database (SQL) secara otomatis.

Teknologi ini bertujuan untuk menjembatani celah antara pengguna awam yang tidak paham pemrograman dengan data kompleks yang tersimpan di dalam database.

## Rumusan Masalah NL2SQL ⚠️

Masalah dalam NL2SQL umumnya terbagi menjadi tiga kategori besar:

A. Ambiguitas Bahasa Manusia (Linguistic Ambiguity)
   Bahasa manusia sering kali tidak spesifik.
   Masalah: Pengguna mungkin bertanya, "Siapa pelanggan terbaik kita?". Kata "terbaik" bisa berarti pelanggan dengan transaksi terbanyak, total belanjaan tertinggi, atau yang paling lama berlangganan.
   Dampak: AI bingung menentukan kolom mana yang harus digunakan untuk pengurutan (ORDER BY).

B. Struktur Database yang Kompleks (Schema Mapping)
   Masalah : Nama kolom dalam database sering kali menggunakan singkatan teknis (misal: cust_id_fin_01) yang tidak mirip dengan bahasa manusia ("Nomor Identitas Pelanggan").

   Dampak: AI gagal memetakan kata benda dalam kalimat ke nama tabel atau kolom yang benar.

C. Join dan Logika Bertingkat (Complex Queries)
   Masalah: Pertanyaan yang membutuhkan data dari banyak tabel (Multi-join) atau filter bertingkat (Subqueries).

   Dampak: SQL yang dihasilkan sering kali salah dalam menghubungkan kunci utama (Primary Key) dan kunci asing (Foreign Key).

## Bagaimana Cara Kerja NL2SQL?
✅ Proses NL2SQL biasanya melibatkan kecerdasan buatan (AI), khususnya Natural Language Processing (NLP). Berikut adalah Salur sederhananya:

✅ Input Pengguna: Anda mengetik pertanyaan seperti, "Tampilkan daftar karyawan yang memiliki gaji di atas 10 juta."

✅ Analisis AI: Sistem menganalisis struktur kalimat, mencari kata kunci (entitas), dan memetakannya ke tabel serta kolom yang ada di database.

✅ Generasi SQL: AI menyusun kode SQL yang valid berdasarkan analisis tersebut.

✨ Hasil: SELECT * FROM karyawan WHERE gaji > 10000000;

✨ Eksekusi: Kode tersebut dijalankan di database, dan hasilnya diberikan kembali kepada Anda.

## Mengapa NL2SQL Penting?
Ada beberapa alasan, mengapa NL2SQL sangat penting.

🤖 Demokratisasi Data: Orang di bagian pemasaran, HR, atau manajer tingkat atas bisa mengambil data sendiri tanpa harus menunggu bantuan dari tim IT atau data analyst.

🤖 Efisiensi Waktu: Menulis query SQL yang kompleks bisa memakan waktu. Dengan NL2SQL, prosesnya hanya butuh hitungan detik.

🤖 Mengurangi Kesalahan Manusia: Mengurangi risiko typo atau kesalahan logika saat menulis perintah manual yang panjang.

## Dasar-Dasar Database (SQL) 🗄️
Sebelum mengubah bahasa alami menjadi SQL, Anda harus sangat mahir dalam SQL itu sendiri.

- DML (Data Manipulation Language): SELECT, INSERT, UPDATE, DELETE.

- Complex Joins: Memahami INNER, LEFT, RIGHT, dan FULL JOIN.

- Aggregation & Grouping: GROUP BY, HAVING, dan fungsi jendela (window functions).

- Database Schema: Memahami relasi Primary Key dan Foreign Key serta normalisasi database.

## Contoh Perbandingan (Case Study) 💡

### Contoh 1:
#### Bahasa Manual (Input):            

#### Siapa saja pembeli Jakarta?        
                                       
#### Quary SQL (Output):

```SELECT * FROM customers WHERE city = 'Jakarta';```

### Contoh 2:
#### Bahasa Manual (Input):  

#### Total penjualan Bulan lalu  

#### Quary SQL (Output): 

 ```SELECT SUM(amount) FROM sales WHERE month = 'April';```

 ## API yang digunakal adalah OLLAMA
API Ollama adalah jembatan komunikasi yang memungkinkan aplikasi lain (seperti website, aplikasi mobile, atau skrip Python) untuk berinteraksi dengan model AI yang berjalan di dalam Ollama tersebut.

## 🛠️ Apa Yang Dilakukan Oleh OLLAMA?

- Dengan menggunakan API, Anda bisa membuat program yang secara otomatis melakukan hal-hal berikut:

- Generate Response: Mengirim perintah teks dan mendapatkan jawaban.

- Streaming: Mendapatkan jawaban kata demi kata secara real-time (seperti ChatGPT).

- Chat: Mengelola percakapan yang memiliki riwayat (memory).

- Model Management: Meminta sistem untuk mengunduh (pull), menghapus, atau menyalin model AI tertentu melalui kode.

- Embeddings: Mengubah teks menjadi angka (vektor) untuk kebutuhan pencarian data tingkat lanjut (RAG).
