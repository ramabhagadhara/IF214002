### Rancang solusi digital dari permasalahan yang teman-teman anggap penting untuk diselesaikan
Sistem manajemen pengolahan hasil panen petani untuk membantu petani dalam memnatau perkembangan hasil tani

### Tentukan fitur-fitur utama dari solusi digital tersebut 
- penghitung jumlah benih yang banyak di tanam
- penghitung keuntungan setiap lahan
- penghitung hasil panen perlahan

### Buat rancangan basis datanya dalam bentuk ER diagram
![uass drawio](https://user-images.githubusercontent.com/100655814/176568900-8675a314-bc03-47cd-aa0d-43be6b0440a2.png)

### Buat model fisik dari basis datanya dalam bentuk query SQL yang meliputi: 1) data definition language untuk pembuatan tabel, 2) data manipulation language untuk contoh data awal, 3) data query language untuk analisis / business intelligence
- DDL

 ```sql
 CREATE TABLE penduduk (
  id_penduduk INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  kode_daerah INT(15) NOT NULL,
  no_kk INT(15) NOT NULL,
  nik INT(15) NOT NULL
)
 ```
  
  ```sql
CREATE TABLE daerah (
  kode_daerah INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_daerah VARCHAR(40) NOT NULL
)
 ```
  ```sql
ALTER TABLE `penduduk` ADD FOREIGN KEY (`kode_daerah`) REFERENCES `daerah`(`kode_daerah`) ON DELETE RESTRICT ON UPDATE RESTRICT;
  ```
- DML 

```sql
INSERT INTO `daerah` (`kode_daerah`, `nama_daerah`) VALUES ('2201', 'cibiru'), ('2202', 'ujung berung'), ('2203', 'cimahi');
```
```sql
INSERT INTO `penduduk` (`id_penduduk`, `kode_daerah`, `no_kk`, `nik`) VALUES (NULL, '2201', '123456789', '121212344'), (NULL, '2201', '123456789', '121212345'), (NULL, '2201', '123456789', '121212346'), (NULL, '2201', '123456789', '121212347'), (NULL, '2201', '123456789', '121212348'), (NULL, '2202', '123456788', '114536742'), (NULL, '2202', '123456788', '114536742'), (NULL, '2203', '123456778', '757675657');
  ```
