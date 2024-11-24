# praktikum6

# CODINGAN 1
```
kontak = {
  "rifai": "083183265423",
  "maysa": "087818766769"
}
print("Kontak rifai:", kontak["rifai"])

kontak["maul"] = "082127150958"
kontak["rido"] = "087815646769"

print("Semua Nama:")
for nama in kontak:
  print("- " + nama)

print("Semua Nomor:")
for nomor in kontak.values():
  print("- " + nomor)

print("Daftar Nama dan Nomornya:")
for nama, nomor in kontak.items():
  print( "- " + nama + ": " + nomor)

del kontak["maysa"]

print("Semua Nama setelah penghapusan :")
for nama in kontak:
  print( "- " + nama)

print("Semua Nomor setelah penghapusan :")
for nomor in kontak.values():
  print( "- " + nomor)

print("Daftar Nama dan Nomornya setelah penghapusan :")
for nama, nomor in kontak.items():
     print( "- " + nama + ":"+ nomor)
```

# HASIL CODINGAN

![Cuplikan layar 2024-11-23 135538](https://github.com/user-attachments/assets/3c3250c4-7250-46f0-9d52-37cb3812c82b)

# Penjelasan Codingan 1

1. Pertama, buat kamus kontak:

       kontak = {
       "rifai": "083183265423",
       "maysa": "087818766769"
       }
Ini membuat kamus dengan 2 pasang key-value, dimana nama sebagai key dan nomor telepon sebagai value.

2. Hubungi Rifai:

       print("Kontak rifai:", kontak["rifai"])
    Mengakses value dari key "rifai" untuk menampilkan nomornya.

3. Hubungi kami:

       kontak["maul"] = "082127150958"
       kontak["rido"] = "087815646769"
    Menambahkan 2 kontak baru ke dalam kamus.

4. Mencetak semua nama (kunci):

       print("Semua Nama:")
       for nama in kontak:
        print("- " + nama)
Melakukan loop untuk mencetak semua key (nama) dalam kamus.

5. Mencetak semua nomor (nilai):

       print("Semua Nomor:")
       for nomor in kontak.values():
        print("- " + nomor)
Menggunakan metode .values() untuk mencetak semua nilai (nomor) dalam kamus.

6. Mencetak nama dan nomor bersama:

       print("Daftar Nama dan Nomornya:")
       for nama, nomor in kontak.items():
       print("- " + nama + ": " + nomor)
Menggunakan metode .items() untuk mencetak pasangan key-value (nama dan nomor).

7. Menghapus kontak:
   
       del kontak["maysa"]
Menghapus kontak dengan kunci "maysa" dari kamus.

8. Terakhir, mencetak kembali semua data setelah penghapusan:

- Mencetak semua nama yang tersisa
- Mencetak semua nomor yang tersisa
- Mencetak semua pasangan nama dan nomor yang tersisa

Hasil running kode menunjukkan:
- Awalnya ada 4 kontak (rifai, maysa, maul, rido)
- Setelah penghapusan maysa, tersisa 3 kontak
- Data berhasil dimanipulasi (ditambah dan dihapus) dengan benar
- Semua kamus operasi (akses, tambah, hapus, loop) berfungsi dengan baik

# flowchart

![flowchart praktikum6](https://github.com/user-attachments/assets/51e030a5-a129-4979-bd6b-932708dbbb85)

# CODINGAN 2

```
# Dictionary untuk menyimpan data mahasiswa
data_mahasiswa = {}

# Fungsi untuk menambahkan data mahasiswa
def tambah_data():
    nim = input("Masukkan NIM: ")
    if nim in data_mahasiswa:
        print("Data dengan NIM ini sudah ada!")
        return
    nama = input("Masukkan Nama: ")
    tugas = float(input("Masukkan Nilai Tugas: "))
    uts = float(input("Masukkan Nilai UTS: "))
    uas = float(input("Masukkan Nilai UAS: "))
    akhir = (0.3 * tugas) + (0.35 * uts) + (0.35 * uas)
    data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": akhir}
    print("Data berhasil ditambahkan!")

# Fungsi untuk mengubah data mahasiswa
def ubah_data():
    nim = input("Masukkan NIM yang ingin diubah: ")
    if nim not in data_mahasiswa:
        print("Data tidak ditemukan!")
        return
    print("Data ditemukan: ", data_mahasiswa[nim])
    nama = input("Masukkan Nama baru: ")
    tugas = float(input("Masukkan Nilai Tugas baru: "))
    uts = float(input("Masukkan Nilai UTS baru: "))
    uas = float(input("Masukkan Nilai UAS baru: "))
    akhir = (0.3 * tugas) + (0.35 * uts) + (0.35 * uas)
    data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": akhir}
    print("Data berhasil diubah!")

# Fungsi untuk menghapus data mahasiswa
def hapus_data():
    nim = input("Masukkan NIM yang ingin dihapus: ")
    if nim in data_mahasiswa:
        del data_mahasiswa[nim]
        print("Data berhasil dihapus!")
    else:
        print("Data tidak ditemukan!")

# Fungsi untuk mencari data mahasiswa
def cari_data():
    nim = input("Masukkan NIM yang ingin dicari: ")
    if nim in data_mahasiswa:
        print("Data ditemukan: ", data_mahasiswa[nim])
    else:
        print("Data tidak ditemukan!")

# Fungsi untuk menampilkan semua data mahasiswa
def tampilkan_data():
    if not data_mahasiswa:
        print("TIDAK ADA DATA")
        return
    print("Daftar Nilai")
    print("=" * 63)
    print("| NO |    NIM    |      NAMA      | TUGAS | UTS | UAS | AKHIR |")
    print("=" * 63)
    for i, (nim, data) in enumerate(data_mahasiswa.items(), start=1):
        print(f"| {i:<2} | {nim:<9} | {data['nama']:<13} | {data['tugas']:<5} | {data['uts']:<3} | {data['uas']:<3} | {data['akhir']:<5.2f} |")
    print("=" * 63)

# Program utama
def main():
    while True:
        print("\n[L]ihat, [T]ambah, [U]bah, [H]apus, [C]ari, [K]eluar")
        pilihan = input("Pilihan: ").lower()
        if pilihan == "l":
            tampilkan_data()
        elif pilihan == "t":
            tambah_data()
        elif pilihan == "u":
            ubah_data()
        elif pilihan == "h":
            hapus_data()
        elif pilihan == "c":
            cari_data()
        elif pilihan == "k":
            print("Keluar dari program. Terima kasih!")
            break
        else:
            print("Pilihan tidak valid!")

if __name__ == "__main__":
    main()
```

# HASIL CODINGAN

![Cuplikan layar 2024-11-23 142528](https://github.com/user-attachments/assets/5709839d-6922-49d1-b948-01d83f8c84d4)

# PENJELASAN CODINGAN 2

Berikut adalah ringkasan ulang program manajemen data mahasiswa:  

1. Menu Utama:  
   Program dimulai dengan menampilkan pilihan berikut:  
   - Lihat data mahasiswa: Menampilkan daftar mahasiswa yang ada.  
   - Tambah data mahasiswa: Menambahkan informasi mahasiswa baru.  
   - Ubah data mahasiswa: Memperbarui informasi mahasiswa tertentu.  
   - Hapus data mahasiswa: Menghapus data mahasiswa berdasarkan NIM.  
   - Cari data mahasiswa: Mencari data mahasiswa dengan NIM tertentu.  
   - Keluar: Mengakhiri program.  

2. Lihat Data Mahasiswa:  
   Jika pengguna memilih opsi ini, program akan menampilkan daftar mahasiswa. Jika tidak ada data, program akan menampilkan pesan "TIDAK ADA DATA".  

3. Tambah Data Mahasiswa:  
   - Program meminta pengguna memasukkan NIM.  
   - Jika NIM sudah ada, program akan memberi pesan "DATA SUDAH ADA".  
   - Jika NIM belum ada, program meminta pengguna mengisi data tambahan seperti nama, nilai tugas, nilai UTS, dan nilai UAS.  
   - Program akan menghitung nilai akhir dan menyimpan data tersebut.  

4. Ubah Data Mahasiswa:  
   - Pengguna diminta memasukkan NIM mahasiswa yang ingin diperbarui.  
   - Jika NIM ditemukan, program meminta pengguna mengedit data seperti nama, nilai tugas, nilai UTS, dan nilai UAS.  
   - Program akan menghitung ulang nilai akhir dan menyimpan perubahan.  

5. Hapus Data Mahasiswa:  
   - Pengguna diminta memasukkan NIM mahasiswa yang ingin dihapus.  
   - Jika NIM ditemukan, data akan dihapus dari database.  

6. Cari Data Mahasiswa:  
   - Pengguna diminta memasukkan NIM mahasiswa yang ingin dicari.  
   - Jika NIM ditemukan, program akan menampilkan informasi mahasiswa.  
   - Jika tidak ditemukan, program akan memberi pesan "DATA TIDAK DITEMUKAN".  
