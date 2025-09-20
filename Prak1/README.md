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
      <img width="759" height="" alt="Konfigurasi Nama" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491905411-3f10381e-3f88-44c7-af24-76f5f3162881.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T105142Z&X-Amz-Expires=300&X-Amz-Signature=9d0da7ea982a6f5c9d81e1fcf0ffc535fb5fc34d8da8498968ef9eaa5ee5f991&X-Amz-SignedHeaders=host" />

   2) Setelah itu, atur alamat email yang akan digunakan dengan perintah berikut.
      ```
       git config --global user.email "your@email.com"
      ```
      <img width="992" height="" alt="Konfigurasi Email" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491905728-e820ac40-bacb-4c8a-b25c-751445dbd539.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T105708Z&X-Amz-Expires=300&X-Amz-Signature=4bc5450de276e2873e46f0509cc962dbe71bf6cd2f37167805db2b43baf264f5&X-Amz-SignedHeaders=host" />
   
   3) Untuk memastikan nama dan email terdaftar, jalankan perintah berikut:
      ```
      git config --global user.name
      ```
      <img width="992" height="" alt="Cek Nama" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491906000-5de1cb53-023d-496e-95a0-66b2e79f9f01.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T110039Z&X-Amz-Expires=300&X-Amz-Signature=490a82cb302099acb63944b1778dd493ef6ed56b4c080e24e60d39d9092c2cf6&X-Amz-SignedHeaders=host" />

      ```
      git config --global user.email
      ```
      <img width="992" height="" alt="Cek Email" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491906336-e5fdf0e9-47df-448e-8e48-557d2adbc31d.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T110304Z&X-Amz-Expires=300&X-Amz-Signature=923f4c3795be7f9ec123d16487ddff1cea8b9184c949931074a66b8b49cf52d9&X-Amz-SignedHeaders=host" />

---

## B. Bagian 2: Alur Kerja Dasar Git (Lokal)

   ### 1. Membuat Proyek Baru dan Inisialisasi Git

   1) Buka **Command Prompt** atau **terminal**, jalankan perintah berikut untuk membuat folder baru, pada contoh ini path terminal yang dipakai yaitu `/Users/chaerul/Kuliah UP/Semester 5/Prak. PBW A`.
      ```
      mkdir Prak1
      ```
      <img width="" height="" alt="Membuat Folder Prak1" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491968117-9de5fc8e-98c4-4e30-92ef-9dfe3a630bc0.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T190111Z&X-Amz-Expires=300&X-Amz-Signature=0ee776d4a9e3f46709c0ab40eee6328ad446c508d651a9984d664b34a82876bd&X-Amz-SignedHeaders=host" />

   2) Setelah folder dibuat, jalankan perintah berikut untuk pindah ke folder `Prak1` yang telah dibuat.
      ```
      cd Prak1
      ```

      <img width="" height="" alt="Pindah ke Projek" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491973182-f1e4f200-6323-4c2b-99cb-4343d0a40d06.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T195810Z&X-Amz-Expires=300&X-Amz-Signature=8ee30dbe7c41fe233d963faad5268aaf3a204e8602c8c8a6c8e719ecad55898a&X-Amz-SignedHeaders=host" />
   
   3) Jalankan perintah berikut untuk inisialisasi projek atau folder yang telah dibuat
      ```
      git init
      ```
      <img width="" height="" alt="Inisialisasi Projek" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491974494-7ab5e9df-875e-4021-a050-e606262adc1e.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T203619Z&X-Amz-Expires=300&X-Amz-Signature=04f183e55303cc4f1c78ecc3d1fbd70e00c658790c67418b2ab03c817d57e9f7&X-Amz-SignedHeaders=host" />
   
   ### 2. Buat Beberapa File

   1) Jalankan perintah berikut untuk membuat file `index.html` pada folder `Prak1`
      ```
      echo "<h1>Selamat Datang</h1>" > index.html
      ```
      <img width="" height="" alt="Membuat file index.html" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491975883-e0629351-bc94-47b5-b9d6-22115e85d31d.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T204524Z&X-Amz-Expires=300&X-Amz-Signature=c9da162d3f4388f5b441bd830915a26e62ee3090958afcf72d536fe40b24b04f&X-Amz-SignedHeaders=host" />

   2) Jalankan perintah berikut untuk membuat folder `css` pada folder `Prak1`
      ```
      mkdir css
      ```
      <img width="" height="" alt="Membuat folder css" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491976029-0cf516e9-1a1c-4a94-a974-4c7dfde7f1d8.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T204759Z&X-Amz-Expires=300&X-Amz-Signature=10d8ec33f80eadaad68872ab5a3fd6cc69d8bd47e58fc6f562b60d8cc00bd5b4&X-Amz-SignedHeaders=host" />

   3) Jalankan perintah berikut untuk membuat file `style.css` pada folder `css` yang telah dibuat.
      ```
      echo "body { font-family: sans-serif; }" > css/style.css
      ```
      <img width="" height="" alt="Membuat folder css" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491976253-b8dee407-1db0-49f2-af1d-d4c0b9093a6c.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T205230Z&X-Amz-Expires=300&X-Amz-Signature=f46d90f0b7427c2de7cdbb3838947ddd3f78056e30e7a435464e6bb403e86e8a&X-Amz-SignedHeaders=host" />

   ### 3. Cek Status & Masuk ke Staging Area

   Setelah file proyek dibuat, kita perlu menyimpannya ke dalam **version control Git**. Proses ini dilakukan melalui dua tahap, yaitu pengecekan status dan menambahkan file ke staging area.

   1) Cek status repository dengan perintah di bawah ini. Perintah ini akan menampilkan file apa saja yang belum dicatat oleh Git.
      ```
      git status
      ```
      <img width="" height="" alt="Cek status" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491976742-fe139b0c-e0d3-4155-9628-c388a9a99cf5.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T210226Z&X-Amz-Expires=300&X-Amz-Signature=b4812a948e7c9e0983375773444c99f1acaa673f996ea18203dbac55ccd2c6ba&X-Amz-SignedHeaders=host" />
   
   2) Tambahkan semua file ke **staging area** menggunakan perintah berikut ini. Titik (.) berarti semua file di dalam folder tersebut akan dimasukkan ke **staging area**.
      ```
      git add .
      ```
      <img width="" height="" alt="git add" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491977260-c0e56848-a5b7-4890-bef7-d4287c7d83a9.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T211322Z&X-Amz-Expires=300&X-Amz-Signature=1487ca06e23c68b2163010750a428c461fafbbbef2b4f9926f5b86838c56f914&X-Amz-SignedHeaders=host" />
   
   3) Menyimpan Perubahan (Commit)

      Simpan perubahan tersebut dengan **commit**. Teks di dalam tanda kutip merupakan pesan **commit**, yang menjelaskan perubahan yang dilakukan.
      ```
      git commit -m "feat: Inisialisasi proyek dengan file index dan css"
      ```
      <img width="" height="" alt="git commit" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491977563-c5cc6418-7901-4799-9f7f-2faef901db34.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T212032Z&X-Amz-Expires=300&X-Amz-Signature=e7b05337d57cda8b27328bdd3aac8527c41544551a210d8d596bb5003c714ef1&X-Amz-SignedHeaders=host" />
   
   4) Buat dan Pindah ke Branch Baru

      Jalankan perintah berikut untuk membuat **branch** baru dengan nama `fitur-kontak`
      ```
      git checkout -b fitur-kontak
      ```
      <img width="" height="" alt="Membuat branch baru" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491977916-be20e697-5cc6-42c3-84f7-21d2f8035bae.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T212750Z&X-Amz-Expires=300&X-Amz-Signature=c50275f31a836c28e9f14c8703df60743f6cdf94223ace7368935ce757594131&X-Amz-SignedHeaders=host" />
   
   5) Buat File Baru di Branch `fitur-kontak`

      Jalankan perintah berikut untuk membuat file `kontak.html` pada branch `fitur-kontak`
      ```
      echo "<h1>Halaman Kontak</h1>" > kontak.html
      ```
      <img width="" height="" alt="Membuat file kontak.html" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491978137-b03760cc-64d6-445f-a920-d0bc6e362a3a.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T213330Z&X-Amz-Expires=300&X-Amz-Signature=431da69924a0b5df80b445549aee4122891e99b1807e6d58a96a7cb2e41231be&X-Amz-SignedHeaders=host" />
   
   6) Staging & Commit di Branch

      Tambahkan file baru ke **staging area** dan simpan dengan **commit** menggunakan perintah berikut:
      ```
      git add .
      ```
      <img width="" height="" alt="git add . kontak.html" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491978412-4acef6c8-458b-4196-b59b-a9ef00635db8.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T213924Z&X-Amz-Expires=300&X-Amz-Signature=c36582a4941b9228bc7a9ccef9509b3be1aa8d09835395a6104207d4a00d8503&X-Amz-SignedHeaders=host" />

      ```
      git commit -m "feat: Menambahkan halaman kontak"
      ```
      <img width="" height="" alt="git commit kontak.html" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491978525-f409e677-6277-4490-aabd-700153fb2b98.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T214126Z&X-Amz-Expires=300&X-Amz-Signature=9d4ca3e447d2f99d010c55b7b222d4b75f7deb926d16a0faf7a51b8f0f0c2fcb&X-Amz-SignedHeaders=host" />
   
   7) Pindah dan Menggabungkan Branch (**Merge**)

      Pindah ke branch utama (**main/master**) dan gabungkan (**merge**) branch `fitur-kontak` ke branch utama menggunakan perintah berikut:
      ```
      git checkout main
      ```
      <img width="" height="" alt="pindah ke branch utama" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491978875-ec321449-bdbb-4134-847c-ceb8b8652fcb.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T214924Z&X-Amz-Expires=300&X-Amz-Signature=83a41b981fadc71a7ef10ffe584092b42482f403090fd3f887c1b0253cf1147c&X-Amz-SignedHeaders=host" />

      ```
      git merge fitur-kontak
      ```
      <img width="" height="" alt="merge ke branch utama" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491978956-ed57363c-f459-4cbb-a45f-83ce5ba462cc.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T215049Z&X-Amz-Expires=300&X-Amz-Signature=b5782a3474559bfa6a5d1dbe535eeaffb23370be59e9ff906d2b7fbd3cf41e1d&X-Amz-SignedHeaders=host" />
      
---

## C. Bagian 3: Integrasi dengan GitHub

   1. Membuat Repository di GitHub
      <img width="" height="" alt="create repository" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491979705-9b284bde-cdf8-47be-b58c-6d89af4a323b.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T220600Z&X-Amz-Expires=300&X-Amz-Signature=44d7747acb5d1d1ccde87375938b3fcc960f417baa17e2f6d2af9ee55fd77a88&X-Amz-SignedHeaders=host" />

   2. Menghubungkan Repository Lokal dengan GitHub
   
      1) Jalankan perintah berikut untuk menambahkan repository GitHub sebagai remote. Salin link repository GitHub.
         ```
         git remote add origin https://github.com/youraccount/your-project
         ```
         <img width="" height="" alt="git remote" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491979459-4ec37c2d-7eb4-4057-952e-ead5802c10a5.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T220120Z&X-Amz-Expires=300&X-Amz-Signature=e4773ef7ddc2684553567963609580fca1923049a771ebe8eb270363fb7568e6&X-Amz-SignedHeaders=host" />

      2) Atur nama branch utama menjadi `main`:
         ```
         git branch -M main
         ```
         <img width="" height="" alt="Ubah branch jadi main" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491979613-0f39e457-ebaf-4f74-8f31-50e6719c5121.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T220416Z&X-Amz-Expires=300&X-Amz-Signature=2160441312ce7a03b2c958b022e5607e9c44ff14c6899f4bcc64204a7e282abc&X-Amz-SignedHeaders=host" />

      3) Unggah proyek ke GitHub dengan perintah:
         ```
         git push -u origin main
         ```
         <img width="" height="" alt="git push" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491979842-b51c9e69-1f4e-4d69-a341-6e90bf488b69.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T220953Z&X-Amz-Expires=300&X-Amz-Signature=585e59419d6639dd592b110db9a00d8930e8147efa46fcd3cf161a58a485175e&X-Amz-SignedHeaders=host" />

      4) Setelah itu refresh GitHub, maka file yang sudah dibuat akan muncul di dalam repository GitHub yang sudah dibuat dan repository lokal akan terhubung dengan repository GitHub, dan seluruh file proyek akan tersedia secara online.
      
         <img width="" height="" alt="Hasil Pembuatan File di GitHub" src="https://github-production-user-asset-6210df.s3.amazonaws.com/77475645/491979920-c17c7b86-7e2b-491e-a5cb-f56be9de30ef.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250920%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250920T221230Z&X-Amz-Expires=300&X-Amz-Signature=2049ec7b3fa378dce6cb18a62c0d82ae6b3693e5eed6e8474abf922dac7632fa&X-Amz-SignedHeaders=host" />

---

## D. Bagian 4: Workflow Kerja Kelompok di GitHub (Feature Branch Workflow)

