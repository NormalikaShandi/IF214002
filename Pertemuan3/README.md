
# IDE: MEMBUAT TOKO ONLINE YANG MENJUAL KERAMIK

## Deskripsi

Di era teknologi seperti sekarang ini banyak toko-toko online yang menjual berbagai macam barang dan keperluan sehari hari. Dengan ini saya memunculkan ide membuat aplikasi untuk toko online yang menjual keramik. Aplikasi ini menyediakan berbagai model, motif dan warna keramik. Dan took ini menyediakan system pengiriman ekspedisi sendiri.

## Fitur

1.	Pembeli dapat memilih berbagai model, motif dan warna keramik
2.	Pembeli dapat melakukan proses transaksi pembelian dengan penjual.
3.	Penjual mengirim keramiik 

## Entitas dan Atribut

### Barang

-	\* id barang
-	Nama barang
-	Ukuran barang
-	Harga satuan
-	Jumlah barang
-	Stok barang

### Pembeli

-	\* id pembeli
-	Nama
-	Alamat
-	No telpon

### Karyawan

-	\* id karyawan
-	Nama
-	Jenis kelamin
-	Alamat
-	No telpon

### Kurir

-	\* id kurir
-	Nama
-	Jenis kelamin
-	Alamat
-	No telpon

### Transaksi

-	\* No Transaksi
-	\* id pelanggan
-	\* id karyawan
-	\* id barang 
-	Tanggal transaksi
-	Total harga

### Pengiriman 
-	\* id kurir 
-	\* id pelanggan
-	\* id barang
-	\* id transaksi
-	Alamat

## RELATIONSHIP
- Pembeli 1 1 - 1 N Barang
- Pembeli 1 1 - 1 N Transaksi
- Karyawan 1 1 - 1 1 Pembeli
- Barang 1 1 - 1 N Transaksi 
- Karyawan 1 1 - 1 N Transaksi  
- Kurir 1 1 - 1 N Transaksi
- 
