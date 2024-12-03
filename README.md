# labpy06-labpy07

Nama        : M.Ridho Febrian <p>

Kelas       : TI.24.A.5 <p>

Nim         : 312410500 <p>

Mata kuliah : Bahasa Pemrograman <p>

# Praktikum 6 

# Program daftar nilai Mahasiswa

Pada praktikum 6, kita akan membuat program sederhana dengan mengaplikasikan penggunaan fungsi
yang akan menampilkan daftar nilai mahasiswa,

#### Codingan Praktikum 6

# Daftar untuk menyimpan data mahasiswa
```python
daftar_mahasiswa = []

def tambah(nama, nilai):
    """Fungsi untuk menambah data mahasiswa."""
    mahasiswa = {'nama': nama, 'nilai': nilai}
    daftar_mahasiswa.append(mahasiswa)
    print(f"Data mahasiswa {nama} telah ditambahkan.")

def tampilkan():
    """Fungsi untuk menampilkan data mahasiswa."""
    if not daftar_mahasiswa:
        print("Tidak ada data mahasiswa.")
        return
    print("\nDaftar Mahasiswa:")
    for mahasiswa in daftar_mahasiswa:
        print(f"Nama: {mahasiswa['nama']}, Nilai: {mahasiswa['nilai']}")

def hapus(nama):
    """Fungsi untuk menghapus data mahasiswa berdasarkan nama."""
    global daftar_mahasiswa
    daftar_mahasiswa = [mahasiswa for mahasiswa in daftar_mahasiswa if mahasiswa['nama'] != nama]
    print(f"Data mahasiswa dengan nama {nama} telah dihapus.")

def ubah(nama, nilai_baru):
    """Fungsi untuk mengubah data mahasiswa berdasarkan nama."""
    for mahasiswa in daftar_mahasiswa:
        if mahasiswa['nama'] == nama:
            mahasiswa['nilai'] = nilai_baru
            print(f"Data mahasiswa {nama} telah diubah menjadi nilai {nilai_baru}.")
            return
    print(f"Mahasiswa dengan nama {nama} tidak ditemukan.")

# penggunaan fungsi
tambah("ridho", 85)
tambah("bagus", 90)
tambah("kia", 78)

tampilkan()

ubah("ridho", 88)
tampilkan()

hapus("bagus")
tampilkan()
```

#### Penjelasan Kode Program
```python
# Daftar untuk menyimpan data mahasiswa
daftar_mahasiswa = []
```
`daftar_mahasiswa`: Ini adalah list kosong yang akan digunakan untuk menyimpan data mahasiswa. Setiap mahasiswa akan disimpan sebagai dictionary yang berisi nama dan nilai.

#### Fungsi `tambah(nama, nilai)`
```python
def tambah(nama, nilai):
    """Fungsi untuk menambah data mahasiswa."""
    mahasiswa = {'nama': nama, 'nilai': nilai}
    daftar_mahasiswa.append(mahasiswa)
    print(f"Data mahasiswa {nama} telah ditambahkan.")
```
Parameter: Fungsi ini menerima dua parameter, `nama` dan `nilai`, yang merupakan informasi yang akan ditambahkan untuk mahasiswa baru.
Dictionary: Di dalam fungsi, sebuah dictionary `mahasiswa` dibuat dengan kunci 'nama' dan 'nilai'.
Menambahkan ke List: Dictionary mahasiswa ditambahkan ke dalam list daftar_mahasiswa menggunakan metode `append()`.
Output: Fungsi ini mencetak pesan konfirmasi bahwa data mahasiswa telah ditambahkan.


#### Fungsi `tampilkan()`
```python
def tampilkan():
    """Fungsi untuk menampilkan data mahasiswa."""
    if not daftar_mahasiswa:
        print("Tidak ada data mahasiswa.")
        return
    print("\nDaftar Mahasiswa:")
    for mahasiswa in daftar_mahasiswa:
        print(f"Nama: {mahasiswa['nama']}, Nilai: {mahasiswa['nilai']}")
```

Pengecekan Kosong: Fungsi ini pertama-tama memeriksa apakah `daftar_mahasiswa` kosong. Jika kosong, akan mencetak pesan bahwa tidak ada data mahasiswa.

Menampilkan Data: Jika ada data, fungsi ini mencetak "Daftar Mahasiswa:" dan kemudian melakukan iterasi melalui setiap mahasiswa dalam list. Untuk setiap mahasiswa, ia mencetak nama dan nilai menggunakan format string.

#### Fungsi `hapus(nama)`
```python
def hapus(nama):
    """Fungsi untuk menghapus data mahasiswa berdasarkan nama."""
    global daftar_mahasiswa
    daftar_mahasiswa = [mahasiswa for mahasiswa in daftar_mahasiswa if mahasiswa['nama'] != nama]
    print(f"Data mahasiswa dengan nama {nama} telah dihapus.")
```

Parameter: Fungsi ini menerima satu parameter, `nama`, yang merupakan nama mahasiswa yang ingin dihapus.

List Comprehension: Fungsi ini menggunakan list comprehension untuk membuat list baru yang hanya berisi mahasiswa yang tidak memiliki nama yang sama dengan parameter `nama`. Ini secara efektif menghapus mahasiswa yang diinginkan dari `daftar_mahasiswa`.
Output: Fungsi ini mencetak pesan konfirmasi bahwa data mahasiswa telah dihapus.

#### Fungsi `ubah(nama, nilai_baru)`
```python
def ubah(nama, nilai_baru):
    """Fungsi untuk mengubah data mahasiswa berdasarkan nama."""
    for mahasiswa in daftar_mahasiswa:
        if mahasiswa['nama'] == nama:
            mahasiswa['nilai'] = nilai_baru
            print(f"Data mahasiswa {nama} telah diubah menjadi nilai {nilai_baru}.")
            return
    print(f"Mahasiswa dengan nama {nama} tidak ditemukan.")
```

Parameter: Fungsi ini menerima dua parameter, `nama` dan `nilai_baru`, yang merupakan nama mahasiswa yang ingin diubah dan nilai baru yang akan diberikan.
Iterasi: Fungsi ini melakukan iterasi melalui setiap mahasiswa dalam `daftar_mahasiswa`. Jika nama mahasiswa cocok dengan parameter nama, nilai mahasiswa diubah menjadi `nilai_baru`.
Output: Jika mahasiswa ditemukan dan nilainya diubah, fungsi mencetak pesan konfirmasi. Jika tidak ditemukan, fungsi mencetak pesan bahwa mahasiswa tidak ditemukan.


#### Penggunaan Fungsi

```python
#  penggunaan fungsi
tambah("ridho", 85)
tambah("bagus", 90)
tambah("kia", 78)

tampilkan()

ubah("ridho", 88)
tampilkan()

hapus("bagus")
tampilkan()
```
Menambah Data: Tiga mahasiswa ditambahkan dengan memanggil fungsi `tambah()`.

Menampilkan Data: Fungsi `tampilkan()` dipanggil untuk menampilkan semua data mahasiswa yang telah ditambahkan.

Mengubah Data: Fungsi `ubah()` dipanggil untuk mengubah nilai mahasiswa "ridho" menjadi 88.

Menghapus Data: Fungsi `hapus()` dipanggil untuk menghapus mahasiswa "bagus" dari daftar.

Menampilkan Data Setelah Modifikasi: Fungsi `tampilkan()` dipanggil lagi untuk menunjukkan daftar mahasiswa setelah pengubahan dan penghapusan data.


### Tampilan Program Saat Dijalankan

###  1. Setelah menambahkan mahasiswa:
![tambah](https://github.com/user-attachments/assets/63ceff99-f133-4a2c-b154-021771e7ba18)


###  2. Setelah menampilkan data:
![tampilan](https://github.com/user-attachments/assets/c1f54b47-0127-46a0-846d-60dd78ea4298)


###  3. Setelah mengubah nilai mahasiswa:
![ubah](https://github.com/user-attachments/assets/f91dab11-5d7d-4012-9b31-0dbfc43d08e9)


###  4. Setelah menampilkan data lagi:
![tampilan](https://github.com/user-attachments/assets/da1393fc-f4fc-4ac1-be67-55ce8db3e61f)


###  5. Setelah menghapus mahasiswa:
![hapus](https://github.com/user-attachments/assets/07b80b70-cc55-40ca-b867-924dfa81c2f3)


###  6. Setelah menampilkan data terakhir:
![tampilan](https://github.com/user-attachments/assets/700ddac0-7a29-4b65-8aed-68ee4ccb7b5b)








## inilah flowchart saya dan penjelasan nya:
![flowchart](https://github.com/user-attachments/assets/8f5ca538-0c24-4a8c-89a7-76cdee0d05dd)

### penjelasan:
1. Mulai

2. Inisialisasi `daftar_mahasiswa` sebagai list kosong.

3. Fungsi `tambah(nama, nilai)`

-Input: `nama, nilai`

-Buat dictionary `mahasiswa` dengan `nama` dan `nilai`.

-Tambahkan `mahasiswa` ke `daftar_mahasiswa`.

-Tampilkan pesan: "Data mahasiswa {nama} telah ditambahkan."

4. Fungsi `tampilkan()`

-Jika `daftar_mahasiswa` kosong:

  Tampilkan pesan: "Tidak ada data mahasiswa."

-Jika tidak kosong:Tampilkan "Daftar Mahasiswa:"

  Untuk setiap `mahasiswa` di `daftar_mahasiswa`, tampilkan `nama` dan `nilai`.

5. Fungsi `hapus(nama)`

-Hapus `mahasiswa` dari `daftar_mahasiswa` yang `nama`-nya sama dengan input `nama`.

-Tampilkan pesan: "Data mahasiswa dengan nama {nama} telah dihapus."

6. Fungsi `ubah(nama, nilai_baru)`

-Untuk setiap `mahasiswa` di `daftar_mahasiswa`:

 Jika `mahasiswa['nama']` sama dengan `nama`:

   Ubah `mahasiswa['nilai']` menjadi `nilai_baru`.

Tampilkan pesan: "Data mahasiswa {nama} telah diubah menjadi nilai {nilai_baru}."

Keluar dari fungsi.

Jika tidak ditemukan:

Tampilkan pesan: "Mahasiswa dengan nama {nama} tidak ditemukan."

7. Penggunaan Fungsi

-Panggil `tambah("ridho", 85)`

-Panggil `tambah("bagus", 90)`

-Panggil `tambah("kia", 78)`

-Panggil `tampilkan()`

-Panggil `ubah("ridho", 88)`

-Panggil `tampilkan()`

-Panggil `hapus("bagus")`

-Panggil `tampilkan()`

8. Selesai




