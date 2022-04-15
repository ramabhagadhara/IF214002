# Pertemuan 6 Basis Data - UID dan Normalisasi 


  
   **Petugas**
  
  🔑 id
  |🔑 id_Petugas|Nama_Petugas|NoHp_Petugas|Alamat|
  |---|---|---|---|
  |1|Rama Bhagadhara|0813145801|Jl.Kebangsaan no 11|
  
  
   **Lahan**
  
  🔑 id
  |🔑 Id_Lahan|Id_Petugas|Nama_Lahan|Luas_Lahan|Jenis_Tanah|
  |---|---|---|---|---|
  |1|1|pak mamat|1000|Humus|
  
  
   **Penanaman**
  
  🔑 id
  |🔑 Id_Penanaman|Id_Lahan|Nama_Benih|Jumlah_Benih|Harga_Benih|Tanggal_Menanam|Perkiraan_Panen|
  |---|---|---|---|---|---|---|
  |1|1|Padi|100|1000|11-04-2022|11-05-2022|
  
   **Bahan**
  
  🔑 id
  |🔑 Id_Bahan|Nama_Bahan|Jumlah_Bahan|Satuan|Harga_Bahan|
  |---|---|---|---|---|
  |1|Pupuk|100|Kg|10000|
  
  **Panen**
  
  🔑 id
  |🔑 Id_Panen|Id_Penanaman|Hasil_Panen|Harga_Jual|Tanggal_Panen|
  |---|---|---|---|---|
  |1|1|100|1000\gram|12-05-2022|
  
  
  **Evaluasi**
  
  🔑 id
  |🔑 Id_Evaluasi|Id_Bahan|Id_Panen|Keuntungan_Panen|Modal_Panen|Total_Keuntungan|Status_Panen|
  |---|---|---|---|---|---|---|
  |1|1|1|1000000|300000|700000|Untung|
