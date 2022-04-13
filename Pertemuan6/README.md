#### DIAGRAM ERD
![Tambah Data](https://github.com/NormalikaShandi/IF214002/blob/main/Pertemuan6/img%20draw.io/Screenshot%20(749).png "Tambah Data")

# Normalisasi
- Normalisasi bentuk ke 1
    - Harus memiliki primary key
    - Tidak boleh ada sel yang bernilai lebih dari satu
- Normalisasi bentuk ke 2
    - Harus tersertifikasi normalisasi bentuk 1
    - Tidak boleh ada kolom non-key yang bergantung pada sebagian dari composite key
- Normalisasi bentuk ke 3
    - Harus tersertifikasi normalisasi bentuk 2
    - Kolom non-key hanya boleh bergantung kepada primary key, tidak boleh ada ketergantungan tambahan ke kolom non-key lainnya

## Sebelum Normalisasi
#### Tabel Pembeli
|🔑id_pembeli|nama|alamat|no_telepon|
|---|---|---|---|
|1|Agus|Jalan Mawar no. 12|081234567890|
|2|Deno|Jalan Melati no. 34|085678901234|

#### Tabel Karyawan
|🔑id_karyawan|nama|alamat|no_telepon|
|---|---|---|---|
|1|Ani|Jalan Gajah no. 82|081209876543|
|2|Eko|Jalan Harimau no. 97|089876543211|

#### Tabel Kurir
|🔑id_kurir|nama|alamat|no_telepon|
|---|---|---|---|
|1|Ali|Jalan Anggur no. 22|081234567890|
|2|Tono|Jalan Apel no. 26|085678901234|

#### Tabel Barang
|🔑id_barang|nama|deskripsi|stok|harga|
|---|---|---|---|---|
|1|Keramik Mosaik 30x30 bunga biru|keramik ini bercorak bunga dengan warna biru dan dengan ukuran 30cm x 30cm. pembelian minimum 1 dus|50|90000|
|2|Keramik Standard 20x20 polos putih|keramik ini bercorak polos dengan warna putih dan dengan ukuran 20cm x 20cm. pembelian minimum 1 dus|450000|

#### Tabel Transaksi
|🔑id_transaksi|id_pembeli|id_karyawan_yang_menyetujui|tanggal_transaksi|status_pembayaran|
|---|---|---|---|---|
|1|3|5|12 Mei 2021|Berhasil|
|2|4|6|13 Mei 2021|Gagal|

#### Tabel Item_Transaksi
|🔑id_item_transaksi|id_transaksi|id_barang|jumlah_barang|harga_setiap_barang|
|---|---|---|---|---|
|4|7|35|1|50000|
|8|9|43|2|45000,120000|

##### dipisah
#### Tabel Item_Transaksi
|🔑id_item_transaksi|id_transaksi|id_barang|jumlah_barang|harga_setiap_barang|
|---|---|---|---|---|
|4|7|35|1|50000|
|8|9|43|1|45000|
|8|9|43|1|120000|
