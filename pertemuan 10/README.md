- Buat infografik / cheatsheet dari perintah-perintah MySQL di atas (boleh yang mau pake PostgreSQL)
- 
#### MySql cheat sheet
![Tambah Data](https://github.com/NormalikaShandi/IF214002/blob/main/pertemuan%2010/img/3d811129fdc712cfa425b4d15d566360.jpg "Tambah Data")


#### Postgresql Cheat sheet
![Tambah Data](https://github.com/NormalikaShandi/IF214002/blob/main/pertemuan%2010/img/Postgres-Cheat-Sheet-back.png "Tambah Data")

- Buat query untuk mencari penduduk berusia diatas 25 tahun yang berada di kabupaten 3204 dari [data ini](https://github.com/insanalamin/IF214002/blob/main/pertemuan10/penduduk.sql)

 ``` sql
   SELECT YEAR(CURDATE())-YEAR(tanggal_lahir) AS usia FROM penduduk WHERE usia > 25 && kode_kabupaten = 3204 ;
 ```
