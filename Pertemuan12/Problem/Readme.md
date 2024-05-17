## Bounded-Buffer Problem

![331269544-db2f56c7-7062-403a-92c1-f0a1c76e7882](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/45c488a1-641a-4455-8cf3-85da8a08c38d)

Masalah bounded buffer ini adalah proses antara produsen dengan konsumen. Kendala masalah ini yaitu penjadwalan (scheduling) dan mutual exclusion (mutex) 

Dimana konsumen harus menunggu jika ada buffer yang kosong ( konsumen harus menunggu hingga produsen menempatkan data ke dalam buffer) , sedangkan produsen harus menunggu jika buffer sedang penuh (produsen harus menunggu hingga konsumen mengambil data dari buffer sehingga ada ruang kosong untuk menempatkan data baru), dan hanya ada satu buffer yang dapat memanipulasi buffer tersebut .

Dalam masalah bounded buffer, ada sumber daya yang terbatas, yaitu buffer itu sendiri, yang digunakan untuk menyimpan data yang dihasilkan oleh produsen. Produsen harus menempatkan (write) produk-produknya ke dalam buffer yang tersedia.

Sedangkan konsumen akan mengambil (read) sumber daya yang penuh tersebut dan meninggalkannya pada sumber daya yang kosong. Kompleksitas utama dari masalah tersebut adalah menjaga perhitungan jumlah ketersediaan sumber daya yang kosong ataupun penuh

Untuk mengatasi masalah sinkronisasi antara keduanya, menggunakan semaphore. Semaphore membantu memastikan bahwa produsen menunggu saat buffer penuh dan konsumen menunggu saat buffer kosong. Ini memastikan bahwa buffer tidak berada dalam kondisi penuh atau kosong secara berlebihan dan mengatur akses produsen dan konsumen secara aman.
