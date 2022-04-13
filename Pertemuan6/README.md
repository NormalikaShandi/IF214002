#### DIAGRAM ERD
![Tambah Data](https://github.com/NormalikaShandi/IF214002/blob/main/Pertemuan6/img%20draw.io/Screenshot%20(748).png "Tambah Data")

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
