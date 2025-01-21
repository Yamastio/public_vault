Tags: [[devops_fundamental]]

## Masalah dalam Proses Pengembangan Aplikasi

1. **Model Waterfall**
    - Waterfall adalah model pengembangan aplikasi yang mengikuti urutan fase yang sistematis dan berurutan, di mana fase satu harus selesai sebelum melanjutkan ke fase berikutnya.
    - Masalahnya, proses ini lambat, kaku terhadap perubahan, dan memiliki siklus rilis yang panjang. Jika ada perubahan di tengah jalan, harus kembali ke fase awal.
    - Banyak perusahaan masih menggunakan model ini karena kultur yang sudah mendarah daging, meski model ini terkenal lambat.
2. **Arsitektur Monolitik**
    - Arsitektur monolitik menggabungkan semua komponen aplikasi dalam satu unit. Contohnya, authentication service, order service, dan account service ditempatkan dalam satu server Back-End.
    - Meski baik untuk pemula, seiring bertambahnya kompleksitas aplikasi, arsitektur ini sulit dikelola karena semua komponen saling bergantung. Jika satu komponen gagal, bisa mempengaruhi komponen lain.
3. **Proses Manual**
    - Proses manual dalam pengembangan aplikasi memperlambat pekerjaan, tidak konsisten, dan rawan kesalahan. Misalnya, konfigurasi server secara manual memakan waktu lama dan rentan kesalahan.
    - Pengujian kode secara manual juga memperlambat proses, serta bisa terjadi kesalahan karena Developer mungkin lupa melakukan pengujian lengkap.
4. **Struktur Tim Tertutup**
    - Tim Developer dan IT Operations sering kali bekerja secara terpisah dan memiliki prioritas yang berbeda, menyebabkan konflik dan saling menyalahkan.
    - Developer fokus pada pengembangan fitur secepat mungkin tanpa memperhatikan kualitas, sementara IT Operations berfokus pada stabilitas infrastruktur.
    - Akibatnya, terjadi masalah saat kode dideploy, yang berujung pada saling tuduh antara tim.

**Solusi: DevOps**

- DevOps hadir sebagai solusi untuk mengatasi masalah kolaborasi antara tim Developer dan IT Operations, meningkatkan efisiensi dan kualitas dalam proses pengembangan aplikasi.

## Pengertian DevOps

**DevOps** adalah kombinasi dari filosofi kultur, sekumpulan praktik, dan rangkaian alat (tools) yang bertujuan untuk meningkatkan kemampuan perusahaan dalam menyajikan aplikasi atau perangkat lunak dengan cepat dan efisien【1】. Istilah ini berasal dari gabungan kata "Developer" (Development) dan "IT Operations" (Operations).

## Tujuan Utama DevOps

- Memadukan tim Developer dan IT Operations untuk bekerja sama dengan lebih baik.
- Menghilangkan hambatan dalam proses pengembangan aplikasi.
- Meningkatkan kecepatan dan kualitas pengembangan serta rilis aplikasi.

## Komponen Utama DevOps:

1. **Filosofi Kultur/Budaya:**
    - Menerapkan budaya berbagi tanggung jawab antara Developer dan IT Operations untuk mengurangi kesenjangan antara kedua tim.
2. **Praktik:**
    - Menggunakan prosedur yang merampingkan cara kerja tim, seperti continuous integration dan continuous delivery (CI/CD), untuk mempercepat proses pengembangan dan memastikan kualitas aplikasi.
3. **Tools (Perangkat Alat):**
    - Mengotomatiskan tugas-tugas berulang, seperti pengujian dan deployment, untuk meningkatkan efisiensi dan reliabilitas proses pengembangan.

## Manfaat DevOps:

- Mempercepat inovasi dan rilis produk.
- Meningkatkan kolaborasi antar tim.
- Memungkinkan perusahaan bersaing lebih efektif di pasar.
- Menyediakan feedback pengguna yang lebih berkualitas, yang berdampak pada peningkatan nilai bisnis.

Dengan DevOps, tim Developer dan IT Operations yang sebelumnya terpisah akan dapat bersatu untuk menciptakan proses pengembangan yang lebih damai dan efisien.

## Manfaat Penerapan DevOps

DevOps membawa banyak manfaat bagi perusahaan dalam hal pengembangan perangkat lunak dan operasional. Berikut ini adalah beberapa manfaat utama dari penerapan DevOps:

1. **Ketangkasan**
    - Meningkatkan kemampuan perusahaan untuk merespons kebutuhan pasar lebih cepat.
    - Memungkinkan perusahaan menciptakan inovasi dengan cepat dan efisien.
    - Microservice dan continuous delivery mempermudah tim dalam merilis pembaruan dengan lebih cepat.
2. **Proses Rilis Cepat**
    - DevOps meningkatkan frekuensi rilis perangkat lunak, memungkinkan perusahaan untuk memperbaiki bug dan menambahkan fitur baru lebih cepat.
    - Praktik seperti continuous integration dan continuous delivery/deployment mengotomatiskan proses rilis perangkat lunak, mulai dari build hingga deployment.
3. **Keandalan**
    - Membantu menjaga kualitas aplikasi dan infrastruktur saat melakukan pembaruan.
    - Menggunakan praktik seperti continuous integration dan continuous delivery/deployment untuk memastikan bahwa setiap perubahan dapat berfungsi dengan baik.
    - Monitoring dan observability memastikan informasi kinerja aplikasi diperoleh secara real-time.
4. **Skalabilitas**
    - DevOps memungkinkan pengelolaan dan pengoperasian infrastruktur serta proses pengembangan aplikasi dalam skala besar.
    - Automasi dan konsistensi membantu mengelola sistem kompleks dengan lebih efisien dan risiko yang lebih rendah.
    - Infrastructure as Code membantu mengelola lingkungan Development, Testing, dan Production dengan lebih andal.
5. **Kolaborasi Meningkat**
    - DevOps mendorong kolaborasi yang lebih erat antara Developer dan IT Operations, berbagi tanggung jawab, dan mengurangi inefisiensi.
    - Developer hanya perlu fokus pada penulisan kode, sedangkan alur kerja otomatis mengelola proses deployment tanpa serah terima manual.
6. **Keamanan**
    - DevOps memungkinkan perusahaan bergerak cepat sambil tetap menjaga keamanan dan compliance.
    - Dengan menggunakan compliance policies otomatis dan teknik manajemen konfigurasi seperti Infrastructure as Code dan Policy as Code, keamanan dapat dikelola dalam skala besar.

Dengan memahami manfaat-manfaat ini, perusahaan dapat lebih yakin untuk mengadopsi DevOps guna meningkatkan efisiensi, inovasi, dan kualitas dalam pengembangan aplikasi.