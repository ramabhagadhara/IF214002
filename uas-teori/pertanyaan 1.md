### Rancang solusi digital dari permasalahan yang teman-teman anggap penting untuk diselesaikan
Dalam Masalah ini saya akan merancan solusi digital terkait jumlah penduduk yang terus melunjak di kota besar yang dimana akan membuat kota itu overpopulation dan membuat kesenjagan sosial yang lebar

### Tentukan fitur-fitur utama dari solusi digital tersebut 
- penghitung jumlah penduduk di daerah yang over population

### Buat rancangan basis datanya dalam bentuk ER diagram
![uas drawio](https://user-images.githubusercontent.com/100655814/176567424-0ce5845e-1085-4177-8e03-884667227ff4.png)

### Buat model fisik dari basis datanya dalam bentuk query SQL yang meliputi: 1) data definition language untuk pembuatan tabel, 2) data manipulation language untuk contoh data awal, 3) data query language untuk analisis / business intelligence

  ```sql
 CREATE TABLE penduduk (
  id_penduduk INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  kode_daerah INT(15) NOT NULL,
  no_kk INT(15) NOT NULL,
  nik INT(15) NOT NULL
)

CREATE TABLE daerah (
  kode_daerah INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_daerah VARCHAR(40) NOT NULL
)

ALTER TABLE `penduduk` ADD FOREIGN KEY (`kode_daerah`) REFERENCES `daerah`(`kode_daerah`) ON DELETE RESTRICT ON UPDATE RESTRICT;
  ```
  
  
