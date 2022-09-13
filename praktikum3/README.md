# Praktikum 3 - ARP
## A. Definisi
![arp](asset/3.arp.png "ARP")
ARP adalah protokol yang berjalan pada osi layer 2 atau data link layer. Protokol ini digunakan untuk memetakan Logical address (IP Address) ke Physical address (MAC Address). Protokol diterapkan untuk memudahkan pc satu dengan yang lain dalam mencari alamat atau posisi dari pc tujuannya.

## B. rARP
Untuk protokol ini merupakan kebalikan dari ARP. Protokol ini digunakan untuk memetakan Physical Address ke Logical Address.

## C. Cara kerja ARP
Cara kerja ARP memiliki konsep yang sama dari satu perangkat dengan perangkat yang lain. Untuk detailnya adalah sebagai berikut : 
1. Pada awal perangkat tersebut terhubung ke dalam sebuah jaringan, tabel arp yang dimiliki perangkat tersebut akan kosong. Jadi masing-masing perangkat masih belum mengenal satu sama lain. Dari mulai MAC Address, hingga IP Address. Ketika perangkat tersebut sudah mulai melakukan aktifitas, perangkat yang melakukan aktifitas tersebut akan mengirimkan pesan ARP pada seluruh perangkat jaringan dalam satu broadcast domain. Lalu apakah broadcast domain itu? Topik tersebut dapat kita bahas pada sesi selanjutnya.
2. Setelah pesan broadcast dikirimkan, perangkat yang memiliki alamat yang sesuai dengan pesan arp tersebut, akan mengirimkan balasan berupa pesan broadcast lagi yang memberitahukan source address perangkat tersebut, sekaligus menambahkan alamat dari pengirim pesan sebelumnya ke tabel arp nya sendiri.
3. Pesan balasan tersebut akhirnya diterima oleh pengirim asalnya dan tabel arp pun terisi dengan alamat dari perangkat yang membalas pesan tersebut.

## D. Real Case
Untuk membuktikan hal tersebut, mari kita lakukan percobaan berikut ini. Sebelumnya siapkan terlebih dahulu 
1. ping pc A ke pc B

2. ping lagi dari pc A ke pc B
3. ping pc A ke pc A