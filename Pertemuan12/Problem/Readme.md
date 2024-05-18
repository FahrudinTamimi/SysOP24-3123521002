[Bounded-Buffer Problem](#bounded-buffer-problem)

[Readers and Writers Problem](#readers-and-writers-problem)

[Dining Philosophers Problem](#dining-philosophers-problem)




## Bounded-Buffer Problem

![331269544-db2f56c7-7062-403a-92c1-f0a1c76e7882](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/45c488a1-641a-4455-8cf3-85da8a08c38d)

Masalah bounded buffer ini adalah proses antara produsen dengan konsumen. Kendala masalah ini yaitu penjadwalan (scheduling) dan mutual exclusion (mutex) 

Dimana konsumen harus menunggu jika ada buffer yang kosong ( konsumen harus menunggu hingga produsen menempatkan data ke dalam buffer) , sedangkan produsen harus menunggu jika buffer sedang penuh (produsen harus menunggu hingga konsumen mengambil data dari buffer sehingga ada ruang kosong untuk menempatkan data baru), dan hanya ada satu buffer yang dapat memanipulasi buffer tersebut .

Dalam masalah bounded buffer, ada sumber daya yang terbatas, yaitu buffer itu sendiri, yang digunakan untuk menyimpan data yang dihasilkan oleh produsen. Produsen harus menempatkan (write) produk-produknya ke dalam buffer yang tersedia.

Sedangkan konsumen akan mengambil (read) sumber daya yang penuh tersebut dan meninggalkannya pada sumber daya yang kosong. Kompleksitas utama dari masalah tersebut adalah menjaga perhitungan jumlah ketersediaan sumber daya yang kosong ataupun penuh

Untuk mengatasi masalah sinkronisasi antara keduanya, menggunakan semaphore. Semaphore membantu memastikan bahwa produsen menunggu saat buffer penuh dan konsumen menunggu saat buffer kosong. Ini memastikan bahwa buffer tidak berada dalam kondisi penuh atau kosong secara berlebihan dan mengatur akses produsen dan konsumen secara aman.

## Readers and Writers Problem

Readers and Writers Problem adalah masalah sinkronisasi dalam komputasi paralel dan terdistribusi yang melibatkan akses bersama ke sumber daya (seperti file atau database) oleh beberapa proses atau thread.

## Permasalahan

Mutual Exclusion: Hanya satu penulis yang boleh mengakses sumber daya pada suatu waktu untuk menghindari kondisi balapan (race conditions) yang dapat menyebabkan data korup.

## Solusi

Solusi untuk Readers and Writers Problem biasanya melibatkan penggunaan semaphores.

Prioritas Pembaca (Readers Priority):

Pembaca memiliki prioritas lebih tinggi daripada penulis. Jika ada pembaca yang ingin membaca, mereka tidak perlu menunggu penulis selesai menulis, tetapi penulis harus menunggu sampai semua pembaca selesai membaca.

Prioritas Penulis (Writers Priority):

Penulis memiliki prioritas lebih tinggi daripada pembaca. Jika ada penulis yang ingin menulis, pembaca yang ingin membaca harus menunggu sampai penulis selesai menulis.

## Dining Philosophers Problem

Dining Philosophers Problem adalah masalah pemrograman konkuren yang mengilustrasikan beberapa tantangan dalam mengelola sumber daya terbatas (seperti chopsticks atau garpu) di antara beberapa proses (filosof).

## Permasalahan

Deadlock: 

Terjadi jika setiap filosof memegang satu chopstick dan menunggu chopstick lainnya tanpa ada yang melepaskan chopstick yang sudah dipegang.

Starvation: 

Terjadi jika seorang filosof terus menerus tidak mendapatkan dua chopstick yang diperlukan untuk makan karena chopstick selalu diambil oleh filosof lain.

## Solusi

Solusi untuk masalah ini adalah menggunakan semaphores untuk mengatur pengambilan dan peletakan chopstick.


