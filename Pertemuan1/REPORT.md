# Laporan Praktikum Sistem Operasi Jobsheet 1

<h4>Nama : Moch Dedy Triagwi<h4>
<h4>NIM  : 254107020233<h4>
<h4>Kelas: TI-1H<h4>

## Latihan 1.10

### Latihan 1.10.1 - Latihan Konseptual

#### Latihan 1.1

Jelaskan 5 fungsi utama sistem operasi dengan contoh konkret dari minimal 2
OS berbeda (Windows, macOS, atau Linux).

#### Jawaban

Fungsi:

- Sistem operasi mengatur proses yang berjalan agar CPU digunakan secara efisien
- Membuat dan mengakhiri proses
- Mengatur komunikasi antar proses (IPC)
- Menangani multitasking
- Menentukan proses mana yang mendapatkan giliran CPU

Contoh:

- Windows -> Task Manager menampilkan daftar aplikasi dan penggunaan CPU.
- Linux -> Perintah "ps, top, dan htop" untuk melihat proses aktif

#### Latihan 1.2

Kapan sebaiknya menggunakan Windows vs Linux vs macOS? Analisis
berdasarkan use case: gaming, development, server, creative work, dan enterprise.

#### Jawaban

Berdasarkan fungsi

- Windows -> Perkantoran dan Bisnis, Gaming, Aplikasi Umum & Kompatibilitas Tinggi.
- Linux -> Server dan Cloud Computing, Development dan Programming, Sistem yang Membutuhkan Stabilitas Tinggi.
- MacOS -> Creative Work (Desain, Editing, Audio, Video), Ekosistem Apple, development iOS

### Latihan 1.10.2 Latihan Praktikal

#### Latihan 1.3

Install Ubuntu Server 22.04 LTS di VirtualBox dengan langkah berikut:

1. Download Ubuntu Server ISO dari website resmi
2. Create VM baru di VirtualBox (RAM: 2GB, Disk: 25GB)
3. Install dengan automatic partitioning (guided)
4. Buat user account dengan password yang kuat
5. Reboot dan login ke sistem
6. Dokumentasikan proses instalasi dengan screenshot key steps

#### Jawaban

1. Download Ubuntu Server
   ![Langkah 1](image/Langkah1.png "Langkah1")
2. Login menggunakan user account dan password

   ![Langkah 2](image/Langkah2.png "Langkah2")

3. Tampilan Neofetch
   ![Langkah 3](image/Langkah3.png "Langkah3")

#### Latihan 1.4

Setelah instalasi Ubuntu Server, lakukan tasks berikut:

1. Update package list: sudo apt update
2. Upgrade packages: sudo apt upgrade
3. Install neofetch: sudo apt install neofetch
4. Jalankan neofetch dan screenshot hasilnya
5. Check disk usage dengan df -h
6. Check memory dengan free -h
7. Dokumentasikan output dari setiap command

#### Jawaban

1. Langkah 1

   ![Langkah 1](image/Langkah1_1.4.png "Langkah1")

2. Langkah 2
   ![Langkah 2](image/Langkah2_1.4.png "Langkah2")
3. Langkah 3

   ![Langkah 3](image/Langkah3_1.4.png "Langkah3")

4. Langkah 4

   ![Langkah 4](image/Langkah4_1.4.png "Langkah4")

5. Langkah 5

   ![Langkah 5](image/Langkah5_1.4.png "Langkah5")

6. Langkah 6

   ![Langkah 6](image/Langkah6_1.4.png "Langkah6")

#### Latihan 1.5

Eksplorasi sistem yang baru diinstall:

1. Tampilkan informasi OS: cat /etc/os-release
2. Tampilkan versi kernel: uname -r
3. List partisi: lsblk
4. Check network connectivity: ping -c 4 google.com
5. Install dan jalankan htop untuk melihat resource usage
6. Buat laporan singkat tentang konfigurasi sistem Anda

#### Jawaban

1. Langkah 1
   ![Langkah 1](image/Langkah1_1.5.png "Langkah1")
2. Langkah 2
   ![Langkah 2](image/Langkah2_1.5.png "Langkah2")
3. Langkah 3
   ![Langkah 3](image/Langkah3_1.5.png "Langkah3")
4. Langkah 4
   ![Langkah 4](image/Langkah4_1.5.png "Langkah4")
5. Langkah 5 - Instalasi dan menjalankan htop
   ![Langkah 5](image/Langkah5_1.5.png "Langkah5")
   ![Langkah 5](image/runhtop.png "Langkah5")

6. <h4>Laporan Konfigurasi Sistem Ubuntu Server
   1. Informasi Sistem Operasi
       * Nama OS: Ubuntu
       * Versi: 24.04.4 LTS
       * Codename: Noble Numbat
       * Basis: Debian
   2. Versi Kernel
       * Kernel: 6.8.0-100-generic
   3. Konfigurasi Disk dan Partisi
       * Total Disk: 25 GB
   4. Penggunaan Penyimpanan
       * Root (/) memiliki kapasitas 12 GB
       * Digunakan: 5.1 GB
       * Sisa ruang: 5.6 GB
       * Persentase penggunaan: 48%
   5. Konfigurasi Memori (RAM dan Swap)
       * Total RAM: 1.9 GB
       * Digunakan: 340 MB
       * Tersedia: 1.6 GB
       * Swap: 2.0 GB (belum digunakan)
