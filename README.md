

# Studio Grafika 2D/3D Sederhana

Proyek ini adalah sebuah aplikasi grafika komputer sederhana yang dibangun menggunakan Python dengan pustaka PyOpenGL. Aplikasi ini memungkinkan pengguna untuk menggambar berbagai objek 2D, melakukan transformasi pada objek tersebut, serta menampilkan dan memanipulasi sebuah kubus 3D dalam satu jendela.

Aplikasi ini menggabungkan rendering 2D ortografis dan 3D perspektif, dengan sistem kontrol interaktif melalui keyboard dan mouse.

## Fitur Utama

  * **Mode Ganda 2D/3D:** Menggambar objek 2D dan menampilkan objek 3D secara bersamaan.
  * **Menggambar Objek 2D:** Mendukung pembuatan titik, garis, persegi, dan elips.
  * **Transformasi Objek 2D:**
      * **Seleksi:** Pilih objek untuk ditransformasi.
      * **Translasi:** Geser objek ke atas, bawah, kiri, atau kanan.
      * **Rotasi:** Putar objek pada poros tengahnya.
      * **Skala:** Perbesar ukuran objek dari titik tengahnya.
  * **Clipping Garis 2D:** Implementasi algoritma **Cohen-Sutherland** untuk memotong garis yang berada di luar area kliping yang ditentukan pengguna.
  * **Manipulasi Objek 3D:**
      * Tampilkan/sembunyikan kubus 3D.
      * **Translasi Manual:** Gerakkan kubus pada sumbu X, Y, dan Z.
      * **Rotasi Manual:** Putar kubus pada sumbu X, Y, dan Z.
      * **Rotasi Otomatis:** Aktifkan/nonaktifkan animasi putaran (spin) kubus pada sumbu Y.
  * **Kontrol Kamera 3D:** Zoom in dan zoom out pada scene 3D.
  * **Kontrol Interaktif:** Semua fungsi dikontrol melalui input keyboard dan klik mouse yang intuitif.

## Prasyarat

Sebelum menjalankan aplikasi, pastikan Anda telah menginstal pustaka yang diperlukan. Anda dapat menginstalnya menggunakan `pip`:

```bash
pip install PyOpenGL PyOpenGL-accelerate
```

## Cara Menjalankan

Simpan kode di atas sebagai file Python (misalnya, `studio_grafika.py`) dan jalankan melalui terminal atau command prompt:

```bash
python studio_grafika.py
```

## Panduan Penggunaan

### Kontrol Mouse

  * **Klik Kiri:** Digunakan untuk menggambar objek atau menentukan titik.
      * Dalam mode **gambar titik/persegi/elips**, satu klik akan membuat objek di posisi kursor.
      * Dalam mode **gambar garis**, klik pertama menentukan titik awal dan klik kedua menentukan titik akhir.
      * Dalam mode **area kliping**, klik pertama menentukan sudut pertama dan klik kedua menentukan sudut kedua dari area kliping.

### Kontrol Keyboard

#### Mode Menggambar & Umum

  * `1`: Mode menggambar **Titik**.
  * `2`: Mode menggambar **Garis**.
  * `3`: Mode menggambar **Persegi**.
  * `4`: Mode menggambar **Elips**.
  * `5`: Mode menentukan **Area Klipping** (menghapus area kliping lama jika ada).

#### Pengaturan Visual 2D

  * `r`: Ubah warna gambar menjadi **Merah**.
  * `g`: Ubah warna gambar menjadi **Hijau**.
  * `b`: Ubah warna gambar menjadi **Biru**.
  * `d`: Kembalikan warna ke **Default** (hitam).
  * `+`: **Tambah** ketebalan garis/ukuran titik.
  * `-`: **Kurangi** ketebalan garis/ukuran titik.

#### Kontrol Objek 2D (Seleksi & Transformasi)

1.  Gambar beberapa objek terlebih dahulu.
2.  Gunakan `k` (sebelumnya) dan `l` (berikutnya) untuk memilih objek. Objek yang terpilih akan ditransformasi.

<!-- end list -->

  * `k`: Pilih objek **sebelumnya** dalam daftar.
  * `l`: Pilih objek **berikutnya** dalam daftar.
  * `t`: Aktifkan mode **Translasi** untuk objek terpilih.
      * `y`: Geser ke atas.
      * `h`: Geser ke kiri.
      * `j`: Geser ke bawah.
      * `u`: Geser ke kanan.
  * `o`: Aktifkan mode **Rotasi** untuk objek terpilih.
      * `q`: Putar objek sebesar 5 derajat.
  * `S` (Shift + s): Aktifkan mode **Skala** (perbesar) untuk objek terpilih.
  * `c`: **Hapus/Reset** semua transformasi aktif pada objek terpilih.

#### Kontrol Objek 3D (Kubus)

  * `v`: **Tampilkan/Sembunyikan** kubus 3D.
  * `[` / `]`: Translasi kubus ke **kiri/kanan** (sumbu X).
  * `p` / `;`: Translasi kubus ke **atas/bawah** (sumbu Y).
  * `.` / `/`: Translasi kubus **mendekat/menjauh** (sumbu Z).
  * `f`: Rotasi manual pada sumbu **X**.
  * `g`: Rotasi manual pada sumbu **Y**.
  * `H` (Shift + h): Rotasi manual pada sumbu **Z**.
  * `A` (Shift + a): **Aktifkan/Nonaktifkan rotasi otomatis** (spin) pada sumbu Y.
  * `0`: **Reset** posisi dan rotasi kubus ke keadaan semula.

#### Kontrol Kamera 3D

  * `Panah Atas`: **Zoom In** (mendekatkan kamera).
  * `Panah Bawah`: **Zoom Out** (menjauhkan kamera).
