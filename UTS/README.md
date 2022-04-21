1. Basis data relasional dapat langsung dibangun menggunakan perintah SQL di sistem basis data seperti MySQL, dsb tanpa ada perancangan terlebih dahulu.  
   Jelaskan apa keuntungan melakukan perancangan basis data terlebih dahulu (menggunakan ERD ataupun Class Diagram) !
  
   jawab 
   - kecepatan dan kemudahan 
     
     Manfaat pertama dari basis data adalah dalam hal kecepatan dan kemudahan. Artinya dirancangnya basis data bertujuan untuk mempercepat proses pengolahan informasi. Karena adanya konsep primary key, indexing, searching, sorting, dan masih banyak lagi. Disamping itu, basis data yang baik menuntut penggunaannya harus mudah digunakan.
     
    - kebersamaan pemakai 
    
      Database yang baik dituntut untuk dapat dipakai bersamaan (shared-database). Contohnya adalah database MySQL, yang menyediakan akses database dalam waktu yang bersamaan. Pengelolaan data industri dimudahkan dengan adanya shared-database, karena aplikasi Enterprise berbasis web bisa diakses oleh seluruh staff yang berkepentingan, yang mana hal tersebut membutuhkan akses database dalam waktu bersamaan. Untuk itulah sistem shared-database biasanya menyediakan fitur User dan Access Privelege yang menentukan dan mengatur batasan data dan fitur data apa saja yang bisa diakses oleh user tertentu.
   
   - Kemudahan dalam penyajian laporan 
   
     Basis data memberikan kemudahan dalam menyajikan informasi hasil pengelolaan data yang disimpan didalam basis data. Dengan adanya bantuan fitur view dan Query, data ini bisa disajikan dengan berbagai bentuk dan jenis, mulai dari tabel Tabular, laporan grafik, statistik, dan Lain-lain.
 
2.Jelaskan bagaimana cara mentransformasikan proses bisnis sebuah organisasi menjadi struktur data di basis data !

  - pertama analisa dulu masalah yang ingin dikerjakan atau di bantu dengan solusi digital 
  - jika sudah ketemu masalahnya,tentukan fitur yang diiginkan untuk membantu dalam menyelesaikan masalah itu 
  - selanjutnya tentukan model data nya menggunakan diagram chen,tentukan atributnya,entitasnya dan relation antara objeknya 
  - selanjutnya buat ERD notasi Crow Foot dari struktur data logical yang mewakili fitur - fitut di solusi digital tersebut
  - jika sudah di buat normalisasi sampai bentuk ke tiga hingga mudah dipahami dalam proses bisnisnya 


3. Rancang solusi digital dari satu permasalahan yang ada di sekitar Anda.  

  a. Deskripsikam solusi digital tersebut dalam satu paragraf 
  
  Dalam kasus ini saya mengambil masalah pertanian,saya ingin memeberikan solusi dalam manajemen pertanian,mulai dari membantu pencatatan data dara penanaman,pencatatan data dalam panen,hingga evaluasia selama pertanian berlangsung diharapkan dari aplikasi ini dapat membantu para petani,dan menemukan solusi jika panen gagal atau rugi dan meningkatkan saat panen untung,hal ini dapat dilakukan karena adanya manajemn pertqanian ini dan nantiakan di analisa oleh ahli pertanian 
  
  b. Buat list fitur-fitur yang ada pada solusi digital tersebut 
   
   - input lahan oleh petugas 
   - menghitung modal saat menanam 
   - menghitung keuntungan panen 
   - menghitung modal bahan
   - evaluasi selama masa bertani sampai panen 
   - grafik hasil panen per 6 bulan 
   
   c.Buat ERD notasi Chen dari struktur data yang mewakili fitur2 di solusi digital tersebut
   
   ![diagram chen drawio](https://user-images.githubusercontent.com/100655814/164355030-907f1edf-92b1-4db2-955e-d361981b71da.png)

    
  d. Buat notasi ERD Crow Foot dari struktur data logical yang mewakili fitur fitur di solusi digital tersebut,lengkap dengan keys,tipe data dan normalisai hingga bentuk ketiga 
  
  ![erd notasi crow foot](https://user-images.githubusercontent.com/100655814/164372356-8206af4f-7ae8-44d8-9744-482dfea71bd0.png)
  
  flowchart 
  
  ![flowchart drawio](https://user-images.githubusercontent.com/100655814/164372419-628ff96d-3390-46b3-acf6-dc1965423b65.png)
