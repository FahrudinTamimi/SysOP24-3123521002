**TUGAS PENDAHULUAN:**

_Jawablah pertanyaan-pertanyaan di bawah ini :_

1.Apa yang dimaksud redirection?
_Redirection_ adalah proses mengalihkan aliran input atau output dari sebuah perintah atau proses ke atau dari sebuah file, perangkat, atau proses lain. 

2.Apa yang dimaksud pipeline?
_Pipeline_ adalah sebuah konsep dalam sistem operasi Unix dan Unix-like seperti Linux yang memungkinkan output dari satu perintah menjadi input untuk perintah berikutnya.

3.Apa yang dimaksud perintah di bawah ini : echo, cat, more, sort, grep, wc, cut, uniq

_echo_: Perintah ini digunakan untuk menampilkan teks yang diberikan sebagai argumen ke layar atau ke file.

_cat_: Perintah ini digunakan untuk menggabungkan dan menampilkan isi dari satu atau beberapa file teks ke layar.

_more_: Perintah ini digunakan untuk menampilkan isi dari sebuah file pada terminal.

_sort_: Perintah ini digunakan untuk mengurutkan baris-baris dalam sebuah file teks .

_grep_: Perintah ini digunakan untuk mencari pola tertentu dalam sebuah file teks atau output dari perintah.

_wc_: Perintah ini digunakan untuk menghitung jumlah baris, kata, dan byte dalam sebuah file teks.

_cut_: Perintah ini digunakan untuk memotong bagian-bagian tertentu dari setiap baris dalam sebuah file teks.

_uniq_: Perintah ini digunakan untuk menghilangkan baris duplikat dari sebuah file teks yang telah diurutkan.

**PERCOBAAN:**

1.Login sebagai user.

2.Bukalah Console Terminal dan lakukan percobaan-percobaan di bawah ini. Perhatikan hasil setiap percobaan.

3.Selesaikan soal-soal latihan.

**Percobaan 1 : File descriptor**

1.Output ke layar (standar output), input dari system (kernel)

$ ps

![ps](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/4c2ff56c-55b2-4c7e-b9f7-4179578654b5)

Untuk menampilkan informasi tentang proses yang sedang berjalan di sistem.

2.Output ke layar (standar output), input dari keyboard (standard input)

 $ cat
 
 hallo, apa khabar
 
 hallo, apa khabar
 
 exit dengan ^d
 
 exit dengan ^d
 
 [Ctrl-d]
 
![cat](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/7c3d0081-54b3-4a5e-bf81-cf8e8f80e2c1)

untuk menggabungkan dan menampilkan isi dari satu atau beberapa file teks ke layar.

3.Input nama direktori, output tidak ada (membuat direktori baru), bila terjadi error maka tampilan error pada layar (standard error)

$ mkdir mydir

$ mkdir mydir **(Terdapat pesan error)**

![mkdir](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/aa531113-0572-446a-8508-8c5184ceb36e)

Untuk membuat direktori baru dengan nama mydir

terdapat pesan error karena berkas mydir sudah pernah dibuat atau berkas sudah ada

**Percobaan 2 : Pembelokan (redirection)**

1.Pembelokan standar output

 $ cat 1> myfile.txt
 
 Ini adalah teks yang saya simpan ke file myfile.txt
 
![cat myfile](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/fef67ca6-7c85-434a-b81c-de5e30ef34ed)

cat 1> myfile.txt digunakan untuk menulis teks ke dalam file myfile.txt

2,Pembelokan standar input, yaitu input dibelokkan dari keyboard menjadi dari file

 $ cat 0< myfile.txt
 
 $ cat myfile.txt
 
![pembelokan2](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/e59e42bc-5fb3-45f7-baeb-430b4471ba48)

Untuk membaca teks dari file myfile.txt dan menampilkannya di terminal.

3.Pembelokan standar error untuk disimpan di file

 $ mkdir mydir (Terdapat pesan error)
 
 $ mkdir mydir 2> myerror.txt
 
 $ cat myerror.txt
 
![mydir2](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/b7da8988-39cd-423e-9793-1ff1f8f8b8ed)

Tidak dapat membuat berkas dengan nama mydir karena berkas sudah ada

4.Notasi 2>&1 : pembelokan standar error (2>) adalah identik dengan file descriptor 1.

 $ ls filebaru (Terdapat pesan error)
 
 $ ls filebaru 2> out.txt
 
 $ cat out.txt
 
 $ ls filebaru 2> out.txt 2>&
 
 $ cat out.txt
 
![ls](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/f4226480-10da-4f9a-aa9a-e1b4efff87d5)

5.Notasi 1>&2 (atau >&2) : pembelokan standar output adalah sama dengan file descriptor 2 yaitu standar error

$ echo “mencoba menulis file” 1> baru

$ cat filebaru 2> baru 1>&

$ cat baru

![echo](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/928d21ec-8d22-4f94-a94e-642eb79fbcba)

echo untuk menulis teks ke dalam file "baru"

$ cat baru untuk menampilkan isi dari file baru.

6.Notasi >> (append)

$ echo “kata pertama” > surat

$ echo “kata kedua” >> surat

$ echo “kata ketiga” >> surat

$ cat surat

$ echo “kata keempat” > surat

$ cat surat

![surat](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/1dd4a355-2199-410a-a890-87ab8fc013f5)

Perintah pertama echo "kata pertama" > surat menulis teks "kata pertama" ke dalam file "surat".

Perintah kedua echo "kata kedua" >> surat menambahkan teks "kata kedua" ke dalam file "surat", tanpa menghapus atau mengganti isi yang sudah ada di dalamnya.

Perintah ketiga echo "kata ketiga" >> surat juga menambahkan teks "kata ketiga" ke dalam file "surat".

Perintah cat surat digunakan untuk menampilkan isi file "surat" di terminal. Outputnya akan berisi "kata pertama", "kata kedua", dan "kata ketiga" secara berturut-turut.

Perintah echo "kata keempat" > surat kemudian menulis teks "kata keempat" ke dalam file "surat", menggantikan isi yang sudah ada di dalamnya.

Terakhir, perintah cat surat digunakan lagi untuk menampilkan isi file "surat" di terminal. Outputnya akan berisi hanya "kata keempat".

7.Notasi here document (<<++ .... ++) digunakan sebagai pembatas input dari keyboard. Perhatikan bahwa tanda pembatas dapat digantikan dengan tanda apa saja, namun harus sama dan tanda penutup harus diberikan pada awal baris

$ cat <<++

Hallo, apa kabar?

Baik-baik saja?

Ok!

++

$ cat <<%%%

Hallo, apa kabar?

Baik-baik saja?

Ok!

%%%

![apa kabar](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/bc0aea6d-1b65-4e37-ad9f-30327b74c794)

Perintah cat <<EOF digunakan untuk membaca input dari pengguna hingga menemukan delimiter EOF (End of File).

8.Notasi – (input keyboard) adalah representan input dari keyboard. Artinya menampilkan file 1, kemudian menampilkan input dari keyboard dan menampilkan file 2. Perhatikan bahwa notasi “-“ berarti menyelipkan input dari keyboard

$ cat myfile.txt – surat

![txtsurat](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/32d566a7-9d96-41b3-af03-58ff9f543a4f)

Untuk menampilkan isi di dalam berkas surat.

**Percobaan 3 : Pipa (pipeline)**

1.Operator pipa (|) digunakan untuk membuat eksekusi proses dengan melewati data langsung ke data lainnya.

$ who

$ who | sort

$ who | sort –r

$ who > tmp

$ sort tmp

$ rm tmp

$ ls –l /etc | more

$ ls –l /etc | sort | more

![who](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/307766c5-cf61-472e-82b5-d63f493899a0)

![who2](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/9a4f1251-6ce0-4a62-81b5-e8fb59cd0394)

_who_: Perintah ini digunakan untuk menampilkan daftar pengguna yang saat ini login ke sistem.

_who | sort_: menampilkan daftar pengguna yang login diurutkan berdasarkan nama pengguna.

_who | sort -r:_ Perintah yang sama seperti sebelumnya, namun dengan opsi -r yang akan mengurutkan secara terbalik

_who > tmp_: Output dari perintah who disimpan dalam file sementara yang disebut tmp

_sort tmp_: Isi dari file sementara tmp diurutkan.

_rm tmp_: File sementara tmp dihapus.

_ls -l /etc | more:_ Perintah ls -l /etc menampilkan daftar isi direktori /etc 

2.Untuk membelokkan standart output ke file, digunakan operator ">"

$ echo hello

$ echo hello > output

$ cat output

![output](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/06ef6d9b-d9ab-4484-89ab-eaf2b83439b7)

3.Untuk menambahkan output ke file digunakan operator ">>"

$ echo bye >> output

$ cat output

![output2](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/e352d69c-13ea-48d2-8ca2-069a06d0929f)

4.Untuk membelokkan standart input digunakan operator "<"

$ cat < output

![output3](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/d4a285d5-6558-4b3a-a593-8a9792eb587a)

5.Pembelokan standart input dan standart output dapat dikombinasikan tetapi tidak boleh menggunakan nama file yang sama sebagai standart input dan output.

$ cat < output > out

$ cat out

$ cat < output >> out

$ cat out

$ cat < output > output

$ cat output

$ cat < out >> out (Proses tidak berhenti)

[Ctrl-c]

$ cat out

![output4](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/f60f4ff5-b644-4862-b693-0e6d4d3a1cab)

**Percobaan 4 : Filter**

1.Pipa juga digunakan untuk mengkombinasikan utilitas sistem untuk membentuk fungsi yang lebih kompleks

 $ w –h | grep <user>

 $ grep <user> /etc/passwd

 $ ls /etc | wc

 $ ls /etc | wc –l

 $ cat > kelas1.txt

 Badu

 Zulkifli

 Yulizir

 Yudi
 
 Ade

 [Ctrl-d]

 $ cat > kelas2.txt

 Budi

 Gama
 Asep
 
 Muchlis
 
 [Ctrl-d]
 
 $ cat kelas1.txt kelas2.txt | sort
 
 $ cat kelas1.txt kelas2.txt > kelas.txt
 
 $ cat kelas.txt | sort | uniq
 
![filter2](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/14215fb2-ce57-4cab-8829-1446be885f01)

![filter](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/903ce598-a4e8-4df9-88cb-5eca5576957c)


**LATIHAN:**

1.Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru.

![latihan1](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/05eee8f6-1146-4933-bd97-f1e72a7511ca)

ls > filebaru.txt  untuk melihat daftar lengkap dari direktori aktif dan menyimpannya ke dalam file baru

Setelah menjalankan perintah tersebut, untuk melihat isi dari file myfile.txt ddapat menggunakan perintah cat

2.Lihat daftar secara lengkap pada direktori /etc/passwd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.

![latihan2](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/b8b7f55c-b4e0-4b28-9a0d-f54a4b25372c)

cat /etc/passwd >> filebaru.txt untuk mengambil berkas kemudian menambahkan berkasnya ke dalam filebaru.txt 

3.Urutkan file baru dengan cara membelokkan standard input.

![latihan3](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/62954138-61e7-443c-84c2-aee9e18f16bf)

Untuk mengurutkan isi berkas yang ada di myfile.txt menggunakan perintah sort  < filebaru.txt.

4.Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut.

![latihan4](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/05735c40-4dcc-44c0-9145-7e7623197dcd)

Sort <filebaru.txt > filebaru.urut: Untuk mengurutkan isi berkas yang ada di filebaru.txt kemudian dipindahkan ke berkas filebaru.urut

5.Buatlah direktori latihan 2 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt.

![latihan5](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/c8ffa6d4-ef7c-4d9e-a8a8-b29f18080c4f)

Mkdir latihan2 2> rmdirerror.txt: untuk membuat direktori baru dengan nama "latihan2". Jika direktori tersebut tidak dapat dibuat dan menghasilkan pesan kesalahan, pesan kesalahan tersebut akan dialihkan ke berkas yang disebut "rmdirerror.txt"

6.Urutkan kalimat berikut :

Jakarta

Bandung

Surabaya

Padang

Palembang

Lampung

![latihan6](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/18d7cffb-6066-4dfc-9c24-11dcf79c63c4)

Untuk mengurutkan teks menggunakan berintah sort << @@@..... kemudian progam akan bekerja hingga user mengetikkan @@@ lagi

7.Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.

![latihan7](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/f5aedce1-4dab-4dbd-8957-bd25a767b439)

![latihan7 1](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/7245c27d-e927-4b3f-b759-e42e4416a567)

Wc filebaru.urut >> filebaru untuk menghitung jumlah baris, kata dan karakter pada filebaru.urut kemudian dipindahkan ke dalam berkas filebaru.

8.Gunakan perintah di bawah ini dan perhatikan hasilnya.

 $ cat > hello.txt
 
 dog cat
 
 cat duck
 
 dog chicken
 
 chicken duck
 
 chicken cat
 
 dog duck
 
 [Ctrl-d]
 
 $ cat hello.txt | sort | uniq
 
 $ cat hello.txt | grep “dog” | grep –v “cat”
 
![latihan8](https://github.com/FahrudinTamimi/SysOP24-3123521002/assets/160558690/502a377f-0d0b-45b5-884f-b0f0d8c4eb8c)

cat > hello.txt digunakan untuk membuat atau mengedit berkas bernama "hello.txt" dengan menggunakan input dari keyboard dan akan berhenti ketika menekan [Ctrl-d] .

cat hello.txt | sort | uniq digunakan untuk mengurutkan dan menghapus baris duplikat dari isi berkas "hello.txt".

cat hello.txt | grep "dog" | grep -v "cat" digunakan untuk menampilkan baris-baris dari berkas "hello.txt" yang mengandung kata "dog" tetapi tidak mengandung kata "cat".



