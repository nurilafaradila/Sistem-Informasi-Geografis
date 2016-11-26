**SISTEM INFORMASI GEOGRAFI – PERTEMUAN 5**

**Membuat dan Mengedit Data Geospasial**

1. **Latar Belakang**

Pada pertemuan 5 GIS kali ini,  akan membahas

- --Cara membuat data geospasial menggunakan library pyshp.
- --Cara mengedit data geospasial menggunakan library pyshp.

1. **Pembahasan**

1. **Cara membuat data geospasial**

Dalam membuat data geospasial kita akan menggunakan library pyshp. Dibutuhkan file namafile.shp dan namafile.dbf

Cara membuatnya adalah :

- --Import shapefile
- --Instansiasi writer method

Sf = shapefile.Writer(param)

Dimana param disini adalah pilih shapetype :

1. shapeType = 1
2. shapeType = 3
3. shapeType = 5

- --Sama seperti read, kita lakukan metode dbf dan shp.

Penggunaan Shapefile (shp)

Untuk menambahkan record tergantung pada type ESRInya.

1. point (x,y)
2. line = (parts: [[x,y],[z,w], …])
3. poly = (parts: [[x,y],[z,w], …])

Penggunaan Databasefile (dbf)

Adapun tahapannya sebagai berikut :

- --membuat atribut terlebih dahulu kemudian menambahkan record.

Contoh :

sf.field (&#39;Nama filed&#39;,&#39;C&#39;,&#39;40&#39;)

Dimana C adalah Character dan 40 adalah length.

Dalam arti nama atribut, nama field dengan panjang 40 karakter.

- --Tambahkan recrd di bawah ini

sf.record(&#39;Bandung&#39;)

sf.record(&#39;Bandung&#39;,&#39;Sarijadi&#39;)

- --Setelah selesai maka simpan, dengan perintah :

sf.save(&#39;namafile.shp&#39;)

1. **Cara mengedit data geospasial**

Langkah-langkah editing data geospasial hamper sama dengan langkah membuat data geospasial, yang membedakannya adalah :

sf = shapefile.Writer(param)

diganti dengan

sf = shapefile.Editor(param)

Param adalah nama letak file.

Adapun operasi dalam editing pada shp dan dbf :

shp        : sf.poly()

         sf.line()

         sf.point()

dbf        : sf.record()

sf.delete(n); dimana        n adalah baris ke-n dari tabel

jika sudah selesai, simpan menggunakan perintah :

sf.save(&#39;namafile&#39;)

1. **Penutup**

1. **Kesimpulan**

Penambahan data geospasial bisa menggunakan attribute yang tersedia dalam parameter writer yang sudah ada.

1. **Saran**

Untuk memahami lebih rinci tentang cara membuat dan mengedit data geospasial, silahkan lakukan praktikum secara langsung menggunakan python.

Link Github        :

[https://github.com/nurilafaradila/Sistem-Informasi-Geografis](https://github.com/nurilafaradila/Sistem-Informasi-Geografis)

Nama        : Nurila Faradila Irfan

NPM        : 1144121

Kelas        : 3A

Prodi        : D4 TEKNIK INFORMATIKA

Kampus        : POLITEKNIK POS INDONESIA

Link Mata Kuliah        :

[http://kampus.awangga.net/assignments/sisteminformasigeografis2016](http://kampus.awangga.net/assignments/sisteminformasigeografis2016)

Referensi                :

[https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm](https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm)

Plagiarisme        :