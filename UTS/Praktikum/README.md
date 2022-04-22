#### 1. Data Control Language (DCL)
Sesuai namanya, perintah dasar DCL berfungsi untuk mengatur hak akses apa saja dari setiap pengguna, seperti database, tabel maupun field di dalamnya. Dengan adanya pengaturan ini, akses pengguna dapat dibatasi sehingga admin bisa menjaga keamanan database. Ada dua jenis perintah DCL, yaitu :

GRANT : di gunakan untuk memberikan akses ke user
REVOKE : kebalikan dari Grant, perintah ini di gunakan untuk menghapus hak akses user

#### 2. Data Definition Language (DDL)
DDL merupakan perintah dasar yang bertujuan untuk membuat serta mendefinisikan struktur database. Terdapat lima jenis perintah DDL, di antaranya :

CREATE : untuk membuat tabel, basis data, field dan beberapa objek basis data lainnya. Untuk menjalankan perintah ini, Kalian bisa menuliskan CREATE TABLE [‘nama_tabel’];
RENAME : untuk mengubah nama pada tabel dalam sistem database. Penulisan query ini dapat di tuliskan sebagai berikut: RENAME TABLE nama_tabel_lama TO nama_tabel_baru;
DROP : untuk menghapus data atau tabel pada suatu sistem database. Contoh penulisan query ini yaitu ​​DROP DATABASE nama_database;
ALTER : untuk menghapus atau menambahkan kolom atau data lainnya pada tabel. Salah satu contoh penulisan query ini ALTER TABLE nama_tabel ADD nama_kolom;
SHOW :  untuk menampilkan data dalam tabel. contoh penulisannya SHOW nama_database;

#### 3. Data Manipulation Language (DML)
Perintah dasar satu ini digunakan untuk mengolah data dan memanipulasi data dalam suatu tabel database. Perintah yang biasanya dilakukan adalah:

SELECT : untuk memperbaharui data dengan menambahkan suatu informasi baru dalam tabel atau database. Contoh penulisan query ini SELECT * FROM(nama tabel);
INSERT : untuk memperbaharui data dengan menambahkan suatu informasi baru dalam tabel atau database. Contoh penulisan query ini INSERT INTO nama_tabel (nama_field);
UPDATE : Digunakan ketika admin database ingin memperbaharui data lama menjadi data terbaru. Contoh penulisan query ini UPDATE nama_tabel;
DELETE : untuk menghapus data dalam tabel. Contoh penulisan query ini DELETE FROM … WHERE nama = ‘…’;
