
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

## ERD

![Tambah Data](https://github.com/NormalikaShandi/IF214002/blob/main/UAS/teori/pertanyaan%20no1/ERD.png "Tambah Data")

