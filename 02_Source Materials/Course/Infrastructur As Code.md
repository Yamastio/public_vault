Tags: [[devops_fundamental]]

## Infrastructure as Code (IaC)

**Pengertian:** IaC adalah praktik pengelolaan infrastruktur menggunakan kode untuk mengotomatisasi pembuatan dan konfigurasi lingkungan.

**Kategorisasi:**

1. **Infrastructure Automation:**
    - Pembuatan infrastruktur secara otomatis.
    - Memudahkan interaksi dengan infrastruktur dalam skala besar.
    - Contoh tools:
        - **Umum:** Terraform
        - **AWS:** AWS CloudFormation
2. **Configuration Management:**
    - Mengotomatiskan pengonfigurasian sistem operasi dan server.
    - Memastikan perubahan konfigurasi yang dapat diulang dan distandardisasi.
    - Contoh tools:
        - **Umum:** Chef, Puppet, Ansible
        - **AWS:** AWS OpsWorks

## Arsitektur Microservices

**Pengertian:** Pendekatan desain aplikasi sebagai kumpulan layanan yang loosely coupled, di mana setiap layanan memiliki kemampuan spesifik dan berfokus pada tujuan bisnis.

**Keunggulan:**

- Tim dapat bekerja secara independen, mempercepat pengembangan dan deployment.
- Komunikasi antar layanan dilakukan melalui API.

**Topik Terkait:**

1. **Container:**
    - Standarisasi pengemasan kode dan dependensi.
    - Tools untuk manajemen container:
        - **Umum:** Kubernetes, OpenShift
        - **AWS:** Amazon ECS, Amazon EKS
2. **Serverless:**
    - Pendekatan komputasi tanpa pengelolaan infrastruktur.
    - Contoh tools:
        - **Umum:** Serverless, OpenFaaS
        - **AWS:** AWS Lambda

## Monitoring dan Logging

**Pengertian:** Monitoring dan logging penting untuk menilai efektivitas perubahan aplikasi dan infrastruktur serta meningkatkan kualitas pengalaman pengguna.

**Fungsi:**

- Memantau kinerja sistem dan mengidentifikasi masalah sebelum terjadi.
- Menghasilkan data yang cukup dari aplikasi dan layanan dalam bentuk logs, metrics, dan traces.

**Contoh tools:**

- **Umum:** Prometheus, Elastic Stack, Dynatrace
- **AWS:** AWS X-Ray, Amazon CloudWatch

**Tools Terkait:**

1. **AWS X-Ray:**
    - Menganalisis aplikasi terdistribusi dan mengidentifikasi masalah dengan cepat.
2. **Amazon CloudWatch:**
    - Memantau resource dan aplikasi di AWS secara real-time, mengumpulkan logs, dan mengatur pemberitahuan.

## Kesimpulan

Materi ini relevan dengan CALMS Framework, khususnya dalam aspek Automation dan Measurement. Pastikan untuk menguasai alat-alat ini untuk meningkatkan praktik DevOps di lingkungan pengembangan Anda.