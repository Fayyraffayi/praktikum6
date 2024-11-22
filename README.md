# praktikum6

# Flowchart

![flowchart praktikum6](https://github.com/user-attachments/assets/51e030a5-a129-4979-bd6b-932708dbbb85)

# Codingan 1
```
kontak = {
"alpi": "085710092053",
"sultan": "087815646769"
}
print("Kontak alpi:", kontak["alpi"])

kontak["aldo"] = "082127150958"
kontak["sultan"] = "087815646769"

print("Semua Nama:")
for nama in kontak:
print(nama)

print("Semua Nomor:")
for nomor in kontak.values():
print(nomor)

print("Daftar Nama dan Nomornya:")
for nama, nomor in kontak.items():
print(nama + ": " + nomor)

del kontak["sultan"]

print("Semua Nama:")
for nama in kontak:
print(nama)

print("Semua Nomor:")
for nomor in kontak.values():
print(nomor)

print("Daftar Nama dan Nomornya:")
for nama, nomor in kontak.items():
 print(nama + ":"+ nomor)
```

# Hasil Codingan

