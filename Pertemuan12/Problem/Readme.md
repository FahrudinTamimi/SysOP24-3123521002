## Bounded-Buffer Problem

![331269544-db2f56c7-7062-403a-92c1-f0a1c76e7882](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/45c488a1-641a-4455-8cf3-85da8a08c38d)

Masalah bounded buffer ini adalah proses di antara produsen dengan konsumen. Kendala yang dari masalah ini yaitu penjadwalan (scheduling) dan mutual exclusion (mutex) seperti konsumen harus menunggu jika ada buffer yang kosong , produsen harus menunggu jika buffer sedang penuh, dan hanya satu buffer yang dapat memanipulasi buffer tersebut .Dengan kata lain, terdapat samber daya yang terbatas dan produsen mengisikan (write) harus produknya ke dalam sumber daya tersebut.
Sedangkan konsumen akan mengambil (read)) sumber daya yang penuh tersebut dan meninggalkannya pada sumber daya yang kosong. Kompleksitas utama dari masalah tersebut adalah menjaga perhitungan jumlah ketersediaan sumber daya yang kosong ataupun penuh
Untuk mengatasi masalah tersebut.dibutuhkan semaphore yang berfungsi sebagai penjaga agar produsen tidak mengakses sumber Untuk mengatasi masalah sinkronisasi pada bounded buffer problem yaitu Semaphore, Semaphore digunakan untuk mengatur akses produsen dan konsumen terhadap sumber daya. semaphore membantu menjaga ketersediaan sumber daya yang kosong atau penuh serta mengatur akses produsen dan konsumen secara aman.
