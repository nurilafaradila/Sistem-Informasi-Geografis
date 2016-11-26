**SISTEM INFORMASI GEOGRAFI – PERTEMUAN 4**

**Retrive Data Geospasial**

1. **Latar Belakang**
<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/0.jpg">
</p>

Manipulasi data geospasial dapat dilakukan dengan menggunakan fungsi CRUD (Create, Retrieve, Update, Delete). Pada pertemuan 4 ini, akan dibahas mengenai retrieve data geospasial.
- **--** Retrieve data geospasial.
- **--** Shapefile.
- **--** Cara operasi pengambilan data.
- **--** Membuat class geospasial editor.
- **--** Membuat method select, where Negara.

2. **Pembahasan**
**Retrieve data geospasial** adalah cara yang dilakukan untuk select/view data record file geometri dan dbf dengan file shp.

**Shapefile** terbagi menjadi dua, yaitu :
<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/1.JPG">
</p>

Data geometri adalah data kordinat yang membentuk bangun datar/ruang, diantaranya :
- **--** Point/titik        [1]
- **--** Line/garis        [3]
- **--** Poliygon        [5]

**Operasi pengambilan data** , menggunakan library pyshp class shapefile
<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/2.JPG">
</p>

Method shp :
- **--** Shapes ( )
- **--** Shape (n) , terdiri dari :
	- Bbox, boading box, merupakan batas view peta.
	- Parts, apakah record ini merupakan bagian dari record lainnya/pecahan record.
	- Points, merupakan kordinat pembentuk peta.
	- Shapetype, merupakan jenis geometri dari points.

Method dbf :
- **--** Fields ( )
- **--** Field (n)


**Praktikum :**

Menampilkan jumlah record dengan cmd
<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/3.JPG">
</p>


Membuat class geospasial editor
<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/4.JPG">
</p>

        Menggunakan tugas.py
<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/5.JPG">
</p>

Membuat method select, where countries
<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/6.JPG">
</p>

3. **Penutup**

Kesimpulan

Kesimpulan yang dapat diambil dari materi ini adalah cara membuat class dan method.

Saran

Pelajari lebih banyak tentang penggunaan bahasa python, agar dapat mempraktekannya dengan berhasil.

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

[www.cifor.org/publications/pdf\_files/Books/SIGeografis/SIG-part-2.pdf](http://www.cifor.org/publications/pdf_files/Books/SIGeografis/SIG-part-2.pdf)

Plagiarisme        :

[https://drive.google.com/open?id=0B34z3XSvW4dDdTFDRllScHIwUUE](https://drive.google.com/open?id=0B34z3XSvW4dDdTFDRllScHIwUUE)

[https://drive.google.com/open?id=0B34z3XSvW4dDX0lDc0w0LUpTZ3c](https://drive.google.com/open?id=0B34z3XSvW4dDX0lDc0w0LUpTZ3c)
