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
