# TUGAS PRAKTIKUM PERTAMA: INSTALASI GIT DAN INTEGRASI GITHUB

## 📃 Identitas Diri

- **Nama**             : Revalina Adelia
- **NPM**              : 4523210091
- **Mata Kuliah**      : Pemrograman Berbasis Web (A)
- **Dosen Pengampu**   : Adi Wahyu Pribadi, S.Si., M.Kom.

## A. Bagian 1: Instalasi & Konfigurasi Awal Git dengan Windows

1. Instalasi Git di Windows

   Git adalah system control versi terdistribusi yang pertama kali diciptakan dan dikembangkan oleh Linus Torvalds serta digunakan untuk mengelola kode program. Berikut langkah-langkah instalasi Git pada sistem operasi Windows:

   1)	Buka Google Chrome (atau browser lain) lalu ketikkan kata kunci “Git download” di kolom pencarian.

      ![Search Git Download](https://github.com/user-attachments/assets/7826a075-8d7c-4f3e-80e5-a6a9eb2b336c)

   2)	Dari hasil pencarian, pilih halaman resmi “Git Downloads” atau juga bisa langsung membuka tautan berikut https://git-scm.com/download/win.

      ![Halaman Resmi Git Download](https://github.com/user-attachments/assets/12785844-d7ce-4e28-8fa5-6749cd7617b3)

   3)	Setelah halaman terbuka, sistem akan menampilkan beberapa pilihan instalasi sesuai dengan sistem operasi. Karena saya menggunakan Windows, pilih opsi Windows kemudian pilih Windows/x64 Setup. File installer akan otomatis terunduh ke laptop.

      ![Git Download pada Windows](https://github.com/user-attachments/assets/953dbd17-8dda-4f21-8074-f5301f2349a3)

      ![Pilih Windows x64 Setup](https://github.com/user-attachments/assets/f6ffa3b3-893b-4da9-ab55-e0e4e709fd81)

   4)	Tunggu hingga proses unduhan selesai, kemudian buka file installer dengan cara mengklik tanda panah kotak pada hasil unduhan tersebut.

      ![Jalankan File  exe](https://github.com/user-attachments/assets/8f97f147-27ad-48a5-aa10-1b51c2589297)

   5)	Jendela instalasi Git akan muncul. Ikuti langkah-langkah instalasi dengan mengklik tombol Install dan Next pada setiap tahap hingga proses selesai, lalu akhiri dengan mengklik Finish.

      ![Pilih Install pada Hasil Download](https://github.com/user-attachments/assets/1909a291-4335-4778-8b48-8cbe84b36c6c)

      ![Klik Finish setelah Install](https://github.com/user-attachments/assets/e7e41254-b3b3-402e-a532-f8f5e082fe30)

   6)	Untuk memastikan Git sudah berhasil terpasang, buka Command Prompt melalui menu Search di Windows, kemudian ketikkan perintah berikut:

     	git --version

      <img width="920" height="952" alt="Buka Command Prompt" src="https://github.com/user-attachments/assets/ebb087e1-01f5-4769-8b95-79f7b76a7ce8" />

      <img width="590" height="164" alt="Mengecek Versi Git" src="https://github.com/user-attachments/assets/7eb9c273-a61d-4193-a718-40e4cde65df0" />

3. Konfigurasi Awal (Wajib)

   Setelah Git berhasil diinstall, langkah berikutnya adalah melakukan konfigurasi awal. Konfigurasi ini bertujuan agar setiap perubahan yang dibuat dapat tercatat dengan identitas berupa nama pengguna dan alamat email yang sesuai.

   1) Lanjutkan di Command Prompt dengan mengetikkan perintah berikut untuk mengatur nama pengguna. Perintah ini berfungsi untuk menyimpan nama pengguna secara global pada Git.

      git config --global user.name Revalina Adelia

      <img width="759" height="33" alt="Konfigurasi Nama" src="https://github.com/user-attachments/assets/b4cba844-d411-47a3-bcda-f11a7ecb6c21" />

   3) Setelah itu, atur alamat email yang akan digunakan dengan perintah berikut.

       git config --global user.email revalina4523091@univpancasila.ac.id

      <img width="992" height="32" alt="Konfigurasi Email" src="https://github.com/user-attachments/assets/4d23975f-b60f-4a62-aa79-15191f8efaba" />


## B. Bagian 2: Alur Kerja Dasar Git (Lokal)

1. Membuat Proyek Baru dan Inisialisasi Git

    1) Buka File Explorer, kemudian buat folder baru dengan nama “tugas-proyek-web”. Pada contoh ini, folder dibuat dalam direktori Documents.

      <img width="519" height="38" alt="Membuat Folder tugas-proyek-web" src="https://github.com/user-attachments/assets/7c0498b3-c39b-4992-b05d-4f488244b709" />

   2) Setelah folder dibuat, buka Command Prompt dan jalankan perintah berikut secara satu persatu.

      mkdir proyek-web

      cd proyek-web

      git init

      <img width="903" height="163" alt="Buat Folder dan Inisialisasi Git" src="https://github.com/user-attachments/assets/893510c4-8da4-45c0-ad32-52ee632d8cc4" />

3. Membuat Beberapa File

   Buat beberapa file awal untuk proyek dengan menjalankan perintah berikut satu per satu:

   echo “<h1>Selamat Datang</h1>” > index.html

   mkdir css

   echo “body { font-family: sans-serif; }” > css/style.css

   <img width="1085" height="155" alt="Membuat Beberapa File" src="https://github.com/user-attachments/assets/a31a2591-cc40-447c-9690-0dc6cf34b644" />

   Setelah perintah dijalankan, folder proyek akan berisi dua file HTML (index.html dan kontak.html) dan satu folder CSS (css) dengan file style.css di dalamnya.

4. Mengecek Status dan Masuk ke Staging Area

   Setelah file proyek dibuat, kita perlu menyimpannya ke dalam version control Git. Proses ini dilakukan melalui dua tahap, yaitu pengecekan status dan menambahkan file ke staging area.

   1) Cek status repository dengan perintah di bawah ini. Perintah ini akan menampilkan file apa saja yang belum dicatat oleh Git.
    
      git status

      <img width="580" height="248" alt="Mengecek Status Repository" src="https://github.com/user-attachments/assets/eaa1fae9-86f4-4074-8206-632095c56545" />

   2) Tambahkan semua file ke staging area menggunakan perintah berikut ini. Titik (.) berarti semua file di dalam folder tersebut akan dimasukkan ke staging area.
    
      git add .

      <img width="513" height="42" alt="Menambahkan Semua File ke Staging Area" src="https://github.com/user-attachments/assets/6867226f-99a0-4ac1-9864-0db4351f9f82" />

6. Menyimpan Perubahan (Commit)

   Simpan perubahan tersebut dengan commit. Teks di dalam tanda kutip merupakan pesan commit, yang menjelaskan perubahan yang dilakukan. 

   git commit -m “feat: Inisialisasi proyek dengan file index dan css”

  <img width="1226" height="123" alt="Menyimpan Perubahan (Commit)" src="https://github.com/user-attachments/assets/4b8024a6-8802-4a80-8eaa-df67d3ae760e" />

5. Membuat Branch dan File Baru di Branch
 
   1) Buat branch baru dengan nama fitur-kontak: 

       git checkout -b fitur-kontak

      <img width="751" height="61" alt="Buat Branch fitur-kontak" src="https://github.com/user-attachments/assets/b6ee52e3-692d-4c76-a585-19c2945f54c9" />

   3) Tambahkan file baru bernama kontak.html dengan perintah: 

      echo “<h1>Halaman Kontak</h1>” > kontak.html

      <img width="932" height="37" alt="File kontak html" src="https://github.com/user-attachments/assets/d0357c9d-0416-4c57-826f-6f87ff5d1fc2" />

   5) Untuk membuka proyek di Visual Studio Code, jalankan code . Visual Studio Code akan menampilkan proyek beserta semua file (index.html, style.css, dan kontak.html).

      <img width="479" height="42" alt="Melihat Visual Studio Code" src="https://github.com/user-attachments/assets/55a9f9d5-6959-42ae-801e-c93a1dab0d8c" />

6. Melakukan Staging dan Commit di Branch

   Tambahkan file baru ke staging area dan simpan dengan commit:

   git add .

   git commit -m “feat: Menambahkan halaman kontak”

  <img width="998" height="151" alt="Melakukan Staging dan Commit di Branch" src="https://github.com/user-attachments/assets/7012e329-0747-4147-aa58-9409f41780cd" />

7. Menggabungkan Branch (Merge)

   1) Pindah ke branch utama. Jika branch main belum dibuat, gunakan master:

       git checkout master

      <img width="653" height="64" alt="Merge Master" src="https://github.com/user-attachments/assets/b9b7b923-72ec-47a0-8fac-ce43afd3015c" />

   3) Lakukan merge branch fitur-kontak ke branch utama:

      git merge fitur-kontak

      <img width="687" height="156" alt="Merge Branch fitur-kontak" src="https://github.com/user-attachments/assets/f56c649e-f127-4ab9-b24a-cb62dfb2e4fc" />

## C. Bagian 3: Integrasi dengan GitHub

1. Membuat Repository di GitHub

2. Menghubungkan Repository Lokal dengan GitHub
 
   1) Jalankan perintah berikut untuk menambahkan repository GitHub sebagai remote. Salin link repository GitHub.
    
      git remote add origin https://github.com/revalinaadelia/tugas-proyek-web-pertama.git
      
   3) Atur nama branch utama menjadi main:

      git branch -M main
      
   5) Unggah proyek ke GitHub dengan perintah:

      git push -u origin main
      
   7) Setelah itu refresh GitHub, maka file yang sudah dibuat akan muncul di dalam repository GitHub yang sudah dibuat.

   Setelah perintah terakhir dijalankan, repository lokal akan terhubung dengan repository GitHub, dan seluruh file proyek akan tersedia secara online.
   
   <img width="1420" height="359" alt="Menghubungkan Repositori Lokal dengan GitHub" src="https://github.com/user-attachments/assets/e7c072bb-b29e-4f86-b7c1-2ffc397e0797" />
   
   <img width="1898" height="615" alt="Hasil Pembuatan File di GitHub" src="https://github.com/user-attachments/assets/7b38cb18-9a15-450b-985a-60fd9ec7ef34" />



