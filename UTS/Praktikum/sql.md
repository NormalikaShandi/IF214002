```sql
CREATE TABLE pembeli (
  id_pembeli INT(10),
  nama_pembeli VARCHAR(20),
  alamat_pembeli VARCHAR(100),
  no_telepon_pembeli INT(13),
  PRIMARY KEY(id_pembeli)
  );
  
CREATE TABLE karyawan (
  id_karyawan INT(10),
  nama_karyawan VARCHAR(20),
  alamat_karyawan VARCHAR(100),
  no_telepon_karyawan INT(13),
  PRIMARY KEY(id_karyawan)
  );
  
CREATE TABLE kurir (
  id_kurir INT(10),
  nama_kurir VARCHAR(20),
  alamat_kurir VARCHAR(100),
  no_telepon_kurir INT(13)
  PRIMARY KEY(id_kurir)
  );
  
CREATE TABLE barang (
  id_barang INT(10),
  nama_barang VARCHAR(100),
  deskripsi_barang VARCHAR(200),
  stok_barang INT(10),
  harga_barang INT(10),
  PRIMARY KEY(id_barang)
  );
  
CREATE TABLE transaksi (
  id_transaksi INT(10),
  id_pembeli INT(10),
  id_karyawan_yang_menyetujui INT(10),
  tanggal_transaksi DATE,
  status_pembayaran VARCHAR(10)
  PRIMARY KEY(id_transaksi),
  FOREIGN KEY(id_pembeli),
  FOREIGN KEY(id_karyawan_yang_menyetujui)
  );  
  
CREATE TABLE item_transaksi (
  id_item_transaksi INT(10),
  id_transaksi INT(10),
  id_barang INT(10),
  jumlah_barang INT(100),
  harga_setiap_barang INT(10)
  PRIMARY KEY(id_item_transaksi),
  FOREIGN KEY(id_transaksi),
  FOREIGN KEY(id_barang)
  );  
  
CREATE TABLE pengiriman (
  id_pengiriman INT(10),
  id_kurir INT(10),
  id_transaksi INT(10),
  jumlah_barang INT(100),
  alamat_pembeli VARCHAR(100)
  PRIMARY KEY(id_pengiriman),
  FOREIGN KEY(id_kurir),
  FOREIGN KEY(id_transaksi)
  );  
```

