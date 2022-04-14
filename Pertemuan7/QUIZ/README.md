### QUIZ 14 April 2022

#### Soal
- Berikan contoh pemanfaatan data historis
- Rancang ERD untuk penyimpanan data karyawan dari sebuah perusahaan, lengkap dengan data historis gaji, data historis tempat tinggal, dan data historis jabatan. Selanjutnya, implementasikan ERD tersebut pada basis data relasional (MySQL / PostgreSQL / SQL Server / dll) menggunakan perintah 

#### Jawab
- contoh pemanfaatan data historis
  - data pemasukan penjualan 
  - tingkat jumlah pasien dirumah sakit
  - data kesehatan, kemiskinan ,dan jumlah penduduk.
  - presentase pendaftar ke SMA negri 
  - presentase nilai siswa
  - kasus korupsi dari tahun ketahun
  - lagu terpopuler 

- Diagram ERD
![Tambah Data](https://github.com/NormalikaShandi/IF214002/blob/main/Pertemuan7/QUIZ/img/Screenshot%20(750).png "Tambah Data")


## SQL

```
CREATE TABLE karyawan (
  nik_karyawan INT(30),
  nama VARCHAR(100),
  tempat_lahir VARCHAR(50),
  tanggal_lahir DATE,
  jenis_kelamin VARCHAR(10),
  no_telepon INT(10),
  email VARCHAR(30),
  kode_jabatan INT(10)
  );
  
CREATE TABLE tempat_tinggal (
  id_tempat_tinggal INT(10),
  nik_karyawan int(30),
  tempat_tinggal_saat_ini VARCHAR(200)
  );
  
CREATE TABLE histori_tempat_tinggal (
  id_tempat_tinggal INT(10),
  nik_karyawan int(30),
  lokasi_histori_tempat_tinggal VARCHAR(200),
  tanggal_ubah_tempat_tinggal DATE
  );
  
CREATE TABLE gaji (
  kode_gaji INT(10),
  nik_karyawan int(30),
  tanggal_gaji DATE,
  gaji_pokok INT(10)
  );
  
CREATE TABLE histori_gaji (
  kode_gaji INT(10),
  nik_karyawan int(30),
  tanggal_histori_gaji DATE,
  histori_gaji INT(10)
  );
  
CREATE TABLE jabatan (
  kode_jabatan INT(10),
  nik_karyawan int(30),
  jabatan VARCHAR(30)
  );
  
CREATE TABLE histori_tempat_tinggal (
  kode_jabatan INT(10),
  nik_karyawan int(30),
  histori_jabatan VARCHAR(30),
  tanggal_histori_jabatan DATE
  ); 
```
