# praktikum6

# Flowchart

![flowchart praktikum6](https://github.com/user-attachments/assets/51e030a5-a129-4979-bd6b-932708dbbb85)

# Codingan 1
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

# Hasil Codingan

![Cuplikan layar 2024-11-23 135538](https://github.com/user-attachments/assets/3c3250c4-7250-46f0-9d52-37cb3812c82b)
