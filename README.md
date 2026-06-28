# learning-journal
This repo is about The Journey of me starting to build my Reverse Engineer Journal. So let's begin!

Kenalan dulu ya, Nama saya Muhammad Fadhillah Ardanu , Disini saya ingin membuat perjalanan saya selama belajar Reverse Engineering dan Saya sangat antusias untuk bisa menceritakan kepada pembaca dari repository ini. Jadi, Kalian akan lihat apa saja yang sudah saya pelajari dari perjalanan saya ini. Enjoy!

***Pengertian***

Reverse Engineering adalah Sebuah tindakan membongkar sesuatu dengan tujuan untuk mereplikasi , menganalisa , mempelajari apa yang ada di dalam objek tersebut. Apa yang dianalisa termasuk dari strukturnya , cara kerjanya dan masih banyak lagi.

***Fungsi***

Seperti yang sudah dikutip sebelumnya, Reverse Engineering memiliki banyak fungsi sebagai tindakan yang bisa memahami cara kerja di dalam suatu software maupun hardware. Mari kita ulik apa yang bisa kita dapatkan dari melakukan Reverse Engineering dari 2 aspek tersebut :

**- Reverse Engineering pada Software**

    Dalam dunia software, Reverse ini berguna untuk mengerti arsitektur di dalamnya tanpa mengetahui _source code_ aslinya.
    1. Analisis Malware: Membongkar perangkat lunak berbahaya untuk memahami perilakunya, mencari pembuatnya, dan membuat antivirus.
    2. Pengujian Kerentanan: Mengidentifikasi celah keamanan dalam suatu program agar bisa diperbaiki sebelum dieksploitasi pihak tidak bertanggung jawab.
    3. Interoperabilitas:  proses membedah suatu sistem untuk memahami antarmuka dan fungsinya, sehingga sistem atau perangkat lunak baru dapat bekerja secara lancar dengan sistem lama atau produk pihak ketiga.

**- Reverse Engineering pada Hardware**

    Dalam dunia hardware, berarti memahami apa saja part part yang ada didalamnya untuk bisa di analisa atau dimasukkan part baru tanpa merusak part lamanya.
    1. Proses: Benda fisik diukur secara detail (misalnya menggunakan pemindaian 3D) untuk diubah menjadi cetak biru digital (blueprint).
    2. Inovasi Produk: Membantu perusahaan mempelajari produk kompetitor untuk meningkatkan kualitas rancangan produk mereka sendiri.

***Teknik Analisis**

    Dalam dunia Reverse Engineering, Teknik Menganalisis suatu objek juga penting untuk tahap yang berkelanjutan. Teknik tersebut yaitu diantaranya :
    1. Analytic Static : 
    
        Di teknik ini, Kita sebagai user menganalisa terlebih dahulu apa yang ada di dalam objek tersebut. Seperti halnya jika di momen saat mobil kita dalam keadaan mati. kita buka kap mesinnya, kita pelajari buku manualnya, kita urutkan jalur kabelnya satu per satu pake senter, dan kita catat merek businya. Sama halnya di dunia Reverse, kita sebagai user menganalisa terlebih dahulu bentuknya seperti apa secara keseluruhan tanpa kita menjalankkan program tersebut dibandingkan kita langsung melakukan _Dynamic Analytic_.

    2. Dynamic Analytic : 
    
        Seperti yang sudah saya singgung sebelumnya, _Dynamic Analytic_ adalah analisis secara langsung cara kerja dari objek tersebut bagaimana. Seperti momen saat kita masuk ke dalam mobil, masukin kunci, dan menyalakan mesinnya. kita bawa mobil itu jalan-jalan di jalanan. Sambil jalan, kita pasang alat sensor di mesin buat ngeliat langsung berapa suhu radiatornya saat digas, atau bensin mana yang disedot pas kita belok. Dalam dunia Reverse, _Dynamic Analytic_ dilaukan ketika program dijalankan. Misalnya, saat kita menganalisa malware, kita langsung menganalisa pada saat malware itu bekerja pada PC kita, mulai dari prosesnya , teknik penyerangannya , dampaknya dan lain lain.


***Tools**

    Tidak jauh jauh dari dunia Reverse, Sudah pasti kita akan berbincang pada Tools yang kita pakai untuk melakukan Reverse Engineering. Tools-tools dibawah merupakan Tools yang biasanya dipakai untuk Penganalisaan secara _Static_ maupun _Dynamic_ diantaranya yaitu :

    1. Ghidra SE
    <img width="1130" height="955" alt="image" src="https://github.com/user-attachments/assets/6cbddf13-4320-4747-8b29-8446e7847e4e" />


        Software ini dikembangkan oleh National Security Agency(NSA) yang bersifat _Open Source_. Ghidra menurut saya adalah software yang paling mudah untuk para user yang ingin menganalisa suatu program secara _Static_ dikarenakan Ghidra memiliki fitur pengubah Bahasa mesin(Assembly) menjadi Bahasa Manusia(C/C++). Disamping Ghidra bersifat _Open Source_, Ghidra juga merupakan Software _Multiplatform_ jadi bisa dijalankan di WIndows, Linux, MacOS yang dimana memudahkan para User dari berbagai platform.

    2. x64dbg

        Tools ini merupakan tools yang dikhususkan untuk menjalankan _Dynamic Analytic_. DIkarenakan saya belum pernah menggunakan Software ini, Jadi saya mengkutip dari websitenya langsung x64dbg. Fitur yang ada dari x64dbg diantaranya ada Memory map Symbol view, Thread view, Source code view, Graph view dan masih banyak lagi. Walaupun Software ini bersifat _Open Source_, x64dbg ini masih dikhususkan untuk Windows.


        
        

    
    
