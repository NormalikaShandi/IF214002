## NORMALISASI

### Normalilasi Bentuk ke-1
Karena semua tabel sudah memiliki primary key, dan tidak ada sel yang memiliki nilai lebih dari 1, maka tabel sudah tersertifikasi normalisasi bentuk ke 1

---
### Normalisasi Bentuk ke-2
Karena tabel sudah tersertifikasi normalisasi bentuk ke-1, dan setiap tabel hanya memiliki 1 primary key saja (tidak ada yang menggunakan composite key), maka tabel sudah tersertifikasi normalisasi bentuk ke-2.

---
### Normalisasi Bentuk ke-3
Pada tabel surat, terdapat kolom non-key yang yang tidak bergantung pada primary key, kolom **id_item_setoran** tidak bergantung pada kolom apapun pada tabel surat. maka kolom id_item_setoran dihapus dari tabel surat.

