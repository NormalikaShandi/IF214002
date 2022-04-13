# Pertemuan4
### catatan
- id_karyawan di Transaksi ditambahkan petunjuk tambahan terkait role karyawan di Transaksi tersebut, misal id_karyawan_yang_menyetujui
- antara Transaksi dengan Pengiriman ini M:M
- 1 Transaksi bisa lebih dari 1 barang
- 1 Transaksi bisa lebih dari 1 pengiriman, kalau keramiknya banyak


- Antara Transaksi - Barang ini M:M jadi harus dibuat entitas penghubung : ItemTransaksi >no transaksi >id barang >jumlah

- Antara Transaksi - Pengiriman ini M:M jadi harus dibuat entitas penghubung
- Antara Karyawan - Pembeli ga ada relationship, karena via Transaksi
- Antara Pembeli - Barang ga ada relationship
- Atribut buat transaksi dilengkapi
- Atribut barang ditambahi
