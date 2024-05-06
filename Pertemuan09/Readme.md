[Fork](#fork)

[Orphan](#orphan)

[Zombie](#zombie)

Buat tulisan tentang konsep fork dan implementasinya dengan menggunakan bahasa pemrograman C! (minimal 2 paragraf disertai dengan gambar)
Akses dan clonning repo : https://github.com/ferryastika/operatingsystem.git
Deskripsikan dan visualisasikan pohon proses hasil eksekusi dari kode program fork01.c, fork02.c, fork03.c,

![f1](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/52ea7a36-ad85-48c2-a57f-76bfee15e3ec)

![git1](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/3726203a-b05d-4759-afab-85cbe137e4ec)

## FORK

Sebelum menjalankan fork , lakukan instalasi compiler dengan menggunakan program apt install gcc g++.
perintah tersebut digunakan untuk menginstall compiler bahasa C dan bahasa C++

gcc adalah compiler untuk bahasa C
g++ adalah compiler untuk bahasa C++

![git2](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/403ed72e-b4aa-429a-a60d-9d06d18ac432)

Untuk menjalankan fork01.cpp , menggunakan perintah g++ fork01.cpp -o fork01.exe

![git4](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/d9db813c-71f6-4bc0-853f-340a19f12b2b)

Perintah di atas digunakan untuk mengkompilasi program C++ yang disebut dengan fork01.cpp menggunakan compiler g++ kemudian akan menghasilkan output berupa fork01.exe

Untuk menampilkan program menggunakan perintah nano fork01.cpp 

![git5](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/fbfc3a42-976b-4dfd-8559-009227f0055a)

Untuk menjalankan progam menggunakan perintah ./fork01.exe

![git6 1](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/49214ca4-6da2-4bd4-8d64-20d2acf8b991)

Output program ini menampilkan ID proses (PID), ID proses parent (PPID), dan ID pengguna (UID). Setiap kali program mencetak informasi tersebut, program akan berhenti selama tiga detik sebelum mencetak informasi lagi. Program ini akan diulang sebanyak tiga kali.

Kemudian untuk menjalankan fork02.cpp dan juga fork03.cpp caranya sama seperti menjalankan fork01.cpp

fork02.cpp

![git8](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/90903dc5-075d-4453-bd23-063280337a8b)

![git7](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/51c8a3f3-62ab-4ef5-be98-49ea8815bdfc)

Output dari program tersebut adalah melakukan proses forking secara berulang sebanyak 5 kali, yang menghasilakn proses baru dengan pesan yang mencatat PID masing-masing.

fork03.cpp 

![git10](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/cfcbb22c-d335-4f1e-81aa-71c0663df6a2)

![git9](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/56e233df-9bea-44e6-b639-e59de8c6a4d5)

Output dari program tersebut adalah menampilkan PID mereka sendiri dan nilai variabel x dalam loop tak terbatas. Program menggunakan system call fork() untuk membuat proses saat ini, dan menciptakan child process.

## ORPHAN

Cara penginstalan orphan sama seperti menginstall fork

Sebelum menjalankan orphan , lakukan instalasi compiler dengan cara mengetikkan apt install gcc g++.

perintah tersebut untuk menginstall compiler bahasa C dan bahasa C++

![git12](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/16bd346e-de7e-4e51-bf65-a08335ba8a79)

![git11](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/d02e3e0f-4d62-4db0-a1de-acd42dcb69a1)

![git13 1](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/f5b7e909-d722-4653-b008-54cf90535efd)

Output dari program tersebut adalah menampilkan PID mereka sendiri

## ZOMBIE

Sebelum menjalankan zombie , lakukan instalasi compiler dengan cara mengetikkan apt install gcc g++.

perintah tersebut untuk menginstall compiler bahasa C dan bahasa C++

![git15 1](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/e399230c-819c-41fa-8c8b-dbceac9da090)

![git14](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/918e03d3-5559-4aba-9303-98943b2cfbd4)

![git15 2](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/bc874b5e-091e-4ac0-8ec5-da19bd7922e0)

Output dari program tersebut adalah tidak menampilkan PID
