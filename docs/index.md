# Sistem Bilangan

Angka adalah simbol untuk menyatakan nilai atau jumlah. Simbol itu sendiri tidak memiliki arti sebelum disepakati aturan tentang cara membaca, menulis, dan menafsirkannya. Aturan yang memberikan makna pada sekumpulan simbol angka inilah yang disebut **sistem bilangan** (*number system*). Sistem bilangan menetapkan simbol yang sah, cara penulisan, serta bagaimana nilai suatu bilangan ditentukan berdasarkan posisi setiap digitnya. Dengan sistem bilangan, setiap angka memperoleh makna yang konsisten sehingga dapat digunakan dalam berbagai perhitungan.

## Bilangan Desimal

Sistem yang paling lazim digunakan manusia adalah **sistem bilangan desimal** dengan **basis 10**. Sistem ini hanya menyediakan sepuluh digit, yaitu **0, 1, 2, 3, 4, 5, 6, 7, 8, dan 9**. Nilai tempat dimulai dari posisi paling kanan sebagai satuan (10⁰), kemudian puluhan (10¹), ratusan (10²), ribuan (10³), dan seterusnya; setiap pergeseran satu posisi ke kiri membuat nilai tempat menjadi sepuluh kali lipat. Contohnya, bilangan **9876₁₀** dapat diuraikan menjadi (9×10³) + (8×10²) + (7×10¹) + (6×10⁰) = 9000 + 800 + 70 + 6 = 9876₁₀. Digit 9 bernilai 9000 karena berada di posisi ribuan, 8 bernilai 800, 7 bernilai 70, dan 6 tetap 6. Posisi setiap digit menjadi penentu utama nilai akhir bilangan.

Sistem desimal juga menerapkan mekanisme *carry*. Karena setiap digit hanya boleh bernilai 0–9, ketika sebuah digit yang sudah bernilai 9 ditambah 1, ia kembali ke 0 dan nilai 1 dipindahkan ke posisi sebelah kiri. Proses inilah yang menghasilkan urutan 9 menjadi 10, 99 menjadi 100, dan seterusnya. Mekanisme yang sama berulang di setiap nilai tempat sehingga sistem desimal mampu merepresentasikan bilangan yang terus membesar tanpa menambah simbol baru.

## Bilangan Biner

Komputer tidak menggunakan sistem desimal, melainkan **sistem bilangan biner** dengan **basis 2** yang hanya memiliki dua simbol: **0** dan **1**. Nilai tempat pada sistem biner dihitung berdasarkan pangkat dua, dimulai dari 2⁰ = 1 di posisi paling kanan, lalu 2¹ = 2, 2² = 4, 2³ = 8, dan seterusnya; setiap pergeseran ke kiri menggandakan nilai tempat, sedangkan ke kanan membaginya dua. Karena digit maksimum hanya 1, penambahan 1 pada digit yang sudah bernilai 1 akan memicu *carry*: digit tersebut kembali ke 0 dan nilai 1 dibawa ke posisi kiri. Akibatnya, urutan bilangan biner menjadi 0₂ → 1₂ → 10₂ → 11₂ → 100₂ → 101₂ → 110₂ → 111₂ → 1000₂. Untuk memperoleh nilai desimalnya, jumlahkan hasil kali setiap digit dengan nilai tempatnya. Contoh, **1010₂** = (1×2³) + (0×2²) + (1×2¹) + (0×2⁰) = 8 + 0 + 2 + 0 = 10₁₀.

## Bilangan Heksadesimal

Penulisan bilangan biner cenderung panjang, misalnya 255 desimal membutuhkan 11111111₂. Untuk meringkasnya, digunakan **sistem bilangan heksadesimal** dengan **basis 16**. Sistem ini menyediakan enam belas simbol, yaitu **0–9** dan **A–F** dengan A=10, B=11, C=12, D=13, E=14, F=15. Nilai tempatnya menggunakan pangkat 16: 16⁰=1, 16¹=16, 16²=256, 16³=4096, dan seterusnya. Contoh, **2AF₁₆** = (2×16²) + (10×16¹) + (15×16⁰) = 512 + 160 + 15 = 687₁₀.

Keunggulan utama heksadesimal terletak pada hubungan tetapnya dengan biner: setiap satu digit heksadesimal selalu mewakili tepat empat bit, seperti ditunjukkan pada tabel berikut.

| Heksadesimal | Biner | Desimal |
|--------------|-------|---------|
| 0            | 0000  | 0       |
| 1            | 0001  | 1       |
| 2            | 0010  | 2       |
| 3            | 0011  | 3       |
| 4            | 0100  | 4       |
| 5            | 0101  | 5       |
| 6            | 0110  | 6       |
| 7            | 0111  | 7       |
| 8            | 1000  | 8       |
| 9            | 1001  | 9       |
| A            | 1010  | 10      |
| B            | 1011  | 11      |
| C            | 1100  | 12      |
| D            | 1101  | 13      |
| E            | 1110  | 14      |
| F            | 1111  | 15      |

Dengan tabel ini, konversi biner ke heksadesimal cukup dilakukan dengan mengelompokkan bit per empat dari kanan. **11001010₂** dikelompokkan menjadi 1100 dan 1010, lalu diubah menjadi **C** dan **A** sehingga hasilnya **CA₁₆**. Sebaliknya, **3F₁₆** langsung diubah menjadi 0011 dan 1111, yaitu **00111111₂**. Heksadesimal menjadi cara ringkas menampilkan data biner tanpa mengubah informasi yang dikandungnya.

## Representasi Data

Setelah memahami bahwa komputer hanya mengenali deretan bit, muncul pertanyaan: bagaimana komputer membedakan apakah rangkaian 0 dan 1 itu mewakili huruf, angka, atau gambar? Jawabannya terletak pada **representasi data**, yaitu aturan yang menerjemahkan berbagai jenis informasi ke dalam bentuk biner agar dapat disimpan, diproses, dan dikirim. Bagi komputer, semua data hanyalah untaian bit; maknanya baru muncul ketika mesin menerapkan aturan representasi yang sesuai.

Ketika pengguna mengetik huruf **A**, komputer tidak menyimpan bentuk visualnya. Sistem mencari nilai yang mewakili huruf A menurut standar representasi karakter, lalu mengubahnya menjadi biner sebelum disimpan. Saat dibaca kembali, proses sebaliknya terjadi: deretan bit ditafsirkan dengan aturan yang sama sehingga huruf A tampil di layar. Standar paling dasar untuk hal ini adalah **ASCII** (*American Standard Code for Information Interchange*). Dalam ASCII, huruf A disimpan sebagai 65₁₀ atau **01000001₂**, B sebagai 66₁₀ (01000010₂), dan C sebagai 67₁₀ (01000011₂).
