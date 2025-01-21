Tags: [[computational]]

## Memory RAM dan CPU

Menyimpan sesuatu, menyimpan aliran listrik. Satuan terkecil dari memory == gated latch

Sistem di dalam 1 gated latch:

1. Data In == data yang ingin dimasukan ke memory
2. Write Enable == mengatur apakah akan di masukan / tidak
3. Data Out == mengeluarkan apa yang disimpan tadi

Sistem diatas hanya 1 bit saja, jika 8 bit atau 1 byte register atau 8 gated latch maka munculah RAM (Random Access Memory) == Memory Sementara

RAM

Satu register (8 bit/8 gated lathced) akan tersimpan dalam satu memory dan memiliki alamat(address)

Di dalam RAM ada 2 BUS (suatu input/output untuk memasukan data)

1. Data Bus → Output dari data yang tersimpan
2. Address Bus → untuk mencari suatu address di dalam suatu RAM, misal ingin cari data address nya 5, maka cari address 5 lalu RAM balikin ke ALU menggunakan Data Bus

Register == Mirip RAM, secara fungsi sama tapi beda tujuan. Register khusus untuk operasi saja, RAM untuk menyimpan suatu bilangan.

Selain Register ada juga Instruction Register == Digunakan untuk instruksi tertentu, jadi dialam RAM selain menyimpan data, kita bisa menaruh instruksi juga.

Ada juga Instruction Address Register, ini untuk menyimpan urutan dari Register tadi. Misal yang pertama kita ingin gunakan operasi tambah dulu, baru kali seperti itu. Yang terjadi maka jika yang pertama berada di Address 7, maka selanjutnya akan tersimpan di Address 8, karena address ke 7 sudah ada isinya.

Ada juga Clock → mengatur agar satu cycle itu berjalan pada waktu yang sama(konsisten), sehingga bisa di prediksi akan selesai kapan.

Nah semuanya diatas itu berada di dalam Chip CPU, ada ALU(melakukan operasi aritmatika) dan Control Unit (Mengatur Instruction itu tadi)

### Cycle (Siklus dalam menyelesaikan instruksi)

1 Cycle itu ada :

1. Fetch (mengambil data dari RAM)
2. Decode (mengetahui isi dari Output)
3. Execute (menjalankan suatu progress)

1 Cycle satuanya hertz, jadi misal 5 hertz maka 5 cycle/detik

### 32 Bit vs 64 Bit

Perbedaanya:

1. 64 Bit bisa membawa lebih banyak data
2. Lebih cepat karena RAM nya lebih besar

### Overclocking

Memaksa CPU yang tadinya bekerja di 5GHz, maka bisa dipaksa bisa jadi lebih kenceng lagi. Jadi yang tadinya transfer data selesai lama bisa lebih cepat lagi dalam beberapa cycle.

### Multicore CPU

1 cycle(siklus instruksi) itu dihandle oleh 1 core CPU saja, jadi jika multicore maka yang handle itu tidak hanya 1 core. Jadi ada 4 jumlah CPU yang menghandle 1 cycle ini, sehingga prosesnya lebih cepat lagi. Bekerja nya secara independen ya, jadi 1 cycle itu 1 core, bukan 1 cycle dikerjakan bersama ber-4. Jika satu instruksi memerlukan 4 siklus untuk selesai, instruksi tersebut akan dieksekusi oleh satu core dalam 4 cycle berturut-turut. Jika ada 4 Instruksi berbeda, maka bisa dikerjakan dalam waktu yang sama, setiap core 1 siklus tadi

1 Core punya memori sendiri, karena dalam 1 chip yang sama maka ada shared memory. Untuk Bus Interface nya sama, cuma cycle nya saja yang berjalan paralel jadi lebih cepat

