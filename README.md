# backend-nrp

Repo tugas mata kuliah **Pengembangan Backend Dasar**, dibuat dari template [`webdev-if-its/backend-template`](https://github.com/webdev-if-its/backend-template). Ganti judul di atas jadi nama repo kalian sendiri (`backend-nrp`, contoh: `backend-5025201012`).

## Aturan Umum

- Tugas tiap pertemuan disimpan di folder `pertemuan-XX/` pada repo ini.
- Commit message wajib menyebut level yang dicapai: `pertemuan-XX: level N selesai`.
- Deadline push: sebelum pertemuan berikutnya dimulai.
- Semua level dicek otomatis lewat `go test` — baca `pertemuan-XX/SOAL.md` tiap minggu untuk detail levelnya.

## Mengambil Pertemuan Baru Tiap Minggu

Repo ini **tidak otomatis sinkron** dengan template dosen. Begitu ada pertemuan baru, jalankan (ganti `pertemuan-02` sesuai minggu berjalan):

```bash
git fetch https://github.com/webdev-if-its/backend-template.git main
git checkout FETCH_HEAD -- pertemuan-02
```

Perintah ini **aman dijalankan kapan pun** — tidak akan menimpa folder pertemuan lain yang sudah kalian kerjakan, karena hanya mengambil folder yang disebutkan. Setelah itu, commit folder barunya seperti biasa.

Kalau dosen memperbaiki sesuatu di pertemuan yang sudah dirilis (mis. ada bug di test), biasanya cukup ambil ulang file yang diperbaiki saja, bukan seluruh folder — akan diumumkan file mana yang berubah.

---

Bagian di bawah ini **isi bertahap** sesuai level yang sedang kalian kerjakan (lihat `pertemuan-01/SOAL.md`) — heading-nya dicek otomatis, jangan diganti namanya.

## Identitas
- Nama: Rafian Dany Azadirahta
- NRP: 5053241008
- Kelas: M

## Commit vs Push
`git commit` adalah proses menyimpan perubahan pada kode secara lokal, perubahannya terlihat di riwayat git sendiri dan belum dapat dilihat oleh orang lain. Sedangkan `git push` mengirim perubahan yang sudah di-commit ke repository online, yang nantinya dapat dilihat oleh rekan yang memiliki akses. Saat seseorang sudah commit tapi lupa push, lalu rekannya pull dari repositori, maka perubahan yang dikerjakan tidak akan ikut terbawa. Jika bagian yang sebenarnya sudah selesai dikerjakan kembali, maka saat bagian yang lupa di-push itu akhirnya di-push, akan menimbulkan konflik.

## Reproducibility
Kalau anggota tim menjalankan program ini dengan versi Go yang berbeda, output dari `CetakInfo` juga akan berbeda karena memuat hasil `runtime.Version()`, misalnya satu orang menampilkan go1.21.0 sementara yang lain go1.23.0. Untuk program sederhana tidak akan jadi masalah karena perbedaan versi hanya terlihat di teks yang dicetak, tidak mempengaruhi jalannya program. Namun jika programnya kompleks, misal menggunakan fitur bahasa yang hanya tersedia di versi Go tertentu, atau bergantung pada library yang berubah antar versi, perbedaan versi Go bisa jadi masalah. Kalau satu anggota tim pakai versi lama yang tidak mendukung fitur tersebut, kodenya bisa gagal di-build di komputernya meskipun berhasil di komputer anggota lain, sehingga perlu menyepakati satu versi Go yang sama di awal.

## Catatan Merge Conflict
(tulis di sini)

## Kenapa .gitignore Penting
(tulis di sini)

## Refleksi
(tulis di sini)
