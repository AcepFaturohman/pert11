## LATIHAN
## INPUT
```
# Dictionary untuk menyimpan data mahasiswa
data_mahasiswa = {}

# Fungsi untuk menambah data mahasiswa
def tambah(nama, nilai):
    if nama in data_mahasiswa:
        print(f"Data dengan nama {nama} sudah ada!")
    else:
        data_mahasiswa[nama] = nilai
        print(f"Data {nama} berhasil ditambahkan.")

# Fungsi untuk menampilkan data mahasiswa
def tampilkan():
    if not data_mahasiswa:
        print("Tidak ada data yang tersimpan.")
    else:
        print("Daftar Nilai Mahasiswa:")
        for nama, nilai in data_mahasiswa.items():
            print(f"Nama: {nama}, Nilai: {nilai}")

# Fungsi untuk menghapus data mahasiswa berdasarkan nama
def hapus(nama):
    if nama in data_mahasiswa:
        del data_mahasiswa[nama]
        print(f"Data {nama} berhasil dihapus.")
    else:
        print(f"Data dengan nama {nama} tidak ditemukan.")

# Fungsi untuk mengubah data mahasiswa berdasarkan nama
def ubah(nama, nilai_baru):
    if nama in data_mahasiswa:
        data_mahasiswa[nama] = nilai_baru
        print(f"Data {nama} berhasil diubah.")
    else:
        print(f"Data dengan nama {nama} tidak ditemukan.")

# Program utama
print("Program Pengelolaan Data Nilai Mahasiswa")
while True:
    print("\nPilih opsi:")
    print("1. Tambah Data")
    print("2. Tampilkan Data")
    print("3. Hapus Data")
    print("4. Ubah Data")
    print("5. Keluar")
    
    pilihan = input("Masukkan pilihan (1-5): ")
    
    if pilihan == "1":
        nama = input("Masukkan nama mahasiswa: ")
        nilai = int(input("Masukkan nilai mahasiswa: "))
        tambah(nama, nilai)
    elif pilihan == "2":
        tampilkan()
    elif pilihan == "3":
        nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
        hapus(nama)
    elif pilihan == "4":
        nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
        nilai_baru = int(input("Masukkan nilai baru: "))
        ubah(nama, nilai_baru)
    elif pilihan == "5":
        print("Program selesai.")
        break
    else:
        print("Pilihan tidak valid!")
```
## OUTPUT

```
Program Pengelolaan Data Nilai Mahasiswa

Pilih opsi:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Masukkan pilihan (1-5): 1
Masukkan nama mahasiswa: FATUR ROHMAN
Masukkan nilai mahasiswa: 97
Data FATUR ROHMAN berhasil ditambahkan.

Pilih opsi:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Masukkan pilihan (1-5): 2
Daftar Nilai Mahasiswa:
Nama: FATUR ROHMAN, Nilai: 97

Pilih opsi:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Masukkan pilihan (1-5): 4
Masukkan nama mahasiswa yang ingin diubah: FATUR ROHMAN
Masukkan nilai baru: 100
Data FATUR ROHMAN berhasil diubah.

Pilih opsi:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Masukkan pilihan (1-5): 2
Daftar Nilai Mahasiswa:
Nama: FATUR ROHMAN, Nilai: 100

Pilih opsi:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Masukkan pilihan (1-5): 3
Masukkan nama mahasiswa yang ingin dihapus: FATUR ROHMAN
Data FATUR ROHMAN berhasil dihapus.

Pilih opsi:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Masukkan pilihan (1-5): 2
Tidak ada data yang tersimpan.

Pilih opsi:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Masukkan pilihan (1-5): 5
Program selesai.

```

## PENJELASAN

#1.Tambah Data:
Data mahasiswa bernama FATUR ROHMAN dengan nilai 97 berhasil ditambahkan.

#2.Tampilkan Data:
Program menampilkan daftar nilai mahasiswa yang tersimpan.

#3.Ubah Data:
Nilai FATUR ROHMAN diubah dari 97 menjadi 100.

#4.Hapus Data:
Data FATUR ROHMAN dihapus dari daftar.

#5.Cek Data:
Setelah dihapus, tidak ada data yang tersimpan.

#6.Keluar:
Program selesai dijalankan.

## FLOWCHART
```mermaid
flowchart TD
    A([Start]) --> B[/User Input/]
    B -->|'T'| C[/Tambah Data/]
    B -->|'U'| D[/Ubah Data/]
    B -->|'H'| E[/Hapus Data/]
    B -->|'L'| F[/Lihat Data/]
    B -->|'K'| G([End])
    
    C --> H{Data Valid?}
    H -->|Yes| I[/Tambahkan ke data_mahasiswa/]
    H -->|No| J[/Tampilkan Pesan Kesalahan/]
    I --> B
    J --> B
    
    D --> K{Nama Ditemukan?}
    K -->|Yes| L[/Tampilkan Data Lama/]
    K -->|No| M[/Tampilkan 'Nama Tidak Ditemukan'/]
    L --> N[/Input Data Baru/]
    N --> O[/Perbarui Data/]
    O --> B
    M --> B
    
    E --> P{Data Kosong?}
    P -->|Yes| Q[/Kembali ke Menu/]
    P -->|No| R{Nama Ditemukan?}
    R -->|Yes| S[/Hapus Data/]
    R -->|No| T[/Tampilkan 'Nama Tidak Ditemukan'/]
    S --> B
    T --> B
    Q --> B
    
    F --> U{Ada Data?}
    U -->|Yes| V[/Tampilkan Tabel Data/]
    U -->|No| W[/Tampilkan 'Tidak Ada Data'/]
    V --> B
    W --> B
    
    G --> X([Selesai])
```

