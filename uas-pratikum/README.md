### Link Demo youtube 

- link demo https://youtu.be/6Wzay4OYl3g

### Solusi Digital 

- Dalam aplikasi yang dibuat di harapkan dapat membantu petani atau dinas pertanian dalam memanajemen data pertanian yang diharapkan dapat diolah untuk membantu memajukan pertanian 

### DDL DML DQL basis data untuk keperluan CRUD dan Visualisasi data 

- DDL

```sql
CREATE TABLE petugas(
 id_petugas int (20) NOT NULL,
 Username VARCHAR(255) NOT NULL,
 Pass VARCHAR (255) NOT NULL,
 Nama_Petugas VARCHAR(255) NOT NULL,
 NoHp_Petugas VARCHAR(255) NOT NULL,
 PRIMARY KEY (id_Petugas)
 );
 CREATE TABLE lahan (
   id_Lahan INT (20) NOT NULL,
   id_Petugas INT (20) NOT NULL,
   Nama_Lahan VARCHAR (255),
   Luas_Lahan VARCHAR(255),
   Jenis_Tanah VARCHAR (255),
   PRIMARY KEY (id_Lahan)
   );
   
   CREATE TABLE penanaman{
   id_Penanaman INT (20) NOT NULL,
   id_Lahan INT (20) NOT NULL,
   Nama_Benih VARCHAR (255) NOT NULL,
   Jumlah_Benih INT (20) NOT NULL,
   Harga_Benih INT (20) not NULL,
   Tanggal_Menanam DATE,
   PRIMARY KEY(id_Penanaman)
   );
   
   CREATE TABLE bahan(
     id_Bahan INT (20) NOT NULL,
     id_Penanaman INT (20) NOT NULL,
     Nama_Bahan VARCHAR (255) NOT NULL,
     Jumlah_Bahan INT (20) NOT NULL,
     Satuan VARCHAR (255) NOT NULL,
     Harga_Bahan INT (20) not NULL,
     PRIMARY KEY (id_Bahan)
     );
     
     CREATE TABLE panen (
       id_Panen INT (20) NOT NULL,
       id_Penanaman INT (20) NOT NULL,
       id_lahan INT (20) NOT NULL,
       Hasil_Panen INT (20) NOT NULL,
       Harga_Panen INT (20) Not NULL,
       Tanggal_Panen DATE,
       PRIMARY KEY (id_Panen)
       );
       
   ```
  ```sql
ALTER TABLE `penduduk` ADD FOREIGN KEY (`id_lahan`) REFERENCES `lahan`(`id_lahan`) ON DELETE RESTRICT ON UPDATE RESTRICT;
  ```
- DML 

```sql
INSERT INTO `petugas` (`id_petugas`, `username`,'pass','nama_petugas','noHp_petugas') VALUES ('', 'petugas1','1234','ronaldo','08876433315'), ('', 'petugas2','12346','messi','08876433316'), ('', 'petugas3','12345','ronaldo','08876433313')
```
- DQL

```sql
SELECT nama_benih, COUNT(*) AS jumlah FROM `penanaman` GROUP BY nama_benih 
  ```
  ```sql
SELECT id_lahan,SUM(hasil_panen) AS total_jumlah FROM panen GROUP BY id_lahan
  ```
  ```sql
SELECT id_lahan,hasil_panen,harga_jual,tanggal_panen,harga_jual*hasil_panen AS total FROM panen WHERE id_lahan = '$id_lahan' GROUP BY total
  ```
