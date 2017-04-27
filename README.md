# Hastebin

[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Pembahasan](#pembahasan) | [Aplikasi Serupa](#aplikasi-serupa) | [Referensi](#referensi)
---:|:---:|:---:|:---:|:---:

## Sekilas Tentang


## Instalasi
[`kembali ke atas`](#chyrp-lite)
### Kebutuhan

### Cara Instalasi

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

```
#### Instalasi aplikasi Chyrp Lite

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


### Kekurangan

### Aplikasi Serupa
[`kembali ke atas`](#chyrp-lite)
#### [Bludit](https://github.com/dignajar/bludit) 

## Referensi
[`kembali ke atas`](#chyrp-lite)
