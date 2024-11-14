# README.md.
# TUGAS BAHASA PEMROGRAMAN P9

![Screenshot 2024-11-14 132334](https://github.com/user-attachments/assets/96033272-621b-4f3b-b61d-1a60d3d98d81)

# Penjelasannya:
# 1. Deklarasi Daftar Mahasiswa
    mahasiswa = []
Di sini, sebuah daftar kosong bernama `mahasiswa` dideklarasikan untuk menyimpan data siswa yang akan diinput.

# 2.  Fungsi `hitung_nilai_akhir`
    def hitung_nilai_akhir(tugas, uts, uas):
    return (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)

Fungsi ini menerima nilai `tugas`, `uts`, dan `uas` sebagai parameter, kemudian mengembalikan nilai akhir berdasarkan bobot yg ditentukan:
   - Tugas: 30%
   - UTS: 35%
   - UAS: 35%

# 3. Input Data Mahasiswa
    while True:
    # Input data mahasiswa
    nama = input("Masukkan Nama: ")
    nim = input("Masukkan NIM: ")
    tugas = float(input("Nilai Tugas: "))
    uts = float(input("Nilai UTS: "))
    uas = float(input("Nilai UAS: "))

Program menggunakan loop  `while True` untuk terus meminta input dari pengguna. Pengguna diminta untuk memasukkan nama, NIM, dan nilai tugas, UTS, serta UAS. Nilai yang dimasukkan untuk tugas, UTS, dan UAS diubah menjadi tipe `float` untuk memungkinkan perhitungan desimal.

# 4. Menghitung Nilai Akhir
    nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)

Setelah mendapatkan masukan, program memanggil fungsi `hitung_nilai_akhir` untuk menghitung nilai akhir berdasarkan nilai yang diinputkan.

# 5. Menyimpan Data Mahasiswa
     data = {
          'nama': nama,
          'nim': nim,
          'tugas': tugas,
          'uts': uts,
          'uas': uas,
          'nilai_akhir': nilai_akhir
      }
       mahasiswa.append(data)

Data siswa yang telah diinput dan dihitung disimpan dalam bentuk kamus, kemudian ditambahkan ke dalam list `mahasiswa`.

# 6. Menanyakan Input Lanjutan
     lanjut = input("Tambah data (y/t)? ")
     if lanjut.lower() == 't':
        break

Setelah menyimpan data, program menanyakan kepada pengguna apakah ingin menambah data siswa lagi. Jika pengguna menjawab 't' (tidak), program akan keluar dari loop.

# 7. Menampilkan Data Mahasiswa
    print("\nDaftar Nilai Mahasiswa")
    print("="*80)
    print("{:<20} {:<15} {:<10} {:<10} {:<10} {:<10}".format(
        "Nama", "NIM", "Tugas", "UTS", "UAS", "Nilai Akhir"))
    print("-"*80)

    for data in mahasiswa:
        print("{:<20} {:<15} {:<10} {:<10} {:<10} {:<10.2f}".format(
            data['nama'],
            data['nim'],
            data['tugas'],
            data['uts'],
            data['uas'],
            data['nilai_akhir']
         ))
     print("="*80)

Setelah semua data diinput, program akan menampilkan daftar semua siswa yang telah dimasukkan beserta nilai-nilai mereka. Data ditampilkan dalam format tabel yang terstruktur.

# Kesimpulan
Program ini adalah contoh sederhana dari sistem manajemen data siswa yang dapat digunakan untuk menginput, menghitung, dan menampilkan nilai akhir siswa. Program ini dapat dikembangkan lebih lanjut dengan menambahkan fitur seperti validasi input, penyimpanan ke file, atau pengeditan data.
