## Data Definition Language (DDL)
#### Create Table
#### Petugas 

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
  ```
#### Lahan 

```sql 
CREATE TABLE lahan (
    id_Lahan INT (20) NOT NULL,
    id_Petugas INT (20) NOT NULL,
    Nama_Lahan VARCHAR (255),
    Luas_Lahan VARCHAR(255),
    Jenis_Tanah VARCHAR (255),
    PRIMARY KEY (id_Lahan)
    );
```

#### Penanaman

```sql 
 CREATE TABLE penanaman{
    id_Penanaman INT (20) NOT NULL,
    id_Lahan INT (20) NOT NULL,
    Nama_Benih VARCHAR (255) NOT NULL,
    Jumlah_Benih INT (20) NOT NULL,
    Harga_Benih INT (20) not NULL,
    Tanggal_Menanam DATE,
    PRIMARY KEY(id_Penanaman)
    );
```

#### Bahan

```sql 
 CREATE TABLE bahan(
      id_Bahan INT (20) NOT NULL,
      id_Penanaman INT (20) NOT NULL,
      Nama_Bahan VARCHAR (255) NOT NULL,
      Jumlah_Bahan INT (20) NOT NULL,
      Satuan VARCHAR (255) NOT NULL,
      Harga_Bahan INT (20) not NULL,
      PRIMARY KEY (id_Bahan)
      );
```

#### Panen

```sql 
   CREATE TABLE panen (
        id_Panen INT (20) NOT NULL,
        id_Penanaman INT (20) NOT NULL,
        Hasil_Panen INT (20) NOT NULL,
        Harga_Panen INT (20) Not NULL,
        Tanggal_Panen DATE,
        PRIMARY KEY (id_Panen)
        );
```

#### Evaluasi

```sql 
  
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

### Data Manipulation Language (DML)
#### Insert Data 
### Petugas 

```sql 
INSERT INTO petugas ( id_petugas, username, pass,nama_petugas, nohp_petugas, alamat) VALUES (1, 'rama' , '1234', 'Rama Bhagadhara', '083213923', 'cibiru');
```
