## Git log (Tugas 1)
![Git Log Tugas 1](online_graph.png)

## Git log (Tugas 2)
![Git Log Tugas 2](gitLog(Tugas2).png)

## Branch Protection Rules (Tugas 2)
![Branch Protection Rules](BP_rules.png)

## Conflict (Tugas 3)
![Conflict](konflik_ab.png)

## Git Log (Tugas 3)
![Git Log Tugas 3](gitLog(Tugas3).png)


## Deskripsi Projek
Project ini merupakan hasil praktikum Git dan GitHub yang bertujuan untuk memahami konsep version control secara langsung. Repository ini berisi sebuah website sederhana berbasis HTML yang menampilkan halaman profil singkat, terdiri dari bagian Home, About, dan Contact.

Dalam project ini diterapkan berbagai fitur Git, seperti pembuatan commit dengan format Conventional Commits, penggunaan branch (feature dan hotfix), pull request, serta pengelolaan konflik dan rebase. Selain itu, project ini juga mendokumentasikan seluruh proses penggunaan Git, mulai dari pengelolaan repository hingga kolaborasi menggunakan GitHub.

Website yang dibuat menampilkan informasi singkat tentang penulis sebagai seorang mahasiswi yang sedang belajar pemrograman web.
 

## Cara menjalankan project
1. Pertama, dibuka terminal (Command Prompt / Terminal / Git Bash), lalu perintah berikut dijalankan untuk mengambil repository dari GitHub ke komputer lokal:
```bash 
git clone https://github.com/saufaini/praktikum-git-561881.git
```

2. Setelah proses clone selesai, akan terbentuk folder project bernama praktikum-git-561881. Masuk ke dalam folder tersebut dengan perintah:
```bash 
cd praktikum-git-561881
```

3. Setelah berada di dalam folder project, file index.html dibuka menggunakan browser dengan perintah:
```bash 
open index.html
```
atau bisa juga dengan membuka folder project melalui File Explorer/Finder, lalu klik dua kali file index.html untuk melihat tampilan website.

## Screenshoot Website (Tugas 4)
![Screenshoot web]((web-html).png)



## 🧠 Dokumentasi Perintah Git (Bagian 1)

### 📁 Navigasi Direktori
- `cd praktikum-git-561881` → masuk ke folder repository lokal
- `pwd` → melihat lokasi direktori saat ini
- `ls` → melihat isi file dalam repository

---

### 🔄 Monitoring Repository
- `git status` → melihat status repository (apakah ada perubahan atau konflik)

---

### 💾 Commit & Perubahan
- `git add .` → menambahkan semua perubahan ke staging area
- `git commit -m "message"` → menyimpan perubahan dengan pesan commit
- `git commit` → digunakan saat menyelesaikan proses merge

---

### 🌐 Sinkronisasi dengan GitHub
- `git pull origin main` → mengambil perubahan terbaru dari repository GitHub ke lokal
- `git push origin <branch>` → mengirim perubahan dari lokal ke GitHub

---

### 🌿 Branching
- `git checkout -b feature/navbar` → membuat dan pindah ke branch navbar
- `git checkout -b feature/footer` → membuat dan pindah ke branch footer
- `git checkout -b hotfix/typo` → membuat dan pindah ke branch hotfix
- `git checkout main` → berpindah ke branch utama

## 🧠 Dokumentasi Perintah Git (Bagian 2)

### ⚔️ Simulasi Konflik

- `git checkout -b experiment/color-A` → membuat dan pindah ke branch percobaan warna A
- `git commit -m "feat: change background color to lightblue"` → mengubah warna background

- `git push origin experiment/color-A` → mengirim branch ke GitHub

- `git checkout main` → kembali ke branch utama
- `git checkout -b experiment/color-B` → membuat branch percobaan warna B

- `git commit -m "feat: change background color to lightcoral"` → mengubah warna dengan nilai berbeda

- `git push origin experiment/color-B` → mengirim branch ke GitHub

- `git pull origin main` → mengambil update terbaru sebelum membuat branch berikutnya

---

### 🔁 Rebase & Riwayat Commit

- `git log --oneline` → melihat riwayat commit secara ringkas
- `git log --oneline --graph` → melihat struktur branch dalam bentuk grafik

- `git rebase -i HEAD~3` → melakukan interactive rebase untuk menggabungkan 3 commit terakhir
- `git rebase --abort` → membatalkan proses rebase (saat tidak ada proses rebase aktif)

- `git push origin feature/dark-mode` → mengirim hasil rebase ke GitHub

---

### 🌿 Branch Dark Mode

- `git checkout -b feature/dark-mode` → membuat branch untuk fitur dark mode

- `git commit -m "feat: add dark mode base"` → commit awal dark mode
- `git commit -m "style: adjust text color for dark mode"` → penyesuaian warna teks
- `git commit -m "style: add padding for layout"` → penyesuaian layout

---

### 🔀 Merge

- `git merge feature/dark-mode` → menggabungkan branch dark mode ke main


## 🧠 Dokumentasi Perintah Git (Bagian 3)

### 🚫 Error Saat Push & Penyelesaiannya

- `git push origin main` → mencoba mengirim perubahan ke branch main (gagal)

- error:
  → push ditolak karena repository remote memiliki perubahan yang belum ada di lokal

- `git pull origin main` → mengambil perubahan terbaru dari GitHub agar sinkron

- `git checkout main` → memastikan berada di branch utama

- `git merge feature/dark-mode` → menggabungkan branch dark mode ke main setelah sinkron

- `git push origin main` → berhasil setelah konflik dan perbedaan versi diselesaikan

---

### 📸 Dokumentasi & File

- `git add .` → menambahkan file dokumentasi (screenshot, README, dll)
- `git commit -m "docs: add conflict and rebase documentation"` → menyimpan dokumentasi ke repository

---

### 🧪 Testing

- `open index.html` → membuka file website di browser untuk melihat hasil akhir