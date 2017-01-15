**SISTEM INFORMASI GEOGRAFI – PERTEMUAN 6**

**MapServer &amp; MapProxy**

1. **Latar Belakang**

Pada pertemuan 6 GIS kali ini,  akan membahas :

- --MapServer dan Fitur-Fitur
- --Cara Menginstall MapServer Pada CentOS
- --MapProxy dan Fitur-Fitur

- --Cara Menginstall MapProxy Pada CentOS

1. **Pembahasan**

1. **Map Server dan Fitur-Fitur**

MapServer adalah sebuah lingkungan pengembangan open source untuk membangun aplikasi internet spasial diaktifkan. Hal ini dapat dijalankan sebagai program CGI atau melalui Mapscript yang mendukung beberapa bahasa pemrograman (menggunakan SWIG). MapServer dikembangkan oleh University of Minnesota - jadi, sering dan lebih khusus disebut sebagai &quot;UMN MapServer&quot;, untuk membedakannya dari komersial &quot;peta server&quot;. MapServer awalnya dikembangkan dengan dukungan dari NASA, yang membutuhkan cara untuk membuat citra satelit yang tersedia untuk umum

Fitur-Fitur Map Server :

Mendukung format data standar industri dan database spasial

- --On-the-fly klasifikasi fitur
- --Canggih label berbasis aturan
- --On-the-fly proyeksi untuk kedua raster dan data vector
- --Menyediakan berbagai macam pertanyaan spasial dan atribut berbasis
- --Mendukung populer Terbuka Geospatial Consortium (OGC) standar termasuk WMS, WFS dan WCS
- --Memanfaatkan best-of-breed teknologi open source geospatial seperti GDAL / OGR, PostGIS dan PROJ.4
- --Terintegrasi dengan lingkungan front-end populer seperti ka-Peta, Chameleon, Mapbender, MapBuilder dan Cartoweb

1. **Install Map Server pada CentOS**

Langkah instalasi MapServer melalui repository elgis dengan menambahkan repository elgis terlebih dahulu, repository elgis juga membutuhkan repository epel.

# rpm -Uvh http://download.fedoraproject.org/pub/epel/6/x86\_64/epel-release-6-8.noarch.rpm

# rpm -Uvh http://elgis.argeo.org/repos/6/elgis-release-6-6\_0.noarch.rpm

Edit file epel.repo tambahkan exclude=armadillo :

# vi /etc/yum.repos.d/epel.repo

Instalasi wget :

# yum install wget

Instalasi armadillo :

# wget http://elgis.argeo.org/repos/6/elgis/x86\_64/gdal-1.9.2-4.el6.x86\_64.rpm

# wget http://proj.badc.rl.ac.uk/cedaservices/raw-attachment/ticket/670/armadillo-3.800.2-1.el6.x86\_64.rpm

# yum install armadillo-3.800.2-1.el6.x86\_64.rpm

kemudian lanjutkan proses instalasi :

# yum install gpsbabel

# yum install gdal

# yum install mapserver

# yum install glibc

# yum install libpng libpng-devel

# yum install gd gd-devel

# yum install giflib-devel

# yum install proj-epsg

# rpm -ql mapserver

# /usr/libexec/mapserver -v

1. **Map Proxy dan Fitur-Fitur**

MapProxy (mapproxy.org) adalah open source ubin geospasial proxy yang mendukung proyeksi ulang. Awalnya dikembangkan oleh Omniscale Mapproxy adalah server proxy python untuk gambar geospasial. Hal ini dapat membaca data dari WMS, ubin, mapserver dan mapnik, dan cache dan melayani data bahwa sebagai WMS, WMTS, TMS dan KML. Hal ini juga dapat melakukan reprojections antara berbagai sistem koordinat referensi.

Fitur – fitur Map Proxy :

- --MapProxy adalah server ubin (WMS-C, TMS, WMTS, KML SuperOverlays).
- --MapProxy juga WMS server yang sepenuhnya kompatibel dan mendukung WMS client (desktop dan web).
- --MapProxy dilengkapi dengan API keamanan yang fleksibel yang memungkinkan untuk menambahkan kontrol berbutir di layanan dan lapisan, bahkan dapat membatasi akses dari lapisan tunggal untuk luasan poligon.
- --Dapat menghasilkan cache ubin untuk kinerja yang lebih baik, ini disebut seeding.
- --Dapat menggunakan MapProxy untuk mengupgrade SDI tanpa menyentuh server yang ada.

1. **Install Map Proxy pada CentOS**

Langkah instalasi MapProxy :

# yum install python-pip python-devel

# pip install MapProxy

1. **Penutup**

1. **Kesimpulan**

MAP Server, adalah aplikasi untuk mngubah data vektor geospasial menjadi gambar ditampilkan sebagai web service. MAP PROXY ,berfungsi untuk menampung hasil gambar dari mapserver agar konsumsi komputasi bisa direduksi.

1. **Saran**

Selanjutnya untuk mendalami materi MapServer dan Map Proxy dengan membaca sumber-sumber yang tersedia di buku maupun internet , dan melakukan praktikum mandiri.

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

https://drive.google.com/open?id=0B34z3XSvW4dDUDFmRkgwLUF5NmM

https://drive.google.com/open?id=0B34z3XSvW4dDa0hjVkg1b24zcXM