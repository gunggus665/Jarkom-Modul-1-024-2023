# Jarkom-Modul-1-024-2023

#No 4
Filter Expression :
-

Screenshot :
![image](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100349628/d41433ac-8992-44cf-93e0-fab36843d1b1)

Flag :
Jarkom2023{ch3cksum_is_u5eful_0x1tq2}

Penjelasan :
Cukup mencari packet no 13, diklik 2x untuk melihat detailnya, dan lihat dibagian checksum.

Kendala :
-

#No 9
Filter Expression :
ip.src == 10.51.40.1 && ip.dst != 10.39.55.34

Screenshot : 
![image](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100349628/92aac124-7e81-4a17-b680-d5ae388dc6d4)

Flag :
Jarkom2023{y3s_its_SlQjPgNjRiP_qu3ry1ng}

Penjelasan  :
Menggunakan and (&&) dan not (!) untuk filter, juga menggunakan ip.dst.src untuk tahu ip yang menuju atau berasal

Kendala :
Pada saat memasukan filter Expression tidak keluar apa apa ternyata caranya tinggal di nc terus dimasukkan filter Expressionnya

#No 10
Filter Expression:
tcp.stream eq 2

Screenshot :
![image](https://github.com/gunggus665/Jarkom-Modul-1-024-2023/assets/100349628/70965cef-25c0-4f4c-96c6-88a925bf9984)

Flag :
Jarkom2023{t3lnet_is_y6CABy2CByzA8668y_N0tSecu2e}

Penjelasan :
Saat saya follow salah satu packet, akan muncul tcp.stream eq xx (xx disini adalah angka), pertama saya menemukan tcp.stream eq 11 yang dimana ini artinya aliran tcp ke-11. Lalu saya coba 1 1 alirannya, banyak packet yang memiliki username dan password seperti admin atau root. Akhirnya, saya mencari dan ketemu di aliran 2 yang dimana tidak seperti admin/root

Kendala :
Pada saat pengerjaan saya cukup lama untuk memfollow satu satu packetnya sampai akhirnya ketemu di eq 2 username dan passwordnya


