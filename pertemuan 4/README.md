![Screenshot (259)](https://user-images.githubusercontent.com/100655814/160035208-4cd2a6a9-4689-4c43-a349-ccfa0a27caf5.png)

# Ide : Sistem manajemen pengolahan hasil panen petani

## Deskripsi
Dalam Aplikasi ini diharapkan dapat membantu petani dalam mengurangi masalah masalah sampai masa panen tiba dan membantu memanajemen pertanian suatu daerah
aplikasi ini memiliki fitur 
- penghitung modal saat menanam benih 
- penghitung modal selama masa perawatan tanaman sebelum panen 
- penghitung untung atau rugi petani saat panen
- Monitoring Pertanian

diharapkan dalam aplikasi ini petani mengetahui berapa untuk atau rugi selama melakukan panen dan dapat memperbaiki pertanian kedepannya

## Entitas dan Atribut

### User
- \*ID
- Nama user
- Password
- Status

### Petugas
- \*ID
- Nama_Petugas
- Nohp_petugas
- alamat_petugas

### Penanaman
- \*ID
- Petugas
- Nama Lahan
- Nama Benih
- Jumlah Benih
- Harga Benih
- Jenis tanah
- Tanggal Menanam
- Perkiraan Panen

### Bahan & Alat
- \*ID
- Nama Bahan_alat
- Jumlah Bahan_alat
- Satuan
- Harga Bahan_alat

### Panen
- \*ID
- Nama benih
- Hasil panen 
- Harga jual
- Tanggal panen

## Relationship
- User 1 1 - 0 N Petugas
- Petugas 1 1 - N N Penanaman
- Petugas 1 1 - N N bahan & alat
- Petugas 1 1 - 1 1 Panen
