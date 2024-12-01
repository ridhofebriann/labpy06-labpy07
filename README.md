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

### inilah tambah,tampilan,ubah,hapus:
![hasil](https://github.com/user-attachments/assets/42a87337-3eb6-4805-b98e-98450a162fef)



