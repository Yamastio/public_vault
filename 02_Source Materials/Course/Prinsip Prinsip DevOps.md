Tags: [[devops_fundamental]]

## Pengantar The Three Ways: Prinsip-Prinsip yang Mendasari DevOps

Setelah memahami pengertian DevOps, kita dapat melangkah lebih jauh dengan mempelajari prinsip-prinsip utama yang mendasari DevOps, yang dikenal sebagai _The Three Ways_. Prinsip-prinsip ini membantu perusahaan untuk meningkatkan kecepatan, kualitas, dan efisiensi dalam pengembangan dan pengiriman perangkat lunak. Konsep ini terinspirasi dari transformasi yang terjadi di dunia manufaktur pada tahun 1980-an, saat perbaikan alur kerja, umpan balik, dan eksperimen berkelanjutan membawa dampak signifikan dalam meningkatkan produktivitas dan kualitas produk.

DevOps juga bertujuan untuk mentransformasi cara perusahaan memanfaatkan teknologi dengan fokus pada kolaborasi antara tim Developer dan IT Operations serta peningkatan produktivitas dalam pengembangan aplikasi. Berikut adalah tiga prinsip utama yang dikenal sebagai _The Three Ways_ dalam DevOps:

### 1. Prinsip Alur Kerja (Flow)

Prinsip pertama ini menekankan pada optimalisasi alur kerja dari pengembangan hingga produksi. Dalam konteks DevOps, alur kerja yang cepat memungkinkan perusahaan untuk merilis fitur dan memperbaiki aplikasi lebih cepat. Prinsip ini berfokus pada mempercepat penyelesaian pekerjaan dari Developer, melalui IT Operations, hingga aplikasi bisa digunakan oleh pengguna. Dengan menerapkan alur kerja yang efisien, perusahaan dapat mengurangi hambatan dan mempercepat waktu ke pasar.

### 2. Prinsip Umpan Balik (Feedback)

Prinsip kedua ini bertujuan untuk menciptakan sistem umpan balik yang terus-menerus antara berbagai tim dan pengguna. Umpan balik yang cepat dan efisien memungkinkan perusahaan untuk mendeteksi dan memperbaiki masalah sebelum berkembang lebih besar. Melalui praktik seperti monitoring aplikasi secara real-time dan observability, perusahaan dapat mengumpulkan data tentang kinerja aplikasi dan merespons perubahan kebutuhan pengguna dengan cepat.

### 3. Prinsip Pembelajaran dan Eksperimen Berkelanjutan (Continuous Learning and Experimentation)

Prinsip terakhir menekankan pentingnya budaya belajar dan eksperimen yang berkelanjutan. Ini melibatkan pengulangan dan latihan untuk menguasai keterampilan baru, serta kesediaan untuk mengambil risiko melalui eksperimen. Dengan terus bereksperimen, perusahaan dapat belajar dari keberhasilan maupun kegagalan, yang pada akhirnya akan mendorong inovasi dan peningkatan kinerja.

## The First Way: Prinsip terkait Alur Kerja dalam DevOps

**Prinsip The First Way** menekankan pentingnya menciptakan alur kerja yang cepat dan lancar antara Development dan Operations, hingga akhirnya aplikasi sampai di tangan pengguna. Dalam DevOps, pekerjaan mengalir dari Development ke Operations, memastikan bahwa fitur atau pembaruan perangkat lunak dapat dirasakan manfaatnya oleh pengguna.

### Membuat Pekerjaan Menjadi Tampak

Pekerjaan dalam bidang IT sering kali tidak tampak secara fisik. Untuk itu, diperlukan visualisasi alur kerja, seperti menggunakan **Kanban board** atau **Scrum board**. Papan ini membantu memantau pekerjaan, mulai dari tahap awal (backlog) hingga selesai (delivered). Setiap tugas direpresentasikan dalam bentuk card yang dipindahkan dari satu kolom ke kolom lainnya, sesuai dengan tahap pengerjaannya.

### Membatasi Work In Process (WIP)

Untuk menghindari multitasking yang berlebihan, perlu ada pembatasan jumlah pekerjaan yang sedang dikerjakan dalam satu waktu (Work In Process/WIP). Dengan menetapkan batas WIP pada kolom tertentu di **Kanban board**, kita dapat memastikan bahwa tugas tidak menumpuk, sehingga alur kerja lebih fokus dan efisien.

### Mengurangi Skala Batch yang Dikerjakan

**Skala batch yang kecil** memungkinkan pekerjaan diselesaikan lebih cepat dan kesalahan dapat terdeteksi lebih awal. Dengan melakukan pekerjaan dalam unit kecil (single-piece flow), alur kerja menjadi lebih cepat, dan kesalahan bisa diperbaiki dengan segera, tanpa menunggu seluruh batch selesai.

### Memangkas Jumlah Handoff

Handoff, atau penyerahan pekerjaan dari satu tim ke tim lain, dapat menjadi penghambat dalam alur kerja. Dengan meminimalkan jumlah handoff dan menggunakan alat seperti **version control system** (misalnya, Git), tim dapat bekerja lebih cepat dan mengurangi waktu tunggu antar proses. Ini juga meminimalkan risiko miskomunikasi yang sering terjadi saat perpindahan tanggung jawab.

## The Second Way: Prinsip Terkait Umpan Balik

Prinsip ini berfokus pada menciptakan alur umpan balik yang cepat dari **Operations** ke **Development** guna mendeteksi masalah sedini mungkin dan mencegah masalah terulang. Feedback yang cepat memungkinkan perbaikan lebih awal, yang menghasilkan sistem kerja yang lebih aman dan tanggap.

Sebagai contoh, jika tim **Operations** menemukan masalah performa aplikasi, feedback kepada tim **Developer** harus diberikan segera agar aplikasi bisa diperbaiki sebelum diluncurkan ke **Production**. Sistem yang efektif harus mampu menemukan masalah secepat mungkin agar tidak terjadi kegagalan besar.

### Swarming dalam Menyelesaikan Masalah

DevOps menggunakan pendekatan **swarming** untuk menyelesaikan masalah, yang berbeda dengan sistem tradisional **three-tier support hierarchy**. Swarming menghindari eskalasi antar level yang berpotensi menimbulkan antrean dan memperlambat proses. Dalam model swarming:

1. Masalah diserahkan langsung kepada individu yang paling mungkin dapat menyelesaikannya.
2. Masalah diawasi sampai selesai.
3. Tim yang terlibat dalam swarming biasanya terdiri dari ahli (SME - **Subject Matter Expert**) yang bisa langsung menangani masalah kritis.

### Mendorong Tanggung Jawab ke Tempat Asalnya

Efisiensi dalam pengambilan keputusan ditingkatkan dengan memberikan wewenang kepada orang-orang yang langsung terlibat dalam proses. Dengan demikian, **Developer** yang menemukan masalah dapat langsung memperbaikinya tanpa harus menunggu persetujuan dari tim lain, yang biasanya memperlama waktu penyelesaian.

Inisiatif yang dapat diambil meliputi:

- Peer review terhadap perubahan kode.
- Otomatisasi proses pengujian kode.
- Eliminasi birokrasi dalam penjadwalan pengujian.

### Mengoptimalkan Kualitas Operasional

Kualitas operasional harus dioptimalkan dengan memperhatikan **arsitektur**, **kinerja**, **stabilitas**, **keamanan**, dan **konfigurasi**. Pelanggan internal (tim **Operations**) dan eksternal (pengguna aplikasi) sama pentingnya untuk diutamakan, sehingga aplikasi yang dikembangkan dapat berjalan lancar dan sesuai ekspektasi pengguna.

### Kesimpulan

Prinsip kedua dalam DevOps ini menekankan pentingnya umpan balik cepat dari Operations ke Development untuk memastikan kualitas aplikasi, keamanan, dan keandalan infrastruktur. Model **swarming** dan praktik **continuous integration** serta **continuous deployment** dengan **automated tests** adalah beberapa cara untuk memastikan feedback tersampaikan dengan cepat dan masalah dapat diperbaiki sebelum aplikasi dirilis ke publik.

## The Third Way

"The Third Way" adalah prinsip yang berkaitan dengan **proses belajar dan eksperimen berkelanjutan** dalam organisasi, khususnya dalam konteks **DevOps** dan **pengembangan aplikasi**. Prinsip ini menekankan pentingnya membangun budaya belajar yang didorong oleh eksperimen, dimana kegagalan dan keberhasilan keduanya berkontribusi pada peningkatan tim dan perusahaan secara keseluruhan.

### Poin Utama The Third Way:

1. **Eksperimen Berkelanjutan:** Eksperimen yang terus-menerus dilakukan dalam pekerjaan sehari-hari untuk menciptakan inovasi dan peningkatan sistem. Hal ini termasuk memperbaiki bug, refactoring kode, dan mengoptimalkan alur kerja tanpa menunggu persetujuan yang berbelit-belit.
2. **Organizational Learning:** Budaya organisasi yang mengedepankan pembelajaran kolektif, di mana kesalahan tidak dijadikan alasan untuk menghukum seseorang, melainkan digunakan untuk memahami akar masalah dan memperbaiki sistem agar lebih tangguh di masa depan.
3. **Mengubah Pengetahuan Lokal Menjadi Global:** Pengetahuan dan keterampilan yang diperoleh secara lokal (dalam tim) harus didokumentasikan dan disebarkan ke seluruh organisasi, sehingga seluruh perusahaan bisa mendapatkan manfaat dari pembelajaran tersebut.
4. **Eksperimen pada Skala Harian:** Mengintegrasikan eksperimen ke dalam pekerjaan sehari-hari agar tim terus berkembang. Contoh dalam dunia IT adalah latihan simulasi kegagalan sistem atau menambah beban kerja pada aplikasi untuk mengidentifikasi kelemahan dan memperbaikinya sebelum benar-benar terjadi masalah besar.
5. **Hubungan Pemimpin dan Pekerja:** Pemimpin berperan dalam menciptakan lingkungan di mana tim bisa belajar dan bereksperimen secara mandiri. Pemimpin harus mendorong target jangka pendek yang jelas dan mendukung proses belajar tim, bukan hanya berfokus pada hasil akhir saja.

### Kesimpulan:

"The Third Way" membantu organisasi membangun **kultur yang berani mengambil risiko**, belajar dari kegagalan, dan memperbaiki proses secara terus-menerus. Dengan membangun kepercayaan dan mendukung inovasi, perusahaan dapat menciptakan tim yang lebih tangguh dan inovatif dalam menghadapi tantangan.