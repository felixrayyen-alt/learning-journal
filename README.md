# learning-journal
This repo is about The Journey of me starting to build my Reverse Engineer Journal. So let's begin!

Kenalan dulu ya, Nama saya Muhammad Fadhillah Ardanu, Di sini saya ingin membuat perjalanan saya selama belajar Reverse Engineering dan Saya sangat antusias untuk bisa menceritakan kepada pembaca dari repository ini. Jadi, Kalian akan lihat apa saja yang sudah saya pelajari dari perjalanan saya ini. Enjoy!

## Pengertian

Reverse Engineering adalah Sebuah tindakan membongkar sesuatu dengan tujuan untuk mereplikasi, menganalisa, mempelajari apa yang ada di dalam objek tersebut. Apa yang dianalisa termasuk dari strukturnya, cara kerjanya dan masih banyak lagi.

## Fungsi

Seperti yang sudah dikutip sebelumnya, Reverse Engineering memiliki banyak fungsi sebagai tindakan yang bisa memahami cara kerja di dalam suatu software maupun hardware. Mari kita ulik apa yang bisa kita dapatkan dari melakukan Reverse Engineering dari 2 aspek tersebut:

### Reverse Engineering pada Software

Dalam dunia software, Reverse ini berguna untuk mengerti arsitektur di dalamnya tanpa mengetahui _source code_ aslinya.
1. **Analisis Malware:** Membongkar perangkat lunak berbahaya untuk memahami perilakunya, mencari pembuatnya, dan membuat antivirus.
2. **Pengujian Kerentanan:** Mengidentifikasi celah keamanan dalam suatu program agar bisa diperbaiki sebelum dieksploitasi pihak tidak bertanggung jawab.
3. **Interoperabilitas:** Proses membedah suatu sistem untuk memahami antarmuka dan fungsinya, sehingga sistem atau perangkat lunak baru dapat bekerja secara lancar dengan sistem lama atau produk pihak ketiga.

### Reverse Engineering pada Hardware

Dalam dunia hardware, berarti memahami apa saja part-part yang ada di dalamnya untuk bisa di analisa atau dimasukkan part baru tanpa merusak part lamanya.
1. **Proses:** Benda fisik diukur secara detail (misalnya menggunakan pemindaian 3D) untuk diubah menjadi cetak biru digital (blueprint).
2. **Inovasi Produk:** Membantu perusahaan mempelajari produk kompetitor untuk meningkatkan kualitas rancangan produk mereka sendiri.

## Metode Analisis

Dalam dunia Reverse Engineering, Teknik Menganalisis suatu objek juga penting untuk tahap yang berkelanjutan. Teknik tersebut yaitu di antaranya:

1. **Analytic Static:** Di teknik ini, Kita sebagai user menganalisa terlebih dahulu apa yang ada di dalam objek tersebut. Seperti halnya jika di momen saat mobil kita dalam keadaan mati. Kita buka kap mesinnya, kita pelajari buku manualnya, kita urutkan jalur kabelnya satu per satu pake senter, dan kita catat merek businya. Sama halnya di dunia Reverse, kita sebagai user menganalisa terlebih dahulu bentuknya seperti apa secara keseluruhan tanpa kita menjalankan program tersebut dibandingkan kita langsung melakukan _Dynamic Analytic_.

2. **Dynamic Analytic:** Seperti yang sudah saya singgung sebelumnya, _Dynamic Analytic_ adalah analisis secara langsung cara kerja dari objek tersebut bagaimana. Seperti momen saat kita masuk ke dalam mobil, masukin kunci, dan menyalakan mesinnya. Kita bawa mobil itu jalan-jalan di jalanan. Sambil jalan, kita pasang alat sensor di mesin buat ngeliat langsung berapa suhu radiatornya saat digas, atau bensin mana yang disedot pas kita belok. Dalam dunia Reverse, _Dynamic Analytic_ dilakukan ketika program dijalankan. Misalnya, saat kita menganalisa malware, kita langsung menganalisa pada saat malware itu bekerja pada PC kita, mulai dari prosesnya, teknik penyerangannya, dampaknya dan lain-lain.

## Tools

Tidak jauh-jauh dari dunia Reverse, Sudah pasti kita akan berbincang pada Tools yang kita pakai untuk melakukan Reverse Engineering. Tools-tools di bawah merupakan Tools yang biasanya dipakai untuk Penganalisaan secara _Static_ maupun _Dynamic_ di antaranya yaitu:

1. **Ghidra SE**
<img width="1280" height="640" alt="image" src="https://github.com/user-attachments/assets/2cc18c2c-fe2e-48bd-9970-dca07fb2d325" />

Software ini dikembangkan oleh National Security Agency (NSA) yang bersifat _Open Source_. Ghidra menurut saya adalah software yang paling mudah untuk para user yang ingin menganalisa suatu program secara _Static_ dikarenakan Ghidra memiliki fitur pengubah Bahasa mesin (Assembly) menjadi Bahasa Manusia (C/C++). Di samping Ghidra bersifat _Open Source_, Ghidra juga merupakan Software _Multiplatform_ jadi bisa dijalankan di Windows, Linux, MacOS yang di mana memudahkan para User dari berbagai platform.

2. **x64dbg**
   <img width="1280" height="640" alt="image" src="https://github.com/user-attachments/assets/8d565eba-421f-420a-b7e3-675d4b9cd1d1" />

Tools ini merupakan tools yang dikhususkan untuk menjalankan _Dynamic Analytic_. Dikarenakan saya belum pernah menggunakan Software ini, Jadi saya mengutip dari websitenya langsung x64dbg. Fitur yang ada dari x64dbg di antaranya ada Memory map Symbol view, Thread view, Source code view, Graph view dan masih banyak lagi. Walaupun Software ini bersifat _Open Source_, x64dbg ini masih dikhususkan untuk Windows.

## Teknik Saat Penganalisaan

   Setelah kita memahami metode penganalisaan, Kita masuk pada tekniknya yaitu ada **Disassembler** & **Decompiler**. Kita bayangkan kita dapet kado sebuah Robot Lego raksasa yang udah jadi, dan bata-batanya dilem super kuat dari pabriknya. Robot yang udah jadi ini adalah ibarat Program Aplikasi (Kode Biner yang cuma dipahami komputer). Kita pengen banget tau gimana cara ngerakit robot ini dari awal. Disinilah 2 Teknik ini bekerja seperti dibawah ini :

1. **Disassembler**

   Disassembler adalah software yang menerjemahkan kode mesin menjadi bahasa mesin. Jadi, Kita masukkan robot ini ke pembongkar mesin. Setelah kita bongkar, ternyata memunculkan intruksi seperti "Ambil satu bata merah 2x4. Geser 5 cm ke kanan. Pasang bata merah. Ambil satu bata biru 1x2. Geser 3 cm ke atas. Pasang bata biru." yang dimana disini tidak memiliki Step yang jelas untuk merakit ulang dari robot. Jika manusia dihadapkan intruksi yang sebanyak itu pasti sudah kewalahan. Jadi, Tujuan asli dari Disassembler yaitu :

- Mengintip Instruksi Asli: Ngasih liat kita instruksi paling mentah dari sebuah program (kayak MOV, PUSH, JMP).
  
- Modifikasi / Patching: Karena bahasanya sangat presisi per langkah, kita bisa dengan gampang ngubah satu instruksi. Misalnya, instruksi "Lompat kalau Password Salah" kita ganti jadi "Lompat kalau Password Benar".
  
- Jadi Penyelamat: Kadang programnya diproteksi atau dibikin ribet sama hacker, sehingga mesin Decompiler bingung dan error. Kalo udah gini, Disassembler adalah jalan terakhir karena sejatinya kode mesin itu sudah induk dari induk dari suatu program.
   <img width="680" height="397" alt="image" src="https://github.com/user-attachments/assets/089b5b29-3b8c-427c-a5f0-3084f9eaf36b" />


2. **Decompiler**

   Decompiler adalah Software yang menerjemahkan bahasa mesin menjadi bahasa pemrograman. Lanjutan dari analogi lego robot raksasa, Karena kita tidak mungkin membaca banyak jutaan intruksi dari Disassembler maka kita masuk ke pembongkar mesin kedua yaitu Decompiler, Disini Decompiler sudah merangkum intruksi-intruksi tadi menjadi rangkuman yang jelas dan mudah dibaca. Contoh hasilnya jadi seperti "Langkah 1: Membuat Lengan Kanan. Susun bagian ini untuk membentuk tangan. Langkah 2: Membuat Kepala." Decompiler menerjemahkan langkah-langkah mesin tadi kembali menjadi bahasa pemrograman tingkat tinggi yang mudah dipahami logikanya oleh manusia. Jadi , tujuan aslinya yaitu :
   
- Menghemat Waktu Analisa: Decompiler merangkum semua jadi bahasa yang lebih gampang dibaca (biasanya bahasa C atau C++).

- Melihat Gambaran Besar: Tujuan utamanya biar kita bisa langsung paham alur cerita programnya karena sudah terlihat blueprintnya seperti apa.Kita bisa dengan cepat ngeliat struktur if-else, looping (perulangan), dan rumus matematika aslinya tanpa harus pusing mikirin memori komputer.
   
   <img width="1130" height="955" alt="Screenshot 2026-06-28 184747" src="https://github.com/user-attachments/assets/bed0c859-8427-4808-afd9-ff4cdac65173" />
   
## Apa yang sudah saya pelajari dari Reverse Engineering

   Disini saya sedikit cerita bagaimana saya bisa mempelajari dari Reverse, Jujur saya sedikit kewalahan saat dihadapkan tugas yang langsung menganalisa malware secara Real-time karena saya belum terbiasa dengan bahasa mesin yang serumit itu. Bahkan saya pun masih belum banyak terbiasa dengan bahasa pemrograman tingkat atas seperti Bahasa C / C++. Oleh karena itu, Saya memulai ulang metode belajar saya dari awal yaitu mengerti fundamentalnya terlebih dahulu dengan mengerti **Bagaimana Reverse itu bekerja?**, **Apa yang membuat Reverse serumit itu?**, **Bagaimana cara mengerti poin penting dari cara kerja Reverse ini?**. Jadi, Saya memutuskan untuk belajar bahasanya terlebih dahulu yaitu Bahasa C yang dimana fokus pada poin penting yang mengarah ke mekanisme Reverse itu sendiri. Disini saya sudah merangkum apa yang sudah saya pelajari dari Bahasa C:

### Memori, Pointer, & Array

1. POINTER (Item: Peta Harta Karun)
   
Variabel Biasa (int x = 10;) = Peti Emas. Isinya 10 Gold, ditaruh di Koordinat Hutan (&x).
Pointer (b) = Kertas Peta Harta Karun. Isinya murni cuma tulisan teks Koordinat Hutan (&x). Di dalem kertas ini nggak ada emasnya.
Mantra Bintang (*b) = Skill Teleport & Jarah. Lu baca koordinat di kertas peta, lu teleport ke lokasi peti, lu ambil emasnya.
Mantra Dan (&b) = Laci Meja. Tempat fisik lu nyimpen si kertas peta itu sendiri di basecamp lu.

3. MEMORY MANAGEMENT (Sistem Penyimpanan Barang)
   
- STACK = Tas Inventory Sementara (Dungeon).
  
Semua peti otomatis masuk sini pas lu masuk dungeon (fungsi).
Pas lu keluar dungeon (return 0;), tasnya dibakar otomatis sama Game Engine.
Kapasitasnya mini, kalau kepenuhan bakal Stack Overflow (Game Crash).

- HEAP = Gudang Pusat Kota.
  
Kapasitasnya raksasa, tapi harus sewa manual pake koin mantra malloc().
Penjaga gudang ga ngasih slotnya ke tangan lu, tapi cuma ngasih Resi Koordinat (Pointer).
Kalau lu udah ga pake, lu WAJIB pamit dan balikin slotnya pake mantra free().
Memory Leak = Lu kabur dari game tapi lupa nge-free() gudang. Slotnya kekunci jadi sampah angker, bikin RAM PC lu abis dan Blue Screen.

5. ARRAY & BUFFER OVERFLOW (Barisan Peti & Mantra Terlarang)
   
- Array (rak_peti[3];) = Rak Panjang Isi 3 Peti Berjejer.

 Di level mesin (Assembly), nama rak itu dihapus. Game Engine cuma nginget Koordinat Peti Nomor 0 (Base Address). Mau ke peti selanjutnya? Tinggal pake rumus Lompatan (Offset).
  
- Buffer Overflow = Meluberkan Rak.

Bahasa C itu cuek, ga punya penjaga batas rak (No Bounds Checking). Lu dikasih rak isi 3 peti, tapi lu paksa masukin barang ke peti gaib nomor 4 (rak_peti[3] = 999). C bakal nurut aja. Di dalam Stack, kalau lu luberin data ini sengaja sampai tumpah berantakan, data lu bakal menimpa Return Address (Tiket Pulang) dari dungeon.
Hacker memanfaatkan ini buat ganti Tiket Pulang lu pake koordinat Mantra Terlarang (Shellcode) mereka. Pas fungsi selesai, komputer malah ngejalanin virus si hacker.

## Apa yang masih bingung

Selama saya mendalami dunia Reverse Engineering, Saya mendapati banyak hal yang baru untuk dipelajari dan menurut saya Wajar akan kebingungan dan sedikit bertanya-tanya tentang hal itu. Diantara yang saya belum memahami secara penuh yaitu :

### Operasi Bitwise

Bingung karena rumusnya udah gak cuma tambah-tambahan atau modulo biasa, tapi udah mainan operasi gaib komputer kayak XOR (^), Shift Right (>>), atau Shift Left (<<).

### Control Flow

Bingung karena fungsi pengecekannya sengaja dibikin beranak-pinak atau lompat-lompat (jump/call), jadi saya pusing nyari di mana gerbang utama penentu password-nya yang asli.

