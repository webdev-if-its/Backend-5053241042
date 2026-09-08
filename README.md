# backend- 5053241042

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

- Nama: Ziyad Raziq Lahitidra Afey
- NRP: 5053241042
- Kelas: M (RPL)

## Commit vs Push

`git commit` menyimpan perubahan di repo lokal, sedangkan `git push` mengirim perubahan itu ke remote (GitHub). Kalau seseorang commit tapi lupa push, teman satu tim tetap melihat versi lama di GitHub.

## Reproducibility

Kalau tim menjalankan program dengan versi Go berbeda, hasilnya bisa tidak konsisten. Misalnya fitur baru di Go 1.23 tidak ada di Go 1.19, sehingga kode bisa error.

## Catatan Merge Conflict

Konflik terjadi di fungsi `CetakInfo` karena dua branch mengubah baris `return` dengan cara berbeda. Branch `fitur-sapaan` menambahkan sapaan, sedangkan branch utama mengubah format output. Hasil akhirnya saya gabungkan: tetap menampilkan Nama, NRP, versi Go, dan juga sapaan dari `Sapa()`.

## Kenapa .gitignore Penting

Kalau file hasil build (`*.exe`, `bin/`) atau konfigurasi IDE (`.vscode/`, `.idea/`) ikut tercommit, repo jadi berantakan dan teman satu tim bisa terganggu karena file pribadi ikut terbawa.

## Refleksi

Bagian paling membingungkan adalah saat pertama kali mengalami merge conflict karena muncul tanda `<<<<<<<` dan `>>>>>>>`. Setelah mencoba menyatukan isi kedua branch, saya jadi paham cara menyelesaikan konflik. Sekarang saya lebih percaya diri menghadapi konflik di Git.
