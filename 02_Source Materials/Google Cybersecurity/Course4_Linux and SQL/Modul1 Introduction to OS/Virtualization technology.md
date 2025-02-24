---
id: Virtualization technology
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Teknologi Virtualisasi

### Apa itu Virtual Machine?

![vm](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/C0Cpca6gRquuxTow47dD1A_2a73d66bee5c40b78984e532c09994f1_82635VQFzN8LaD6GAv3bNTQs6oACAmxKjdlZebYCGsO10hvIVpxBElK4gbJ-KJvmRBsxvQd3XHXUfUtgWzNhR4Va6ODC5D42owmm2vyiluDeV86UAaL9d-pyaxXnjzgHARaWckVzCqj12dnrOq1Ca4o?expiry=1735084800000&hmac=v-lHfqW5poMklx4_sQrCpSa4OX6UH2oPLcAQxQ2V8ig)

- **Virtual Machine (VM)** adalah versi virtual dari komputer fisik. Virtualisasi adalah proses menggunakan perangkat lunak untuk menciptakan representasi virtual dari mesin fisik.
- Mesin virtual (VM) tidak menggunakan perangkat keras fisik, melainkan versi perangkat keras yang didefinisikan oleh perangkat lunak. Sebuah VM memiliki **CPU virtual**, **penyimpanan virtual**, dan perangkat keras virtual lainnya.
- Beberapa VM dapat dijalankan pada perangkat keras fisik yang sama, dengan **memisahkan sumber daya** seperti RAM. Misalnya, komputer dengan 16GB RAM dapat menjalankan tiga VM, masing-masing dengan 4GB RAM.

### Manfaat Virtual Machine

- **Keamanan**: Virtualisasi menyediakan **isolasi** antara VM, yang memberikan lapisan keamanan tambahan. Jika satu VM terinfeksi malware, ia tetap terisolasi dari VM lainnya dan host.
  - Namun, perlu dicatat bahwa ada risiko program berbahaya bisa lolos dari lingkungan virtualisasi dan mengakses mesin host.
- **Efisiensi**: Virtual machine memungkinkan banyak VM berjalan di satu mesin fisik, yang menghemat sumber daya dibandingkan jika setiap tugas harus menggunakan komputer fisik terpisah.
  - Analogi: Virtualisasi seperti **bus kota** yang mengangkut banyak orang sekaligus, dibandingkan jika setiap orang harus menggunakan mobil sendiri.

### Mengelola Virtual Machine

- Virtual machines dikelola dengan perangkat lunak **hypervisor**, yang membantu mengalokasikan dan mengelola sumber daya fisik untuk satu atau lebih VM.
  - **KVM (Kernel-based Virtual Machine)** adalah contoh hypervisor sumber terbuka yang mendukung sebagian besar distribusi Linux dan dibangun langsung ke dalam kernel Linux.

### Bentuk Virtualisasi Lainnya

- Selain VM, ada bentuk virtualisasi lain, seperti **server virtual** yang dibuat dari satu server fisik, atau **jaringan virtual** yang lebih efisien dalam memanfaatkan perangkat keras jaringan fisik.

### Intinya

- **Virtualisasi** adalah teknologi utama dalam industri keamanan karena memberikan manfaat seperti **isolasi malware** dan **efisiensi**. Namun, penting untuk diingat bahwa meskipun aman, masih ada risiko perangkat lunak berbahaya dapat meloloskan diri dari lingkungan virtualisasi.
