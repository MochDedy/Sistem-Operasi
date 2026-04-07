# Laporan Praktikum Sistem Operasi Jobsheet 4

<h4>Nama : Moch Dedy Triagwi<h4>
<h4>NIM  : 254107020233<h4>
<h4>Kelas: TI-1H<h4>

## Percobaan 1: Direktory

Langkah-langkah:

1. Melihat direktori HOME

```
pwd
echo $HOME
```

![langkah1](image/cb1_1.png)

2. Melihat direktori aktual dan parent

```
pwd
cd .
pwd
cd ..
pwd
cd
```

![langkah2](image/cb1_2.png)

3. Membuat satu direktori, lebih dari satu direktori atau sub direktori

```
pwd
mkdir A B C A/D A/E B/F A/D/A
ls -l
ls -l A
ls -l A/D
```

![langkah3](image/cb1_3.png)

4. Menghapus satu atau lebih direktori hanya dapat dilakukan pada direktori kosong dan hanya dapat dihapus oleh pemiliknya kecuali bila diberikan ijin aksesnya

```
rmdir B
ls -l B
rmdir B/F B
ls -l B
```

![langkah4](image/cb1_4.png)

- Terjadi error saat rmdir B karena direktori B tidak kosong sehingga tidak bisa dihapus
- Terjadi error saat ls -l B karena direktori B sudah dihapus sehingga tidak bisa di-list

5. Navigasi direktori dengan instruksi cd untuk pindah dari satu direktori ke direktori lain.

```
pwd
ls -l
cd A
pwd
cd ..
pwd
cd /home/ddyiea/praktikum-os/week04/C
pwd
cd /ddyiea/praktikum-os/week04/C
pwd
```

![langkah5](image/cb1_5.png)

- Terjadi error karena alamat yang ditulis tidak lengkap, jika ingin menulis alamat tanpa harus menulis /home/username/ maka kita bisa menggunakan ~ sebagai pengganti dan bukannya langsung menulis /username/

## Percobaan 2: Manipulasi File

Langkah-langkah:

1. Perintah cp untuk mengkopi file atau seluruh direktori

```
cat > contoh
Membuat sebuah file
[Cntrl-d]
cp contoh contoh1
ls -l
cp contoh A
ls -l A
cp contoh contoh1 A/D
ls -l A/D
```

![langkah1](image/cb2_1.png) 2. Perintah mv untuk memindah file

```
mv contoh contoh2
ls -l
mv contoh1 contoh2 A/D
ls -l A/D
mv contoh contoh1 C
ls -l C
```

![langkah2](image/cb2_2.png)

3. Perintah rm untuk menghapus file

```
rm contoh2
ls -l
rm -i contoh
rm -rf A C
ls -l
```

![langkah3](image/cb2_3.png)

## Percobaan 3: Symbolic Link

```
echo "Hello apa khabar" > halo.txt
ls -l
ln halo.txt z
ls -l
cat z
mkdir mydir
ln z mydir/halo.juga
cat mydir/halo.juga
ln -s z bye.txt
ls -l bye.txt
cat bye.txt
```

![langkah1](image/cb3_1.png)

## Percobaan 4: Melihat Isi File

```
ls -l
file halo.txt
file bye.txt
```

![langkah1](image/cb4_1.png)

## Percobaan 5: Mencari File

1. Perintah find

```
find /home -name "*.txt" -print > myerror.txt
cat myerror.txt
find . -name "*.txt" -exec wc -l '{}' ';'
```

![langkah1](image/cb5_1.png) 2. Perintah which

```
which ls
```

![langkah2](image/cb5_2.png)

3. Perintah locate

```
locate "*.txt"
```

![langkah3](image/cb5_3.png)

## Percobaan 6: Mencari text pada file

```
grep Hallo *.txt
```

![langkah1](image/cb6_1.png)

## Latihan

1. Cobalah urutan perintah berikut:

```
cd
pwd
ls -al
cd .
pwd
cd ..
pwd
ls -al
cd ..
pwd
ls -al
cd /etc
ls -al | more
cat passwd
cd -
pwd
```

![langkah1](image/lat1_1.1.png)
![langkah2](image/lat1_1.2.png)
![langkah3](image/lat1_1.3.png)
![langkah4](image/lat1_1.4.png)

2. Lanjutkan penelusuran pohon pada sistem file menggunakan cd, ls, owd, dan cat. Telusuri direktory /bin, /usr/bin, /sbin, /tmp, dan /boot

- /bin

![langkah1](image/lat1_2.1.png)

- /usr/bin

![langkah2](image/lat1_2.2.png)

- /sbin

![langkah3](image/lat1_2.3.png)

- /tmp

![langkah4](image/lat1_2.4.png)

- /boot

![langkah5](image/lat1_2.5.png)

3. Telusuri direkoty /dev. Identifikasi perangkat yang tersedia. Identifikasi tty (terminal) Anda (ketik who am i); siapa pemilik tty Anda (gunakan ls -l)

![langkah1](image/lat1_3.1.png)
![langkah2](image/lat1_3.2.png)

4. Telusuri directory /proc. Tampilkan isi file interrupts, devices, cpuinfo, meminfo dan uptime menggunakan perintah cat. Dapatkah anda melihat mengapa directory /proc disebut pseudo-filesystem yang memungkinkan akses ke struktu data kernel?

- interrupts

![langkah1](image/lat1_4.1.png)

- devices

![langkah2](image/lat1_4.2.png)

- cpuinfo

![langkah3](image/lat1_4.3.png)

- meminfo

![langkah4](image/lat1_4.4.png)

- uptime

![langkah5](image/lat1_4.5.png)

5. Ubahlah direktory home ke user lain secara langsung menggunakan cd ~username

![langkah1](image/lat1_5.1.png)

6. Ubah kembali ke directory home anda

![langkah1](image/lat1_6.1.png)

7. Buat subdirectory work dan play

![langkah1](image/lat1_7.1.png)

8. Hapus directory work

![langkah1](image/lat1_8.1.png)

9. copy file /etc/passwd ke directory home anda

![langkah1](image/lat1_9.1.png)

10. Pindahkan ke subdirectory play

![langkah1](image/lat1_10.1.png)

11. Ubahlah ke direktory play dan buat symbolic link dengan nama terminal yang menunjuk ke perangkat tty. Apa yang terjadi jika melakukan hard link ke perangkat tty?

![langkah1](image/lat1_11.1.png)

- Akan terjadi error "Invalid cross-device link" jika melakukan hard link ke perangkat tty

12. Buatlah file bernama hello.txt yang berisi kata "hello world". Dapatkah anda gunakan "cp" menggunakan "terminal" sebagai file asal untuk menghasilkan efek yang sama

![langkah1](image/lat1_12.1.png)

13. Copy hello.txt e terminal. Apa yang terjadi?

![langkah1](image/lat1_13.1.png)

14. Masih direktory home, copy keseluruhan direktory ke direktory bernama menggunakan symbolic link.

![langkah1](image/lat1_14.1.png)

15. Hapus direktory work dan isinya dengan satu perintah

![langkah1](image/lat1_15.1.png)