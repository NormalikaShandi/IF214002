## Tugas
Buat DDL, sampel DML, dan DQL 

---
## DDL
```sql
CREATE TABLE pembeli (
  id_pembeli INT(5) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_pembeli VARCHAR(20),
  alamat_pembeli VARCHAR(100),
  no_telepon_pembeli int(13)
);

CREATE TABLE karyawan (
  id_karyawan INT(5) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_karyawan VARCHAR(20),
  alamat_karyawan VARCHAR(100),
  no_telepon_karyawan int(13)
);

CREATE TABLE kurir (
  id_kurir INT(5) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_kurir VARCHAR(20),
  alamat_kurir VARCHAR(100),
  no_telepon_kurir int(13)
);

CREATE TABLE barang (
  id_barang INT(5) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  nama_barang VARCHAR(50),
  deskripsi_barang VARCHAR(200),
  stok_barang int(5),
  harga_barang INT(10)
);

CREATE TABLE transaksi (
  id_transaksi INT(5) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  id_pembeli INT(5),
  id_karyawan_yang_menyetujui INT(5),
  tanggal_transaksi DATETIME,
  status_pembayaran VARCHAR(10)
  );  
  
CREATE TABLE item_transaksi (
  id_item_transaksi INT(5) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  id_transaksi INT(5),
  id_barang INT(5),
  jumlah_barang INT(10),
  harga_setiap_barang INT(10)
  );  
  
CREATE TABLE pengiriman (
  id_pengiriman INT(5) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  id_kurir INT(10),
  id_transaksi INT(10),
  jumlah_barang INT(100),
  alamat_pembeli VARCHAR(100)
  );  
  
```

---
## DDL
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

INSERT INTO pengiriman (id_pengiriman, id_kurir, id_transaksi, jumlah_barang, alamat_pembeli) VALUES (11121,"12231","10011","2","Jalan Apel no. 10")
```

## DQL
- SELECT
```sql
SELECT * FROM transaksi WHERE id_pengguna=10231
```
