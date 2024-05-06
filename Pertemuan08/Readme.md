[Perbedaan Paging dan Swapping](#perbedaan-paging-dan-swapping)

[PERBEDAAN RISC DAN CISC](#perbedaan-risc-dan-cisc)

[Hubungan Arsitektur CPU dengan Arsitektur OS](#hubungan-arsitektur-cpu-dengan-arsitektur-os)


## Perbedaan Paging dan Swapping

**Paging**

1. Paging adalah sebuah teknik yang digunakan oleh sistem operasi untuk membagi-bagi memori fisik menjadi blok-blok kecil yang disebut dengan "frame" dan memori logis menjadi blok-blok kecil yang disebut dengan "page".

2. Dalam sistem paging, proses-proses yang sedang berjalan dipecah menjadi bagian-bagian kecil yang disebut "page". Kemudian, setiap page ini ditempatkan ke dalam frame-frame di memori fisik.

3. Penggunaan paging memungkinkan sistem operasi untuk mengalokasikan memori secara fleksibel, memungkinkan program untuk menggunakan ruang memori yang lebih besar dari yang sebenarnya tersedia di dalam memori fisik. Hal ini juga memungkinkan sistem operasi untuk melakukan pertukaran antara bagian-bagian program yang sedang aktif dan yang sedang tidak aktif dalam memori.

**Swapping**

1. Swapping adalah proses di mana sistem operasi dapat memindahkan seluruh proses atau bagian-bagian dari proses dari memori utama (RAM) ke ruang penyimpanan sekunder (biasanya hard disk) dan sebaliknya.

2. Swapping terjadi ketika memori fisik tidak mencukupi untuk menampung semua proses yang sedang berjalan. Dalam hal ini, sistem operasi memindahkan beberapa proses dari memori utama ke penyimpanan sekunder untuk memberikan ruang yang cukup bagi proses-proses lain yang sedang berjalan.

3. Swapping dapat menyebabkan kinerja sistem menjadi lambat karena memindahkan data antara memori utama dan penyimpanan sekunder membutuhkan waktu yang cukup.

Jadi, perbedaan mendasar antara paging dan swapping adalah bahwa paging adalah teknik untuk mengorganisasi memori fisik dan logis menjadi unit-unit kecil yang disebut page dan frame, sementara swapping adalah proses untuk memindahkan data antara memori utama dan penyimpanan sekunder ketika memori utama tidak mencukupi untuk menampung semua proses yang sedang berjalan.

## PERBEDAAN RISC DAN CISC

**RISC** (Reduced Instruction Set Computing) adalah arsitektur komputer yang memiliki instruksi yang lebih sederhana dan terbatas.

RISC hanya melakukan satu operasi dalam satu instruksi.

**CISC** (Complex Instruction Set Computing) adalah arsitektur komputer yang memiliki instruksi yang kompleks dan beragam.

CISC dapat melakukan banyak operasi yang kompleks dalam satu instruksi.

## Hubungan Arsitektur CPU dengan Arsitektur OS

Arsitektur CPU dan arsitektur sistem operasi (OS) saling berhubungan dalam hal pengaturan dan pemanfaatan sumber daya komputer. CPU bertindak sebagai pusat pengolahan, menjalankan instruksi, dan mengatur jalannya program. Arsitektur CPU menentukan jenis instruksi yang bisa dieksekusi dan cara CPU berkomunikasi dengan perangkat keras lainnya.

Sedangkan, arsitektur OS bertanggung jawab atas pengelolaan seluruh sumber daya komputer, seperti memori, perangkat input/output, dan proses. OS berfungsi sebagai jembatan antara perangkat keras dan perangkat lunak, memberikan antarmuka bagi pengguna dan aplikasi, serta mengendalikan akses ke sumber daya.

Keduanya memiliki hubungan timbal balik. Arsitektur CPU mempengaruhi apa yang bisa dilakukan oleh OS, termasuk jenis instruksi yang didukung dan kemampuan seperti multithreading. Di sisi lain, OS menggunakan fitur-fitur CPU untuk mengelola sumber daya, seperti penjadwalan tugas, pengalokasian memori, dan penanganan interupsi.

Sebagai contoh, CPU yang memiliki banyak inti memungkinkan OS untuk menjalankan beberapa tugas secara bersamaan. Namun, OS juga harus sesuai dengan set instruksi CPU agar bisa menjalankan program dengan lancar. Keduanya bekerja sama untuk memastikan sistem komputer berjalan dengan optimal dan efisien.
