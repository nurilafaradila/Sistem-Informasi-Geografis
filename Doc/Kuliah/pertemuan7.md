**SISTEM INFORMASI GEOGRAFI – PERTEMUAN 7**

**Menjalankan MapServer &amp; MapProxy**

<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/GIS7a.jpg">
</p>

1. **Latar Belakang**

Teknologi pada zaman sekarang sudah semakin canggih, begitu juga dalam pemanfaatan geografis pada sistem digital seperti menyediakan map atau peta yang dibuat secara system, sesuai dengan keinginan. Salah satunya yaitu google maps. Adapun pada pembahasan kali ini akan menjelaskan bagaimana cara menjalankan map proxy dan map server.

Pada pertemuan 7 GIS kali ini,  akan membahas :

- --Cara menjalankan MapServer &amp; MapProxy

1. **Pembahasan**

<p align="center">
	<img src="https://github.com/nurilafaradila/Sistem-Informasi-Geografis/blob/master/img/GIS7b.png">
</p>

Cara menjalankannya adalah sebagai berikut :

1. Untuk meload data geospasial, kita perlu menyiapkannya dulu agar akan ditampilkan nantinya di Map Proxy. Data geospasial tersebut bisa didownload di situs ini, [http://www.halaman.download/](http://www.halaman.download/) kemudian pilih &quot;Producer&quot; dan klik &quot;Indonesia Mapproxy&quot;.
2. Ekstrak file tersebut (Penting!! Ketahui dimana anda mengekstrak file tersebut, karena path-nya akan digunakan untuk mengedit file yang ada di direktori tersebut. Di simpan di direktori Downloads (perhatikan penamaan menggunakan huruf kecil dan besar).
3. Pada file indomap -&gt; mapproxy -&gt; buka file agm.yaml
4. Pada file agm.yaml, edit beberapa baris sesuai dengan direktori tempat menyimpan file :

- --Pada baris binary:

/usr/libexec/mapserver

ubah menjadi binary:

/usr/lib/cgi-bin/mapserv

- --Pada baris map:

var/mapdata/mapfile/indo.map
ubah menjadi map:

/home/nurila/Downloads/indomap/mapfile/indo.map

- --Kemudian direktori baru dengan nama tmp pada direktori indomap
ubah baris working\_dir:

/var/mapdata/tmp
menjadi
/home/nurila/Downloads/indomap/tmp
Kemudian Save

1. Kemudian pada direktori mapproxy (di terminal/cmd), gunakan perintah :
vi mapproxy.ini

edit baris

chdir = /var/mymapproxy/

menjadi

chdir = /home/nurila/Downloads/indomap/mapproxy

Kemudian Save

1. edit file config.py pada direktori mapproxy

ubah
application = make\_wsgi\_app(r&#39;/var/mymapproxy/agm.yaml&#39;)

menjadi
application= make\_wsgi\_app(r&#39;/home/nurila/Downloads/indomap/mapproxy/agm.yaml&#39;)

1. Untuk menjalankan programnya gunakan perintah

uwsgi mapproxy.ini

1. Ketik localhost:8080 untuk mengecek mapproxy apakah sudah terinsall atau belum.
2. Klik demo atau ketik localhost:8080/demo
3. Pada bagian WMTS klik di bawah Image Format yaitu png
4. Tunggu beberapa saat karna datanya sedang di load.
5. Map Peta akan muncul

1. **Penutup**

1. **Kesimpulan**

Setelah dipraktekannya tutorial di atas, maka kita dapat mengetahui bagaimana cara menjalankan map server dan map proxy di dalam sistem operasi ubuntu.

1. **Saran**

Praktikum tentang hal ini harus bisa lebih dipahami dimengerti, tidak hanya dibuat saja, tetapi harus tahu fungsi dari setiap perintah yang dieksekusi.

Link Github        :

https://github.com/nurilafaradila/Sistem-Informasi-Geografis

Nama        : Nurila Faradila Irfan

NPM        : 1144121

Kelas        : 3A

Prodi        : D4 TEKNIK INFORMATIKA

Kampus        : POLITEKNIK POS INDONESIA

Link Mata Kuliah        :

http://kampus.awangga.net/assignments/sisteminformasigeografis2016

Referensi                :

https://en.wikipedia.org/wiki/MapServer

Plagiarisme        :

https://drive.google.com/open?id=0B34z3XSvW4dDQVhrWDJjSjJCXzQ

https://drive.google.com/open?id=0B34z3XSvW4dDZjdOV09vdEdIZ3M
