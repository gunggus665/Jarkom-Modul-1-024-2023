# Jarkom-Modul-1-024-2023

# No 1
Filter Expression :
```pwsh
ftp
```

Screenshot :

![Filtering](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/b961fcb5-402a-48f8-b770-08847b95b17e)
![sequence/ack_dari_aktivitas](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/64af622e-a9a1-4559-9fc4-4c4f6c98f062)
![sequence/ack_dari_response_aktivitas](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/b834f167-78c9-426f-b070-d6bfef28b425)
![1](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/3d094409-b9ac-4715-a146-e7f8ad35ea4e)

Flag :
```
Jarkom2023(y0u_r_g00d_4t_4dr3ssing_FzAnEqM20169326}
```

Cara Pengerjaan :

Menggunakan filter `ftp` untuk menyaring packetnya, dan mencari packet yang mengupload file. Ditemukan packet 147 yang dimana mengunggah atau merequest file .zip. dan ditemukan juga packet 149 yang berupa response dari request/upload packet 147. Setelah itu, mencari sequence number dan acknowledge number raw pada packet 147 dan 149 yang dapat ditemukan pada transmission control protocol.

Kendala :
Mengecek manual packetnya 1 1 sehingga sedikit memakan waktu.

# No 2
Filter Expression :
```pwsh
http
```
Screenshot :

![unnamed](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/d75be307-4484-4c2b-b688-b2377de16f20)
![unnamed (1)](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/4ddb4d1d-ee1f-4f4f-9f98-6a93c4380307)
![unnamed (2)](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/da2f2632-0ff7-40bf-a736-efd101a8815a)

Cara Pengerjaan :

Flag :
```
Jarkom2023{9unic0rn_1s_FBxhYb0A636c60a_c00l}
```

Cara Pengerjaan :

Disuruh untuk mencari webserver pada portal jarkom. Setelah googling, ternyata biasanya webserver terletak di HTTP. Setelah memberi filter HTTP, dapatlah packet yang berisikan konten dari web seperti header, html dan lain”. Tanpa berfikir dan mencari 1 1 saya Find saja server, dan ketemu `gunicorn`.

Kendala :

Tidak tahu biasanya letak webserver dimana, tetapi setelah sedikit searching langsung mengerti ternyata pada html atau saat request get ke http

# No 3 (REVISI)
Filter Expression :
```pwsh
ip.addr == 239.255.255.250 && udp.port == 3702
```

Screenshot :

![unnamed (3)](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/49485e97-4945-42c8-9410-4df33660df66)

Flag :
```
Jarkom2023{4nalyz3_is_0589_EiNlFgAzPmP_gr3at}
```

Cara pengerjaan :

Menggunakan ip.addr (untuk mencari spesifik ip address), AND (&&), udp.port (untuk mencari port tertentu). dan tertera pada wireshark di kolom Protocol kalau semua packet tersebut tipe UDP, dan tinggal menghitung berapa banyak packet yang ada setelah melakukan filter tersebut

Kendala : -

# No 4

Filter Expression : -

Screenshot :

![image](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100349628/d41433ac-8992-44cf-93e0-fab36843d1b1)

Flag :
Jarkom2023{ch3cksum_is_u5eful_0x1tq2}

Cara pengerjaan :
Cukup mencari packet no 13, diklik 2x untuk melihat detailnya, dan lihat dibagian checksum.

Kendala : -

# No 7
Filter Expression :
```pwsh
ip.dst_host == 184.87.193.88
```

Screenshot :

![unnamed (4)](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/b432f987-a40e-454c-ae67-c63109c64c43)

Flag :
```
Jarkom2023{UzyGd1600KJLuJD1L4_4n0th3r_f1lt3ring}
```

Cara pengerjaan :

Diminta untuk mencari packet yang menuju IP tertentu, maka menggunakan filter ip.dst_host == 184.87.193.88 setelah menemukan IP yang dituju maka langsung melakukan nc dan menjawab soal berdasarkan IP yang sudah di sortir.

Kendala :
-

# No 8
Filter Expression :
```pwsh
tcp.dstport == 80 || udp.dstport == 80
```

Screenshot :

![unnamed (5)](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100693456/1e57c7ad-fe8a-45f5-99ba-c87f08b08fd6)

Flag :
```
Jarkom2023{qu3ryyyyying_615694_SkRjQwDlSvE_15_fun}
```

Cara pengerjaan :

Disuruh untuk memberikan kueri filter sehingga wireshark hanya mengambil semua protokol packet yang menuju port 80. menggunakan filter or .dstport (MENUJU) pada tcp dan udp pada port 80. 

Kendala :
-

# No 9
Filter Expression :
ip.src == 10.51.40.1 && ip.dst != 10.39.55.34

Screenshot : 

![image](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100349628/92aac124-7e81-4a17-b680-d5ae388dc6d4)

Flag :
Jarkom2023{y3s_its_SlQjPgNjRiP_qu3ry1ng}

Cara pengerjaan  :
Menggunakan and (&&) dan not (!) untuk filter, juga menggunakan ip.dst.src untuk tahu ip yang menuju atau berasal

Kendala :
Pada saat memasukan filter Expression tidak keluar apa apa ternyata caranya tinggal di nc terus dimasukkan filter Expressionnya

# No 10
Filter Expression:
tcp.stream eq 2

Screenshot :

![image](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100349628/70965cef-25c0-4f4c-96c6-88a925bf9984)

Flag :
Jarkom2023{t3lnet_is_y6CABy2CByzA8668y_N0tSecu2e}

Cara pengerjaan :
Saat saya follow salah satu packet, akan muncul tcp.stream eq xx (xx disini adalah angka), pertama saya menemukan tcp.stream eq 11 yang dimana ini artinya aliran tcp ke-11. Lalu saya coba 1 1 alirannya, banyak packet yang memiliki username dan password seperti admin atau root. Akhirnya, saya mencari dan ketemu di aliran 2 yang dimana tidak seperti admin/root

Kendala :
Pada saat pengerjaan saya cukup lama untuk memfollow satu satu packetnya sampai akhirnya ketemu di eq 2 username dan passwordnya


