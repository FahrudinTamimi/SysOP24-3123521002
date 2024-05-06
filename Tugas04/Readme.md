1. Buatlah presentasi langkah demi langkah tentang siklus CPU (fetch,decode,execute) utk mengeksekusi sebuah program. Jelaskan juga peran dari Bahasa pemrograman dan compiler, begitu juga dengan peran dari Sistem Operaso. Gunakan referensi : [Video referensi 1](https://www.youtube.com/watch?v=Z5JC9Ve1sfI) dan [Video referensi 2](https://www.youtube.com/watch?v=jFDMZpkUWCw)

![cpu](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/bd034173-e322-478e-8266-81ea24ff3d7c)

**Fetch** 

CPU mengambil intruksi pada Addres 0 di memori kemudian LOAD 6 masuk ke intruction register

**Decode** 

CPU menerjemahkan intruksi LOAD 6 kemudian memuat addres 6 yang mempunyai value 1

**Ecexute**

CPU mengeksekusi addres 6 yang mempunyai value 1 kemudian dimasukkan ke dalam Accumulator

![cpu1](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/379d9489-45ba-4e96-8f33-1378255dc2fd)

**Fetch** 

CPU mengambil intruksi pada Addres 1 di memori kemudian ADD 7 masuk ke intruction register

**Decode** 

CPU menerjemahkan intruksi ADD 7 kemudian memuat addres 7 yang mempunyai value 1

**Ecexute**

CPU mengeksekusi addres 7 yang mempunyai value 1 kemudian dimasukkan ke dalam Accumulator, sebelumnya Accumulator sudah terdapat Value 1 jadi 1+1 = 2 kemudian Value 2 ini dimasukkan ke dalam Accumulator

![cpu drawio](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/0909ba44-c76f-4899-aba4-b9e13401fedc)

**Fetch** 

CPU mengambil intruksi pada Addres 2 di memori kemudian STORE 6 masuk ke intruction register

**Decode** 

CPU menerjemahkan intruksi STORE 6 kemudian menyimpan nilai yang ada di Accumulator ke dalam RAM, dialamat 6.

**Ecexute**

CPU mengeksekusi STORE dan menyimpan nilai Accumulator 2 ke dalam Address di dalam RAM.

![cpu3](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/7946a711-bdb3-468a-bbc1-5d2cd543c8d1)

**Fetch** 

CPU mengambil intruksi pada Addres 3 di memori kemudian JUMP 1 masuk ke intruction register

**Decode** 

CPU menerjemahkan intruksi JUMP 1 kemudian melompat kembali ke Address 1.

**Ecexute**

CPU menjalankan JUMP sehingga Programme Counter kembali menjadi 1.

Program akan kembali diulang dengan siklus yang sama.

![cpu4](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/f66f1b4b-a54c-4ee5-8905-6557fb9e34a2)


Pada setiap detak jam, cpu akan melakukan salah satu dari 3 hal : 

a. Fetch (mengambil instruksi dari alamat memori)

Pada tahap ini, prosesor mengambil instruksi dari memori utama (RAM) ke dalam registernya sendiri, biasanya disebut sebagai Instruction Register (IR) atau Program Counter (PC).
Instruksi ini diambil berdasarkan alamat memori yang disimpan dalam PC atau IR.
Setelah instruksi diambil, nilai Program Counter akan diperbarui untuk menunjuk ke instruksi berikutnya dalam aliran program.

b. Decode (memecahkan instruksi dan itu akan menjalankan instruksi) 

Setelah instruksi diambil, tahap berikutnya adalah dekripsi atau dekode instruksi yang diambil.
Dekode instruksi mengartikan instruksi tersebut dan menentukan operasi apa yang harus dilakukan oleh prosesor, serta operand mana yang harus digunakan untuk operasi tersebut.
Proses dekode ini dapat melibatkan pembacaan kode operasi (opcode) dan pengambilan nilai-nilai operand dari lokasi yang sesuai dalam instruksi.

c. Execute (Eksekusi)

Setelah instruksi diambil dan didekode, prosesor menjalankan operasi yang diinstruksikan oleh instruksi tersebut.
Tahap eksekusi melibatkan pengolahan data sesuai dengan operasi yang diinstruksikan, seperti penjumlahan, pengurangan, perkalian, pembagian, atau operasi logika lainnya.
Hasil dari operasi dieksekusi dapat disimpan kembali ke lokasi memori tertentu, atau digunakan sebagai input untuk instruksi selanjutnya dalam program.

**Istilah penting yang terkait dengan siklus fetch-execute** 

CPU: Unit pemrosesan pusat, bertanggung jawab untuk mengeksekusi instruksi dan melakukan pemrosesan data.

Memori Utama: Tempat penyimpanan data dan instruksi program.

Program Counter (PC): Register yang menyimpan alamat instruksi berikutnya yang akan dieksekusi.

Instruction Register (IR): Register yang menyimpan instruksi yang sedang diproses.

Control Unit (CU): Mengontrol dan mengarahkan operasi CPU.

Arithmetic Logic Unit (ALU): Melakukan operasi aritmatika dan logika pada data.

Opcode: Kode yang menentukan operasi yang harus dilakukan oleh CPU.

Operand: Data yang digunakan sebagai input untuk operasi CPU.

3. Baca dan pahami rangkuman materi OS: [Materi Intro to OS-01](https://github.com/ferryastika/OS-01)

4. Jalankan VM Debian anda, lalu lakukan clone https://github.com/ferryastika/flops-iops. Compile dan eksekusi sesuai petunjuk. Sesuiakan jumlah thread dengan jumlah CPU yang ada di VM Debianmu. Catat hasilnya dan jelaskan arti dari hasil ekskusi. Lakukan sebanyak 5 kali. Bandingkan hasilnya anatar temanmu. Buat Plot perbandinnga hasil untuk masing-masing PC di tiap kelompokmu. Analisa hasil percobaan tadi dan beri kesimpulan tentang IOPS dan FLOPS.

![make](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/32cbb5a8-ec2b-4601-89bf-d9142aa9daaa)

$ make digunakan untuk memicu proses pembangunan proyek.

$ make clean digunakan untuk membersihkan file-file sementara dan objek yang dihasilkan selama proses kompilasi

$ sudo make install digunakan setelah berhasil membangun proyek untuk menginstalnya di sistem Anda

$ sudo make uninstall digunakan untuk menghapus instalasi proyek yang sebelumnya diinstal menggunakan make install.

![iops](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/972ff3d4-7c4b-489c-aa41-e0515f68fc49)

  $ iops32 $(nproc)
  
  $ iops64 $(nproc)
  
  $ flops32 $(nproc)
  
  $ flops64 $(nproc)
  
**IOPS (Input/Output Operations Per Second)**

IOPS mengukur seberapa cepat suatu sistem dapat melakukan operasi masukan/keluaran (input/output) pada perangkat penyimpanan seperti hard disk drive (HDD) atau solid-state drive (SSD).

**FLOPS (Floating Point Operations Per Second)**

FLOPS mengukur seberapa cepat suatu sistem dapat melakukan operasi floating point (misalnya, penjumlahan, pengurangan, perkalian, pembagian) dalam perhitungan numerik.

6. Apabila Debian VM mu masih belum terdapat packeage gcc, make dan git, lakukan instalasi dan catat setiap langkahnya!
$ su -l

$ apt install make

$ apt install git

$ apt install gcc

$ git clone https://github.com/ferryastika/flops-iops

$ cd flops-iops

![su](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/31457830-1475-4af0-9861-e2cb064b3b3d)

$ su -l digunakan untuk login sebagai pengguna

$ apt install make digunakan untuk menginstal "make" di sistem Debian.

![git](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/c2d021aa-037c-4087-acd9-f5d7e1b8d5e1)

$ apt install git digunakan untuk menginstal perangkat lunak Git di sistem Debian.

$ apt install gcc digunakan untuk menginstal kompiler GCC (GNU Compiler Collection) di sistem Debian.

![github](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/4a03e938-2de0-4e53-bb35-208dc1fc3888)

$ git clone https://github.com/ferryastika/flops-iops mengunduh repositori flops-iops dari GitHub ke dalam direktori 

$ cd flops-iops digunakan untuk berpindah ke direktori yang baru 
