Nama: MUHAMMAD FATHIR NURCHOLIS

Kelas: TI.24.A4

NIM: 312410287

Matkul: Bahasa Pemrograman

# Latihan Praktikum

<img width="570" alt="Screenshot 2024-11-19 095550" src="https://github.com/user-attachments/assets/0bcd7dc3-1cb8-4672-a2ab-b36c762177d0">

# Elemen.py

```python
list_a = [1, 2, 3, 4, 5]

print(list_a[2])

print(list_a[1:4])

print(list_a[-1])

list_a[3] = 10
print(list_a)

list_a[3:] = [11, 12, 13]
print(list_a)

list_b = list_a[:2]
print(list_b)

list_b.append("misalnya")
print(list_b)

list_b.extend([14, 15, 16])
print(list_b)

list_a.extend(list_b)
print(list_a)
```

Code Program tersebut:

<img width="210" alt="Screenshot 2024-11-19 095115" src="https://github.com/user-attachments/assets/462781d9-c671-4b27-b75d-b0034b5905b1">


hasil program tersebut:

<img width="238" alt="Screenshot 2024-11-19 095211" src="https://github.com/user-attachments/assets/bca5538b-9a02-498e-9af9-6884c4cf58e1">

# Menambah data.py

```python
class Mahasiswa:
    def __init__(self, nama, nim, nilai_tugas, nilai_uts, nilai_uas):
        self.nama = nama
        self.nim = nim
        self.nilai_tugas = nilai_tugas
        self.nilai_uts = nilai_uts
        self.nilai_uas = nilai_uas

    def hitung_nilai_akhir(self):
        return (self.nilai_tugas + self.nilai_uts + self.nilai_uas) / 3

mahasiswa = []

while True:
    nama = input("Nama: ")
    nim = int(input("NIM: "))
    nilai_tugas = int(input("Nilai Tugas: "))
    nilai_uts = int(input("Nilai UTS: "))
    nilai_uas = int(input("Nilai UAS: "))

    mahasiswa.append(Mahasiswa(nama, nim, nilai_tugas, nilai_uts, nilai_uas))

    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == "t":
        break

print("-" * 60)
print("| No | Nama       | NIM  | Tugas | UTS  | UAS  | Akhir     |")
print("-" * 60)

for i, mhs in enumerate(mahasiswa):
    nilai_akhir = mhs.hitung_nilai_akhir()
    print(f"| {i+1:<2} | {mhs.nama:<10} | {mhs.nim:<4} | {mhs.nilai_tugas:<5} | {mhs.nilai_uts:<5} | {mhs.nilai_uas:<5} | {nilai_akhir:<9.2f} |")

print("-" * 60)
```

# Penjelasan Code Menambah data

```python
class Mahasiswa:
    def __init__(self, nama, nim, nilai_tugas, nilai_uts, nilai_uas):
        self.nama = nama
        self.nim = nim
        self.nilai_tugas = nilai_tugas
        self.nilai_uts = nilai_uts
        self.nilai_uas = nilai_uas
```
`__init__`: Konstruktor ini digunakan untuk menginisialisasi objek Mahasiswa dengan atribut: `nama`, `nim`, `nilai_tugas`, `nilai_uts`, `nilai_uas`

```python
def hitung_nilai_akhir(self):
    return (self.nilai_tugas + self.nilai_uts + self.nilai_uas) / 3
```
Metode ini mengembalikan nilai akhir mahasiswa, yang merupakan rata-rata dari `nilai_tugas`, `nilai_uts`, dan `nilai_uas`.

```python
mahasiswa = []
```
Sebuah daftar kosong `mahasiswa` disiapkan untuk menyimpan objek `Mahasiswa` yang akan ditambahkan

```python
while True:
    nama = input("Nama: ")
    nim = int(input("NIM: "))
    nilai_tugas = int(input("Nilai Tugas: "))
    nilai_uts = int(input("Nilai UTS: "))
    nilai_uas = int(input("Nilai UAS: "))

    mahasiswa.append(Mahasiswa(nama, nim, nilai_tugas, nilai_uts, nilai_uas))

    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == "t":
        break
```
Meminta pengguna untuk memasukkan data mahasiswa berulang kali hingga pengguna memasukkan `t` untuk berhenti, Setiap input digunakan untuk membuat data Mahasiswa, yang kemudian ditambahkan ke dalam daftar mahasiswa

```python
print("-" * 60)
print("| No | Nama       | NIM  | Tugas | UTS  | UAS  | Akhir     |")
print("-" * 60)

for i, mhs in enumerate(mahasiswa):
    nilai_akhir = mhs.hitung_nilai_akhir()
    print(f"| {i+1:<2} | {mhs.nama:<10} | {mhs.nim:<4} | {mhs.nilai_tugas:<5} | {mhs.nilai_uts:<5} | {mhs.nilai_uas:<5} | {nilai_akhir:<9.2f} |")

print("-" * 60)
```
`Header` tabel dicetak terlebih dahulu, diikuti oleh baris-baris data untuk setiap mahasiswa, Untuk setiap mahasiswa, metode `hitung_nilai_akhir` dipanggil untuk menghitung nilai akhir, lalu data ditampilkan dalam format tabel

Code Program tersebut:

<img width="729" alt="Screenshot 2024-11-19 100705" src="https://github.com/user-attachments/assets/ce0c1715-c767-42b9-9771-d5f29851c08b">

Hasil Program tersebut:

<img width="298" alt="Screenshot 2024-11-19 100753" src="https://github.com/user-attachments/assets/ec3fb4e8-d377-41e6-b0e8-4c16e48b034c">

Dan ini flowchart nya:

<img width="271" alt="Screenshot 2024-11-19 101536" src="https://github.com/user-attachments/assets/3deaf63a-bc00-4114-b07d-c0d8c928f24a">
