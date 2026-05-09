# Gitflow & Revert Commit Practice

## 📝 Deskripsi Proyek
Proyek ini adalah implementasi alur kerja (workflow) Git yang berfokus pada **Gitflow**, **Branching**, dan manajemen riwayat *commit* menggunakan **Git Revert**. Proyek ini dikerjakan untuk menyimulasikan kolaborasi nyata dalam tim pengembangan perangkat lunak dan manajemen repositori pengujian.

## 🎯 Objective
- Memahami cara kerja **Fork** dan **Clone** repositori.
- Mempraktikkan pembuatan *branch* baru dengan standar penamaan yang rapi (contoh: `feature/...`).
- Mensimulasikan pembuatan *test case* fungsionalitas aplikasi dalam format JSON.
- Memperbaiki kesalahan *commit* (seperti *typo* atau penghapusan file yang tidak disengaja) menggunakan `git revert` tanpa merusak riwayat *commit* utama.
- Mengajukan **Pull Request (PR)** dan memecahkan konflik (*conflict resolution*) sebelum proses penggabungan (*merge*).

## 📂 Struktur Pengerjaan Task
1. **Task 1:** Membuat *branch* `feature/lamria-revert-workflow`, membuat folder khusus, dan menambahkan file *test case* bernama `lamria-login-test.json`.
2. **Task 2:** Menyimulasikan perubahan yang mengandung kesalahan pada file JSON, melakukan *commit* kesalahan tersebut, dan kemudian memulihkan kondisi file ke versi yang benar menggunakan perintah `git revert <commit-id>`.

---

## 💡 Reflection & Key Takeaways

### 1. Pentingnya Alur Kerja yang Rapi dalam Gitflow
Bagian paling penting untuk memastikan alur kerja tetap rapi adalah kedisiplinan dalam menerapkan penamaan *branch* yang terstandarisasi (seperti awalan `feature/`) dan menghindari bekerja langsung di *branch* utama (`main`). 

Dalam kolaborasi proyek nyata, misalnya saat menyusun *test case* baru untuk fitur atau modul pengujian, *branching* memungkinkan pekerjaan terisolasi dengan aman. Hal ini memastikan bahwa skrip pengujian atau perubahan skenario *test* yang masih dalam proses penyusunan tidak merusak kode utama atau mengganggu pekerjaan anggota tim QA lainnya. Selain itu, pemisahan *branch* ini sangat memudahkan proses *code review* sebelum *pull request* disetujui.

### 2. Tantangan Menangani Revert Commit & Conflict
Hal paling menantang saat melakukan *revert commit* dan menangani *conflict* adalah ketelitian dalam membaca indikator *conflict* (`<<<<<<< HEAD`). Diperlukan kehati-hatian untuk menentukan secara pasti baris kode mana yang harus dipertahankan dan mana yang harus dibuang. Hal ini menjadi lebih krusial pada file berformat spesifik, seperti JSON, yang rentan mengalami kerusakan struktur jika ada tanda kurung atau koma yang salah hapus. 

Pengalaman ini secara signifikan meningkatkan pemahaman mengenai pentingnya melakukan *commit* secara kecil dan spesifik (*atomic commits*). Ketika *commit* dilakukan per satuan tugas yang jelas, proses pelacakan riwayat dan pelaksanaan *revert* menjadi jauh lebih terarah dan aman tanpa membawa risiko merusak fungsionalitas lain di dalam sistem.
