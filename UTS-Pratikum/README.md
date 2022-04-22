## UTS-Pratikum

1. Jelaskan contoh-contoh perintah SQL beserta kegunannya ! 

- Perintah SELECT

  perintah SELECT merupakan perintah dasar SQL yang di gunakan untuk memilih data dari database. Data yang di kembalikan di simpan dalam tabel yang di sebut result-set.
  
- Perintah SELECT DISTINCT

  Perintah SELECT DISTINCT merupakan perintah dasar SQL yang di gunakan untuk mengembalikan hanya nilai yang berbeda dari dalam sebuah tabel, dengan kata lain semua record duplikat (record dengan nilai yang sama) yang terdapat pada tabel akan di anggap sebagai satu record/nilai

- Perintah WHERE

  Perintah WHERE merupakan perintah dasar SQL yang di gunakan untuk mem-filter hasil SELECT dengan mengekstrak record yang memenuhi persyaratan tertentu.
 
- Perintah ORDER BY

  Perintah ORDER BY merupakan perintah dasar SQL yang di gunakan untuk mengurutkan result-set dalam pengurutan ‘ascending’ atau ‘descending’. Secara default perintah ORDER BY menampilkan record dalam pengurutan ‘ascending’ (‘ASC’). Untuk mengurutkan ‘descending’, gunakan kata kunci ‘DESC’

- Perintah INSERT INTO

  Dalam SQL, perintah INSERT INTO merupakan perintah dasar SQL bagian dari perintah untuk DML (Data Manipulation Language) Saya asumsikan Anda telah faham perbedaan DDL, DCL, dan DML. Perintah INSERT INTO dapat di gunakan untuk menambahkan record baru ke dalam tabel. 

- Perintah UPDATE

  Perintah UPDATE merupakan perintah dasar SQL yang di gunakan untuk memperbarui atau mengubah nilai suatu record berdasarkan kriteria tertentu.
 
 - Perintah DELETE

  Hampir sama dengan perintah UPDATE, perintah DELETE juga merupakan perintah dasar SQL yang di gunakan untuk menghapus nilai suatu record berdasarkan kriteria tertentu.
 
 - Perintah Create 
 
  perintah untuk membuat tabel baru di dalam sebuah database adalah create. Tak cuma untuk tabel baru, tapi juga database maupun kolom baru. Kamu bisa membuat sebuah query dengan contoh ‘CREATE DATABASE nama_database. 
 
 - Perintah Show
  
  perintah DDL ini digunakan untuk menampilkan sebuah tabel yang ada.
  
  
 2. Berdasarkan ERD yang telah dibuat, buatlah implementasi basis data dari ERD tersebut dalam bentuk tabel basis data lengkap dengan Primary Key, Foreign Key dengan menggunakan perintah CREATE TABLE bahasa SQL. Anda dapat menggunakan vendor basis data yang Anda sukai (MySQL / PostgreSQL / SQL Server / dsb.). Jika belum sempat install basis data di laptop, bisa menggunakan sqliteonline.com untuk mengecek keberhasilan pembuatan tabelnya. 
 
 ```sql

CREATE TABLE petugas(
  id_petugas int (20) NOT NULL,
  Username VARCHAR(255) NOT NULL,
  Pass VARCHAR (255) NOT NULL,
  Nama_Petugas VARCHAR(255) NOT NULL,
  NoHp_Petugas VARCHAR(255) NOT NULL,
  Alamat VARCHAR (255) NOT NULL,
  PRIMARY KEY (id_Petugas)
  );
  
  -- foreign key: id_Petugas
  CREATE TABLE lahan (
    id_Lahan INT (20) NOT NULL,
    id_Petugas INT (20) NOT NULL,
    Nama_Lahan VARCHAR (255),
    Luas_Lahan VARCHAR(255),
    Jenis_Tanah VARCHAR (255),
    PRIMARY KEY (id_Lahan)
    );
    
    -- foreign key: id_Lahan
    CREATE TABLE penanaman{
    id_Penanaman INT (20) NOT NULL,
    id_Lahan INT (20) NOT NULL,
    Nama_Benih VARCHAR (255) NOT NULL,
    Jumlah_Benih INT (20) NOT NULL,
    Harga_Benih INT (20) not NULL,
    Tanggal_Menanam DATE,
    PRIMARY KEY(id_Penanaman)
    );
    
    -- foreign key: id_Penanaman 
    CREATE TABLE bahan(
      id_Bahan INT (20) NOT NULL,
      id_Penanaman INT (20) NOT NULL,
      Nama_Bahan VARCHAR (255) NOT NULL,
      Jumlah_Bahan INT (20) NOT NULL,
      Satuan VARCHAR (255) NOT NULL,
      Harga_Bahan INT (20) not NULL,
      PRIMARY KEY (id_Bahan)
      );
      
      -- foreign key: id_Penanaman 
      CREATE TABLE panen (
        id_Panen INT (20) NOT NULL,
        id_Penanaman INT (20) NOT NULL,
        Hasil_Panen INT (20) NOT NULL,
        Harga_Panen INT (20) Not NULL,
        Tanggal_Panen DATE,
        PRIMARY KEY (id_Panen)
        );
        
        -- foreign key: id_Panen,id_Bahan
        
        CREATE TABLE evaluasi (
          id_Evaluasi INT (20) NOT NULL,
          id_Panen INT (20) NOT NULL,
          id_Bahan INT (20) NOT NULL,
          Keuntungan_Panen INT (20) NOT NULL,
          Modal_Panen INT (20) NOT NULL,
          Total_Keuntungan INT (20) NOT NULL,
          Status_Panen VARCHAR (255) NOT NULL,
          PRIMARY KEY (id_Evaluasi)
          );

```
