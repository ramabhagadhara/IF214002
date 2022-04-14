# contoh pemanfaatan data histori
- Hasil panen para petani per tahun atau per enam bulan 
- gaji karyawan 
- pemasukan keuangan negara 
- pengeluaran keuangan negara  
- kasus aktif covid 
- kasus kematian karena covid 
- trafik pengunjung mal per hari

# rancangan erd karyawan 
![erd karyawan drawio](https://user-images.githubusercontent.com/100655814/163296954-cdb9710d-ca1a-4175-86c4-bc392f561f68.png)

# rancangan table 
![tabel karyawan drawio](https://user-images.githubusercontent.com/100655814/163297037-edb052a7-035d-49f2-85c4-e1c1aec6fa05.png)

# sql 

```sql
CREATE TABLE karyawan(
  	id_Karywan int,
  	Nama VARCHAR(255),
  	Alamat VARCHAR(255)
  );
  
  CREATE TABLE tgl historis gaji(
    	tgl_mulai_gaji DATE,
    	id_Karyawan int,
    	Gaji INT
    );
  
  CREATE TABLE historis jabatan(
    	id_Jabatan int,
    	id_Karyawan int,
    	Jabatan VARCHAR(255)
    );
```
