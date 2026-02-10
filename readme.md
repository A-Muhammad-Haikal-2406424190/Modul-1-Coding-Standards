## Reflection 1
dalam pengimplementasi fitur baru  menggunakan spring boot, 
saya berfokus pada peningkatan kualitas kode melalui penerapan prinsip Clean Code. 
Saya memastikan setiap fungsi bersifat modular dan juga menggunakan penamaan yang deskriptif agar lebih mudah dibaca. 
Lalu, Untuk menjaga standar proyek, fitur edit dan delete juga dikembangkan dengan prinsip DRY guna meminimalisir redundansi.
Dalam manajemen kode, saya menggunakan feature branch workflow untuk menjaga stabilitas branch utama. Meski demikian, 
saya juga mengidentikasi beberapa kerentanan yang ada pada kode saya, salah satu yang saya temukan adalah tidak adanya validasi input data yang masuk ketika create maupun edit product. 
Sebagai langkah mitigasi ke depan, saya berencana untuk membuat validasi input pada page create maunpun edit product .

## Reflection 2
Setelah menulis beberapa unit test pada proyek saya. Saya merasa bahwa unit test merupakan salah satu hal penting untuk dapat memanggkas waktu testing.
Maksud saya, hanya dengan beberapa baris kode saya sudah bisa melakukan testing yang kalau dilakukan secara manual akan memakan waktu yang lumayan banyak. 
Lalu terkait banyaknya unit test sebenarnya tidak ada standar pasti seberapa banyak kita harus menulis unit test.
Menurut saya, unit test bukan dinilai dari seberapa banyak test yang kita lakukan, namun adalah seberapa luas cakupan yang tercoverage dalam test tersebut.
Kemudian, 100% coverage bukan berarti bahwa kode ini telah bebas dari bug karena coverage sendiri hanya menilai dari seberaba banyak baris kode yang dieksekusi oleh test.
Hal ini menyebabkan dapat terjadinya bug, misalnya ketika kode tidak memliki validasi NULL, maka ketika lakukan testing dan coverage mencapai 100%, bukan berarti kode kita akan aman ketika terdapat input null.
Lalu untuk pembuatan functional test class baru, menurut saya hal ini melanggar konsep DRY karena kondisi ini menyebabkan kode menjadi redundan dan menurunkan kualitas kode.
Untuk mengatasi hal tersebut, kita dapat membuat file baru yang berisi base class dari test yang isinya dapat berupa variable/funsi dasar yang nantinya dapat digunakan untuk test lain.
