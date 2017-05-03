# Chyrp Lite

[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Pembahasan](#pembahasan) | [Aplikasi Serupa](#aplikasi-serupa) | [Referensi](#referensi)
---:|:---:|:---:|:---:|:---:

## Sekilas Tentang

Chyrp Lite adalah sebuah mesin blogging yang ringan, dikembangkan dengan [PHP](http://php.net/manual/en/intro-whatis.php) dan [MySQL](https://en.wikipedia.org/wiki/MySQL_AB). Dengan Chyrp Lite, user dapat membuat sebuah blog baik itu blog, baik blog biasa maupun [tumblelog](http://whatis.techtarget.com/definition/tumblelog) (blog yang postnya dapat berupa audio, quote, link, gambar, atau video).

Terdapat fitur utama Feathers dan Pages. Feather digunakan untuk mengupload file-file multimedia seperti gambar, video, dan sebagainya sehingga blog yang dibuat menjadi seperti tumblelog. Pages digunakan untuk membuat sebuah post secara terpisah dari blog utama, misal untuk membuat sebuah kategori post yang terpisah. Bisa dikatakan, Chyrp Lite merupakan gabungan dari blog dan tumblelog.

## Instalasi
[`kembali ke atas`](#chyrp-lite)
### Kebutuhan
  - PHP 5.3.2+
  - MySQL:
    - MySQL 4.1+
    - MySQLi or PDO
  - SQLite:
    -SQLite 3+
    -PDO
### Cara Instalasi
Instalasi *Chyrp Lite* akan dilakukan di *virtual private server* ([VPS](https://en.wikipedia.org/wiki/Virtual_private_server)) berbasis Linux. Cara-cara dibawah ini dilakukan via terminal.
#### Instalasi Linux Apache MySQL PHP
```bash
#instal SSH
sudo apt update
sudo apt install ssh
```
Setelah terinstal SSH, VPS dapat diakses secara *remote*.
```bash
#akses remote dari host melalui port 2222
ssh adam@172.18.88.80 -p 2222

#instal Apache, MySQL, PHP
sudo apt install apache2
sudo apt install mysql-server
sudo apt install php
sudo apt install libapache2-mod-php
sudo apt install php-mysql
sudo apt install php-gd php-mcrypt php-mbstring php-xml php-ssh2
sudo service apache2 restart
```
#### Instalasi aplikasi Chyrp Lite
1. buat database dan user untuk Chyrp lite
```bash
mysql -u root -p -v -e "
  CREATE DATABASE chyrp;
  CREATE USER wordpress IDENTIFIED BY 'password';
  GRANT ALL PRIVILEGES ON chyrp.* TO chyrp;"
 ```
2. Download arsip tar.gz instalasi chyrp lite Saxaul ke direktori sekarang
```bash
wget "https://github.com/xenocrat/chyrp-lite/archive/v2015.06.zip"
```
3. Ekstrak file yang sudah terunduh ke direktori
```bash
sudo tar -xvzf v2015.06.zip && mv chyrp-lite-2015.06 chyrplite
```
4. Pindahkan direktori sekarang ke direktori chyrp
```bash
sudo chown -R www-data:www-data /var/www/html/chyrp
```
5. Lanjutkan konfigurasi chyrp lite melalui laman <http://172.18.88.80/chyrp> (alamat IP tempat menginstal chyrp lite)
Sebagai bahan acuan terdapat [dokumentasi Chyrp lite](https://github.com/xenocrat/chyrp-lite/wiki)

## Cara Pemakaian
[`kembali ke atas`](#chyrp-lite)

## Pembahasan
[`kembali ke atas`](#chyrp-lite)
### Kelebihan
Menurut persepektif developer, Chyrp Lite memiliki beberapa kelebihan sebagai berikut:

- Dibandingkan dengan aplikasi serupa, Chyrp Lite dapat dikatakan sebagai aplikasi dengan requirements paling minimal. Cukup dengan PHP 5.2+ serta MySQL 4.1+ atau SQLite 3+, Chyrp Lite bisa didapatkan. Proses instalasi Chyrp Lite juga tidak rumit, mengingat yang diperlukan hanyalah MySQL atau SQLite saja.

- Saat membahas seputar [template engine](https://en.wikipedia.org/wiki/Web_template_system) di PHP, banyak orang menduga bahwa PHP merupakan template engine. Akan tetapi, meskipun PHP telah memulai dirinya sebagai template language, sayangnya ia tak berevolusi sehingga masih belum mendukung modern template engine yang banyak dikembangkan kini. Menyadari hal tersebut, Chyrp menggunakan [Twig](http://twig.sensiolabs.org/) sebagai template enginenya yang secara umum memiliki kelebihan mudah dimengerti dan dipelajari. Namun kelebihan utama dari Twig yaitu sangat fleksibel untuk memenuhi kebutuhan pengguna karena memiliki open architecture, sehingga pengguna dapat membuat DSL tersendiri. 

- Apabila dibandingkan dengan Chyrp, seperti namanya Chyrp Lite lebih efisien dan lebih dapat diandalkan.

- Mengatur users dan visitors menggunakan model komprehensif yang benar.

### Kekurangan
- Meskipun mendeklarasikan diri sebagai hasil rekonstruksi agresif dari Chyrp, secara umum Chyrp Lite tidak memiliki kelebihan signifikan dibandingkan Chyrp.

- Text editor dari Chyrp Lite tidak terdapat WYSIWYG (yang memungkinkan user melihat hasil akhir interface dari sebuah post sembari user tersebut mengedit postnya)

### Aplikasi Serupa
[`kembali ke atas`](#chyrp-lite)
#### [Bludit](https://github.com/dignajar/bludit) 
Bludit merupakan sebuah aplikasi web sederhana yang digunakan untuk membuat blog maupun situs pribadi hanya dalam singkat. Bludit merupakan aplikasi gratis dan open source. Sama seperti Chyrp, Bludit merupakan platform blog berbasis PHP serta telah memiliki lisensi [MIT](https://en.wikipedia.org/wiki/MIT_License). 

Salah satu kelebihan dari Bludit yaitu penggunaan flat-files untuk penyimpanannya, sehingga tak perlu lagi melakukan install maupun konfigurasi database. Kelebihan lainnya yaitu adanya fitur Cli Mode (Command line Interface Mode) dimana pengguna dapat membuat, mengubah atau menghapus pages atau posts tanpa harus melalui tampilan web.

## Referensi
[`kembali ke atas`](#chyrp-lite)
1. [What can Chyrp Lite do for me?](https://chyrplite.net) - Chyrplite
2. [Why yet another template engine?](http://twig.sensiolabs.org/) - Twig
3. [Introduction | Bludit ](https://github.com/dignajar/bludit) - Bludit

