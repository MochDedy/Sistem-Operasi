# Laporan Remastering Sistem Operasi

<h4>Nama    : Moch Dedy Triagwi<h4>
<h4>NIM     : 254107020233<h4>
<h4>Kelas   : TI-1H<h4>

## Pendahuluan

Remastering sistem operasi adalah proses memodifikasi distribusi Linux yang sudah ada dengan menambahkan, menghapus, atau mengubah komponen tertentu sesuai kebutuhan pengguna. Pada praktikum ini dilakukan remastering Ubuntu LTS menggunakan aplikasi Cubic (Custom Ubuntu ISO Creator).
Tujuan remastering:

1. Menambahkan aplikasi yang sering digunakan sehingga langsung tersedia setelah instalasi sistem.
2. Membuat aplikasi sederhana berbasis Bash Script sebagai bentuk kustomisasi sistem.
3. Mengubah tampilan antarmuka agar lebiih menarik dan mudah digunakan.
4. Menghasilkan file ISO baru yang siap digunakan untuk instalasi pada computer atau mesin virtual lainnya.

Melalui proses ini, pengguna dapat membuat distribusi Linux yang lebih sesuai dengan kebutuhan pekerjaan maupun pembelajaran.

## Perangkat dan Software yang Digunakan

Perangkat dan aplikasi yang digunakan dalam proses remastering adalah sebagai berikut:

1. Sistem Operasi Host : Ubuntu 26.04 LTS
2. Tool Remastering : Cubic (Custom Ubuntu ISO Creator)
3. Virtual Machine : VirtualBox
4. ISO Dasar : Ubuntu 26.04 LTS
5. RAM : 6500 MB
6. Storage : 50 GB
7. CPU : 4

## Persiapan Dasar

#### Instalasi Cubic

1. Buka terminal
   ![Langkah1](image/step1.png)
2. Pastikan paket pengelola repository tersedia:
   ![langkah2](image/step2.png)
3. Tambahkan PPA Cubic
   ![Langkah3](image/step3.png)
4. Perbarui indeks paket dan instal cubic
   ![Langkah4](image/step4.png)
5. Masuk ke CUBIC
   ![Lamgkah5](image/cubic-3.png)
6. Lakukan update terlebih dahulu
   ![Langkah6](image/cubic-4.png)
7. Lakukan installasi beberapa package Linux
   ![Langkah7](image/cubic-5.png)

## Kustomisasi dan Instalasi Aplikasi

### VLC Media Player (Pemutar Multimedia)

VLC Media Player ditambahkan sebagai aplikasi pemutar multimedia karena mampu menjalankan berbagai format audio dan video tanpa memerlukan codec tambahan.

1. Install

   ![Langka1](image/installvlc1.png)
   ![langkah2](image/installvlc.png)
2. Cek hasil download VLC

   ![Langkah3](image/cekvlc.png)

Hasil menunjukkan bahwa VLC berhasil terpasang dan dapat dijalankan melalui menu aplikasi maupun terminal.

### GIMP (Editor Gambar)

GIMP (GNU Image Manipulation Program) adalah perangkat lunak gratis dan sumber terbuka (open-source) yang digunakan untuk mengedit, memanipulasi, dan membuat grafik berbasis raster atau bitmap.

1. Install
   ![Langkah1](image/installgimp1.png)
   ![Langkah2](image/installgimp.png)
2. Cek hasil download GIMP

   ![Langkah3](image/cekgimp.png)

Hasil menunjukkan aplikasi berhasil terpasang dan dapat dijalankan dengan normal.

### Apache2 + PHP (Web server local)

Apache2 dan PHP ditambahkan untuk menyediakan lingkungan pengembangan web secara lokal. Apache2 berfungsi sebagai web server sedangkan PHP digunakan untuk menjalankan aplikasi web dinamis.

1. Install
   ![Langkah1](image/installapach1.png)
   ![Langkah2](image/installapach2_php.png)
2. Cek hasil donwload Apache 2 dan PHP

   ![Langkah3](image/cekapache.png)

3. Lakukan aktivasi apache 2
   ![Langkah4](image/aktivasiapache2.png)

Apache2 dan PHP berhasil berjalan pada sistem sehingga dapat digunakan untuk mengembangkan dan menguji aplikasi berbasis web.

### Visual Studio Code (Code Editor)

Visual Studio Code diinstal sebagai editor kode yang mendukung berbagai bahasa pemrograman dan memiliki banyak fitur untuk membantu proses pengembangan perangkat lunak.

1. Install
   
   ![Langkah1](image/installvscd1.png)
   ![Langkah2](image/installvscd2.png)
   ![Langkah3](image/installvscd3.png)
   ![Langkah4](image/installvscd4.png)
   ![Langkah5](image/installvscd5.png)
   ![Langkah6](image/installvscd6.png)

2. Berhubung Visual Studio Code saya error jadi untuk mengatasi error tersebut perlu akses mengedit file desktop dari VSCODE
   
   ![Langkah1](image/fixvscode.png)
3. Buka akses root menggunakan nano
   
   ![langkah2](image/image.png)
4. Setting pada line ke-5 yaitu EXEC tambahkan "--no-sandbox --disable-gpu"
   ![Langkah3](image/nanoVSCD.png)
5. Cek hasil download Visual Studio Code
   ![Langkah4](image/cekvscd.png)
   Pengecekan dilakukan untuk memastikan VS Code telah berhasil dipasang dan dapat dijalankan pada sistem.

### Aplikasi Custom Bash Script

Bash:

1. Informasi CPU dan RAM
   ![Langkah1](image/aplikasikustom.png)
2. Informasi Detail CPU
   ![Langkah2](image/checkcpu.png)
3. Informasi Detail RAM
   ![Langkah3](image/checkram.png)
   ![Langkah4](image/checkram2.png)
4. Informasi Detail Storage
   ![Langkah5](image/checkstorage.png)
5. Tambahkan izin eksekusi langsung
   
   ![Langkah6](image/izinEksekusi.png)

Pada tahap ini dibuat aplikasi sederhana menggunakan Bash Script. Script berfungsi untuk menampilkan informasi tertentu atau menjalankan perintah otomatis sesuai kebutuhan pengguna.
Pembuatan Bash Script bertujuan untuk menunjukkan bahwa sistem operasi hasil remastering dapat ditambahkan aplikasi buatan sendiri selain aplikasi yang berasal dari repositori

Hasil:

![Langkah7](image/hasilKustom.png)
Saat dijalankan, Bash Script berhasil menampilkan output sesuai dengan yang telah diprogram sebelumnya. Hal ini menunjukkan bahwa script telah bekerja dengan baik tanpa error.

## Kustomisasi Tampilan (Antarmuka)

### Sebelum perubahan

![1](image/wallpapersebelum.png)
![2](image/wallpapersebelum2.png)
Tampilan awal masih menggunakan konfigurasi bawaan Ubuntu dengan tema, wallpaper, dan ikon standar.

#### Melakukan Kustomisasi Wallpaper

1. Buka terminal dan buat folder untuk wallpaper
   ![1](image/folderwallpaper.png)
2. Copy wallpaper yang sudah didownload
   ![2](image/copywallpaper.png)
3. Buat folder Dconf
   
   ![3](image/folderdconf.png)
4. Copy wallpaper ke folder Cubic
   ![4](image/copywallpaperkefolder.png)
5. Lakukan Set Wallpaper
   ![5](image/setwallpaper.png)

#### Melakukan Kustomisasi Tema Sistem dan Paket Ikon

1. Install tema dan ikon yang diinginkan
   ![1](image/installtemadanIcon.png)
   ![2](image/installtemadanIcon2.png)
2. Cek Wallpaper, Tema dan Ikon
   
   ![3](image/checkwallpaper_tema.png)

### Sesudah Perubahan

![1](image/wallpapersesudah.png)
![2](image/wallpapersesudah2.png)
![3](image/wallpapersesudah3.png)

Dilakukan perubahan pada tampilan desktop seperti wallpaper, tema, ikon, maupun pengaturan antarmuka lainnya sehingga sistem memiliki tampilan yang lebih menarik dan berbeda dari Ubuntu standar. Perubahan tampilan ini bertujuan untuk meningkatkan kenyamanan pengguna sekaligus memberikan identitas khusus pada hasil remastering yang dibuat.

## Pembuatan ISO Baru

1. Setelah selesai semuanya lakukan pembuatan ISO baru
   ![1](image/ekstrakISO.png)
   ![2](image/prosesISO.png)
   ![3](image/prosesISO2.png)

Setelah seluruh proses kustomisasi selesai, sistem dibangun kembali menjadi file ISO menggunakan fitur Generate pada Cubic. Proses ini menggabungkan seluruh perubahan yang telah dilakukan ke dalam satu file instalasi baru.

Hasil akhirnya berupa file ISO remaster yang telah berisi seluruh aplikasi, konfigurasi, Bash Script, dan tampilan yang telah dimodifikasi sebelumnya.

## Kesimpulan
Berdasarkan praktikum yang telah dilakukan, proses remastering Ubuntu menggunakan Cubic berhasil dilaksanakan dengan baik. Sistem operasi berhasil dimodifikasi dengan menambahkan VLC Media Player, GIMP, Apache2, PHP, Visual Studio Code, serta aplikasi sederhana berbasis Bash Script untuk menampilkan informasi perangkat keras komputer meliputi informasi prosesor (CPU), kapasitas dan penggunaan memori (RAM), serta kapasitas ruang penyimpanan (Storage).

Selain itu, dilakukan perubahan tampilan antarmuka berupa penggantian wallpaper, tema sistem, dan paket ikon sehingga sistem memiliki tampilan yang lebih menarik dibandingkan versi bawaan. Hasil akhir berupa file ISO baru dengan nama Ubuntu-Custom-254107020233.iso yang dapat digunakan untuk instalasi sistem operasi dengan seluruh aplikasi dan konfigurasi yang telah disiapkan sebelumnya.

Melalui praktikum ini diperoleh pemahaman mendalam mengenai proses remastering Linux, pengelolaan paket aplikasi menggunakan apt, kustomisasi tampilan sistem, pembuatan skrip Bash, serta pembuatan distribusi Linux sesuai kebutuhan pengguna.
