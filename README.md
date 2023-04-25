# **DPBO Latihan Praktikum 7**

##### **Nama : Muhammad Daffa Yusuf Fadhilah**

##### **NIM : 2100543**

Saya Muhammad Daffa Yusuf Fadhilah dengan NIM 2100543 mengerjakan evaluasi LP7
dalam mata kuliah Design Pemrograman Berorientasi Objek
untuk keberkahanNya maka saya tidak melakukan kecurangan seperti
yang telah dispesifikasikan. Aamiin.

## **Deskripsi Tugas**

- Pemain mengendalikan bola. Setiap kali bola bergerak, skor pemain bertambah +1.
- Skor hanya bertambah jika pemain berbelok, bukan bergerak berurutan. Detail:
  - Saat pertama kali membuka program, pemain bergerak ke arah manapun, skor +1.
  - Setelah pemain bergerak, dia harus bergerak ke arah lain agar skornya +1. Jika menekan tombol yang sama, skor tetap (+0).
  - Contoh, pemain membuka program, lalu bergerak ke kanan dan berhenti, maka skor bertambah +1. Jika pemain bergerak ke arah atas, bawah, atau kiri, maka skor bertambah +1. Namun, jika pemain bergerak ke kanan lagi, maka skor +0.
  - Bagaimana jika urutannya, kanan - atas - kiri - kanan? Kanan yang kedua tetap +1, karena pergerakan pemain sebelumnya adalah kiri, sehingga tidak dianggap berurutan.

## **Design Program**

Terdapat beberapa kelas yang java yang dibuat.

- **_GameInterface_** merupakan sebuah interface untuk seluruh objek yang akan dibuat pada game
- **_GameObject_** merupakan sebuah kelas parent bagi para objek yang dibuat seperti ukuran, lokasi, kecepatan objek, dan tipe dari objek
- **_Player_** merupakan class objek bertipe player yang merupakan turunan dari class **GameObject** yang akan menggambarkan player untuk game ini. Disini juga terdapat batasan-batasan perjerakan sebagai tambahan agar player tidak akan keluar dari batasan view pada game
- **_Display_** merupakan class yang berperan menjadi view pada game ini. Berisi mengenai ukuran dan properti windows lainnya seperti `resizeable`.
- **_Handler_** merupakan salah satu controller yang bertugas untuk menangani objek-objek yang ada pada game. Handler akan menyimpan semua objek dan menjalankan prosesnya masing-masing
- **_Controller_** merupakan controller yang berurusan dengan inputan keyboard yang akan memindahkan posisi player.
- **_Game_** merupakan controller utama yang memanggil berbagai class java diatas untuk dijalankan menjadi sebuah game. Proses logika utama pada game juga ada pada controller game ini.
- **_Sychronization_** merupakan driver yang berfungsi untuk menjalankan class **Game**

## **Modifikasi yang Dilakukan**

- Menambahkan attribut `RecentPressed` pada class Controller untuk menyimpan key apa yang sudah ditekan sebelumnya
- Disetiap `KeyEvent` akan dilakukan pengecekan apakah key yang ditekan sama seperti `RecentPressed`. Jika `KeyEvent` yang ditekan sama dengan `RecentPressed`, maka tidak akan ada penambahan score. dan begitu juga sebaliknya

## **Running**

- Start
  ![start](https://github.com/mdaffayusuff/LP7C2DPBO2022/blob/main/ss/1-Start.png?raw=true)

- Press A
  ![A](https://github.com/mdaffayusuff/LP7C2DPBO2022/blob/main/ss/2-Pressed%20A.png?raw=true)

- Press A again
  ![A again](https://github.com/mdaffayusuff/LP7C2DPBO2022/blob/main/ss/3-Pressed%20A%20again.png?raw=true)

- Press S
  ![S](https://github.com/mdaffayusuff/LP7C2DPBO2022/blob/main/ss/4-Pressed%20S.png?raw=true)

- Press D
  ![D](https://github.com/mdaffayusuff/LP7C2DPBO2022/blob/main/ss/5-Pressed%20D.png?raw=true)

- Press D again
  ![D again](https://github.com/mdaffayusuff/LP7C2DPBO2022/blob/main/ss/6-Pressed%20D%20again.png?raw=true)

- Press W
  ![W](https://github.com/mdaffayusuff/LP7C2DPBO2022/blob/main/ss/7-Pressed%20W.png?raw=true)

- Press S
  ![S](https://github.com/mdaffayusuff/LP7C2DPBO2022/blob/main/ss/8-Pressed%20S.png?raw=true)
