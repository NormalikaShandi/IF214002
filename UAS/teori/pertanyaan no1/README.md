
# IDE: MEMBUAT TOKO ONLINE YANG MENJUAL KERAMIK

## Deskripsi

Di era teknologi seperti sekarang ini banyak toko-toko online yang menjual berbagai macam barang dan keperluan sehari hari. Dengan ini saya memunculkan ide membuat aplikasi untuk toko online yang menjual keramik. Aplikasi ini menyediakan berbagai model, motif dan warna keramik. Dan took ini menyediakan system pengiriman ekspedisi sendiri.

### Masalah Prioritas
- perkembangan penjualan perbulan
- penjualan keramik terbanyak/terlaris perbulan
- komplain pembeli

## Fitur

1.	Pembeli dapat memilih berbagai model, motif dan warna keramik
2.	Pembeli dapat melakukan proses transaksi pembelian dengan penjual.
3.	Penjual mengirim keramiik 

## Entitas dan Atribut

### Barang

-	\* id barang
-	Nama barang
-	jenis barang
-	Harga 
-	Stok barang

### Pembeli

-	\* id pembeli
-	Nama
-	Alamat
-	No telpon

### Karyawan

-	\* id karyawan
-	Nama
-	Alamat
-	No telpon

### Kurir

-	\* id kurir
-	Nama
-	Alamat
-	No telpon

### Transaksi

-	\* No Transaksi
-	\* id pelanggan
-	\* id karyawan
-	\* id barang 
-	Tanggal transaksi
-	status pembayaran

### Pengiriman 
-	\* id kurir 
-	\* id pelanggan
-	\* id barang
-	\* id transaksi
-	Alamat Pengiriman

### Item Transaksi
- no transaksi
- id barang
- nama barang 
- jumlah barang

### Barang yang akan dikirim
- no transaksi
- id pembeli
- id barang
- alamat pengiriman 
- tanggal pengiriman

### Pengiriman
- id pengiriman
- id kurir 
- no transaksi
- id pembeli 
- alamat pengiriman

### Barang yang diterima
- id pembeli
- id pengiriman
- no transaksi
- status pengiriman

## ER Diagram dan ERD

![Tambah Data](https://github.com/NormalikaShandi/IF214002/blob/main/UAS/teori/pertanyaan%20no1/er%20diagram.png "Tambah Data")
![Tambah Data](https://github.com/NormalikaShandi/IF214002/blob/main/UAS/teori/pertanyaan%20no1/ERD.png "Tambah Data")

---
## DDL
```sql
CREATE TABLE pembeli (
  id_pembeli INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_pembeli VARCHAR(20),
  alamat_pembeli VARCHAR(100),
  no_telepon_pembeli VARCHAR(13)
);

CREATE TABLE karyawan (
  id_karyawan INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_karyawan VARCHAR(20),
  alamat_karyawan VARCHAR(100),
  no_telepon_karyawan VARCHAR(13)
);

CREATE TABLE kurir (
  id_kurir INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_kurir VARCHAR(20),
  alamat_kurir VARCHAR(100),
  no_telepon_kurir VARCHAR(13)
);

CREATE TABLE barang (
  id_barang INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_barang VARCHAR(50),
  deskripsi_barang VARCHAR(200),
  stok_barang int,
  harga_barang INT
  );

CREATE TABLE transaksi (
  id_transaksi INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  id_pembeli INT,
  id_karyawan_yang_menyetujui INT,
  tanggal_transaksi DATETIME,
  status_pembayaran VARCHAR(10)
  );  
  
CREATE TABLE item_transaksi (
  id_item_transaksi INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  id_transaksi INT,
  id_barang INT,
  jumlah_barang INT,
  harga_setiap_barang INT
  );  
  
CREATE TABLE pengiriman (
  id_pengiriman INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  id_kurir INT,
  id_transaksi INT,
  jumlah_barang INT,
  alamat_pembeli VARCHAR(100),
  no_telepon_pembeli VARCHAR(13)
  );  
  
```

---
## DML
```sql
INSERT INTO pembeli (id_pembeli, nama_pembeli, alamat_pembeli, no_telepon_pembeli) VALUES (10231,"eka","Jalan Apel no. 10","081213141516");
INSERT INTO pembeli (id_pembeli, nama_pembeli, alamat_pembeli, no_telepon_pembeli) VALUES (10232,"edi","Jalan Apel no. 15","081214141516");

INSERT INTO karyawan (id_karyawan, nama_karyawan, alamat_karyawan, no_telepon_karyawan) VALUES (11231,"ali","Jalan bulan no. 20","089512342345");
INSERT INTO karyawan (id_karyawan, nama_karyawan, alamat_karyawan, no_telepon_karyawan) VALUES (11232,"ami","Jalan bintang no. 25","085112342345");

INSERT INTO kurir (id_kurir, nama_kurir, alamat_kurir, no_telepon_kurir) VALUES (12231,"ina","Jalan tomat no. 12","081209879876");
INSERT INTO kurir (id_kurir, nama_kurir, alamat_kurir, no_telepon_kurir) VALUES (12232,"ijah","Jalan labu no. 14","089434564567");

INSERT INTO barang (id_barang, nama_barang, deskripsi_barang, stok_barang, harga_barang) VALUES (10001,"keramik bunga biru","keramik standar ukuran 40x40, harga barang perdus. 1 dus = 10","200","50500");
INSERT INTO barang (id_barang, nama_barang, deskripsi_barang, stok_barang, harga_barang) VALUES (10002,"keramik polos putih","keramik tile ukuran 30x30, harga barang perdus. 1 dus = 10","450","85000");

INSERT INTO transaksi (id_transaksi, id_pembeli, id_karyawan_yang_menyetujui, tanggal_transaksi, status_pembayaran) VALUES (10011,"10231","11231","2022-05-01 07:10:00.000","berhasil")
INSERT INTO transaksi (id_transaksi, id_pembeli, id_karyawan_yang_menyetujui, tanggal_transaksi, status_pembayaran) VALUES (10012,"10232","11231","2022-05-02 09:30:30.000","berhasil")

INSERT INTO item_transaksi (id_item_transaksi, id_transaksi, id_barang, jumlah_barang, harga_setiap_barang) VALUES (11112,"10011","10001","2","50500, 85000")

INSERT INTO pengiriman (id_pengiriman, id_kurir, id_transaksi, jumlah_barang, alamat_pembeli,no_telepon_pembeli) VALUES (11121,"12231","10011","2","Jalan Apel no. 10","081213141516")
```
- update

```sql
UPDATE kurir set nama_kurir = 'ijal' WHERE id_kurir = 12232;
```
## DQL
- SELECT
```sql
SELECT * FROM transaksi WHERE id_pengguna=10231
```



