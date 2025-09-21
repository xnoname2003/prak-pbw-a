# TUGAS PRAKTIKUM PERTAMA: INSTALASI GIT DAN INTEGRASI GITHUB

## 📃 Identitas Diri

- **Nama**             : Chaerul Cahyadi
- **NPM**              : 4523210120
- **Mata Kuliah**      : Pemrograman Berbasis Web (A)
- **Dosen Pengampu**   : Adi Wahyu Pribadi, S.Si., M.Kom.

---

## A. Bagian 1: Instalasi & Konfigurasi Awal Git

   ### 1. Install Git 

   Git adalah system control versi terdistribusi yang pertama kali diciptakan dan dikembangkan oleh Linus Torvalds serta digunakan untuk mengelola kode program. Berikut langkah-langkah instalasi Git pada beberapa sistem operasi:
   
   1. #### Windows
      1. Unduh installer: *https://git-scm.com/download/win*
      2. Jalankan file `.exe` yang diunduh.
      3. Saat instalasi, biarkan pengaturan default lalu klik **Next** hingga selesai.
      3. Buka **Command Prompt** atau **Git Bash** untuk memastikan **Git** berhasil terinstall, jalankan:
         ```
         git --version 
         ```

   2. #### MacOS
      1. Buka **Terimanal** lalu Install **Homebrew**, jalankan perintah berikut: 
         ```
         /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
         ```
      2. Install **Git** pada **Terminal**, jalankan perintah berikut:
         ``` 
         brew install git 
         ```
      3. Untuk memastikan **Git** berhasil terinstall, jalankan:
         ```
         git --version
         ```

   3. #### Linux
      1. Buka **Terimanal** lalu update sistem, jalankan perintah berikut: 
         ```
         sudo apt update
         ```
      2. Install **Git** pada **Terminal**, jalankan perintah berikut:
         ``` 
         sudo apt install git
         ```
      3. Untuk memastikan **Git** berhasil terinstall, jalankan:
         ```
         git --version
         ```

   ### 2. Konfigurasi Awal (Wajib)

   Setelah **Git** berhasil diinstall, langkah berikutnya adalah melakukan konfigurasi awal. Konfigurasi ini bertujuan agar setiap perubahan yang dibuat dapat tercatat dengan identitas berupa nama pengguna dan alamat email yang sesuai.

   1) Lanjutkan di **Command Prompt** atau di **Terminal** dengan mengetikkan perintah berikut untuk  mengatur nama pengguna. Perintah ini berfungsi untuk menyimpan nama pengguna secara global pada **Git**.
      ```
      git config --global user.name "Your Name"
      ```
      <img width="759" height="" alt="Konfigurasi Nama" src="https://github.com/user-attachments/assets/3f10381e-3f88-44c7-af24-76f5f3162881" />

   2) Setelah itu, atur alamat email yang akan digunakan dengan perintah berikut.
      ```
       git config --global user.email "your@email.com"
      ```
      <img width="992" height="" alt="Konfigurasi Email" src="https://github.com/user-attachments/assets/e820ac40-bacb-4c8a-b25c-751445dbd539" />
   
   3) Untuk memastikan nama dan email terdaftar, jalankan perintah berikut:
      ```
      git config --global user.name
      ```
      <img width="992" height="" alt="Cek Nama" src="https://github.com/user-attachments/assets/5de1cb53-023d-496e-95a0-66b2e79f9f01" />

      ```
      git config --global user.email
      ```
      <img width="992" height="" alt="Cek Email" src="https://github.com/user-attachments/assets/e5fdf0e9-47df-448e-8e48-557d2adbc31d" />

---

## B. Bagian 2: Alur Kerja Dasar Git (Lokal)

   ### 1. Membuat Proyek Baru dan Inisialisasi Git

   1) Buka **Command Prompt** atau **terminal**, jalankan perintah berikut untuk membuat folder baru, pada contoh ini path terminal yang dipakai yaitu `/Users/chaerul/Kuliah UP/Semester 5/Prak. PBW A`.
      ```
      mkdir Prak1
      ```
      <img width="" height="" alt="Membuat Folder Prak1" src="https://github.com/user-attachments/assets/9de5fc8e-98c4-4e30-92ef-9dfe3a630bc0" />

   2) Setelah folder dibuat, jalankan perintah berikut untuk pindah ke folder `Prak1` yang telah dibuat.
      ```
      cd Prak1
      ```

      <img width="" height="" alt="Pindah ke Projek" src="https://github.com/user-attachments/assets/f1e4f200-6323-4c2b-99cb-4343d0a40d06" />
   
   3) Jalankan perintah berikut untuk inisialisasi projek atau folder yang telah dibuat
      ```
      git init
      ```
      <img width="" height="" alt="Inisialisasi Projek" src="https://github.com/user-attachments/assets/7ab5e9df-875e-4021-a050-e606262adc1e" />
   
   ### 2. Buat Beberapa File

   1) Jalankan perintah berikut untuk membuat file `index.html` pada folder `Prak1`
      ```
      echo "<h1>Selamat Datang</h1>" > index.html
      ```
      <img width="" height="" alt="Membuat file index.html" src="https://github.com/user-attachments/assets/e0629351-bc94-47b5-b9d6-22115e85d31d" />

   2) Jalankan perintah berikut untuk membuat folder `css` pada folder `Prak1`
      ```
      mkdir css
      ```
      <img width="" height="" alt="Membuat folder css" src="https://github.com/user-attachments/assets/0cf516e9-1a1c-4a94-a974-4c7dfde7f1d8" />

   3) Jalankan perintah berikut untuk membuat file `style.css` pada folder `css` yang telah dibuat.
      ```
      echo "body { font-family: sans-serif; }" > css/style.css
      ```
      <img width="" height="" alt="Membuat folder css" src="https://github.com/user-attachments/assets/b8dee407-1db0-49f2-af1d-d4c0b9093a6c" />

   ### 3. Cek Status & Masuk ke Staging Area

   Setelah file proyek dibuat, kita perlu menyimpannya ke dalam **version control Git**. Proses ini dilakukan melalui dua tahap, yaitu pengecekan status dan menambahkan file ke staging area.

   1) Cek status repository dengan perintah di bawah ini. Perintah ini akan menampilkan file apa saja yang belum dicatat oleh Git.
      ```
      git status
      ```
      <img width="" height="" alt="Cek status" src="https://github.com/user-attachments/assets/fe139b0c-e0d3-4155-9628-c388a9a99cf5" />
   
   2) Tambahkan semua file ke **staging area** menggunakan perintah berikut ini. Titik (.) berarti semua file di dalam folder tersebut akan dimasukkan ke **staging area**.
      ```
      git add .
      ```
      <img width="" height="" alt="git add" src="https://github.com/user-attachments/assets/c0e56848-a5b7-4890-bef7-d4287c7d83a9" />
   
   3) Menyimpan Perubahan (Commit)

      Simpan perubahan tersebut dengan **commit**. Teks di dalam tanda kutip merupakan pesan **commit**, yang menjelaskan perubahan yang dilakukan.
      ```
      git commit -m "feat: Inisialisasi proyek dengan file index dan css"
      ```
      <img width="" height="" alt="git commit" src="https://github.com/user-attachments/assets/c5cc6418-7901-4799-9f7f-2faef901db34" />
   
   4) Buat dan Pindah ke Branch Baru

      Jalankan perintah berikut untuk membuat **branch** baru dengan nama `fitur-kontak`
      ```
      git checkout -b fitur-kontak
      ```
      <img width="" height="" alt="Membuat branch baru" src="https://github.com/user-attachments/assets/be20e697-5cc6-42c3-84f7-21d2f8035bae" />
   
   5) Buat File Baru di Branch `fitur-kontak`

      Jalankan perintah berikut untuk membuat file `kontak.html` pada branch `fitur-kontak`
      ```
      echo "<h1>Halaman Kontak</h1>" > kontak.html
      ```
      <img width="" height="" alt="Membuat file kontak.html" src="https://github.com/user-attachments/assets/b03760cc-64d6-445f-a920-d0bc6e362a3a" />
   
   6) Staging & Commit di Branch

      Tambahkan file baru ke **staging area** dan simpan dengan **commit** menggunakan perintah berikut:
      ```
      git add .
      ```
      <img width="" height="" alt="git add . kontak.html" src="https://github.com/user-attachments/assets/4acef6c8-458b-4196-b59b-a9ef00635db8" />

      ```
      git commit -m "feat: Menambahkan halaman kontak"
      ```
      <img width="" height="" alt="git commit kontak.html" src="https://github.com/user-attachments/assets/f409e677-6277-4490-aabd-700153fb2b98" />
   
   7) Pindah dan Menggabungkan Branch (**Merge**)

      Pindah ke branch utama (**main/master**) dan gabungkan (**merge**) branch `fitur-kontak` ke branch utama menggunakan perintah berikut:
      ```
      git checkout main
      ```
      <img width="" height="" alt="pindah ke branch utama" src="https://github.com/user-attachments/assets/ec321449-bdbb-4134-847c-ceb8b8652fcb" />

      ```
      git merge fitur-kontak
      ```
      <img width="" height="" alt="merge ke branch utama" src="https://github.com/user-attachments/assets/ed57363c-f459-4cbb-a45f-83ce5ba462cc" />
      
---

## C. Bagian 3: Integrasi dengan GitHub

   ### 1. Membuat Repository di GitHub

   <img width="" height="" alt="create repository" src="https://github.com/user-attachments/assets/9b284bde-cdf8-47be-b58c-6d89af4a323b" />

   ### 2. Menghubungkan Repository Lokal dengan GitHub
   
   1) Jalankan perintah berikut untuk menambahkan repository GitHub sebagai remote. Salin link repository GitHub.
      ```
      git remote add origin https://github.com/youraccount/your-project
      ```
      <img width="" height="" alt="git remote" src="https://github.com/user-attachments/assets/4ec37c2d-7eb4-4057-952e-ead5802c10a5" />

   2) Atur nama branch utama menjadi `main`:
      ```
      git branch -M main
      ```
      <img width="" height="" alt="Ubah branch jadi main" src="https://github.com/user-attachments/assets/0f39e457-ebaf-4f74-8f31-50e6719c5121" />

   3) Unggah proyek ke GitHub dengan perintah:
      ```
      git push -u origin main
      ```
      <img width="" height="" alt="git push" src="https://github.com/user-attachments/assets/b51c9e69-1f4e-4d69-a341-6e90bf488b69" />

   4) Setelah itu refresh GitHub, maka file yang sudah dibuat akan muncul di dalam repository GitHub yang sudah dibuat dan repository lokal akan terhubung dengan repository GitHub, dan seluruh file proyek akan tersedia secara online.
      
      <img width="" height="" alt="Hasil Pembuatan File di GitHub" src="https://github.com/user-attachments/assets/c17c7b86-7e2b-491e-a5cb-f56be9de30ef" />

---

## D. Bagian 4: Workflow Kerja Kelompok di GitHub (Feature Branch Workflow)

   ### 1. Clone Repository (sekali di awal)
   Jalankan perintah berikut untuk **clone** atau menduplikat repository ke dalam folder `Prak1`.
   ```
   git clone URL_REPOSITORY
   ```
   <img width="" height="" alt="git clone" src="https://github.com/user-attachments/assets/bac6d5e5-6ab6-46de-94ac-406fa3cd5556" />
