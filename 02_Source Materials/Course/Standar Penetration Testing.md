Tags: [[hacking_fundamentals]] [[blue_team]]

**Standar Penetration Testing (Pentest)** merupakan pendekatan terstruktur untuk menguji keamanan sistem, aplikasi, atau jaringan guna mengidentifikasi dan mengatasi potensi kerentanan. Dua standar utama yang umum digunakan adalah **OWASP (Open Web Application Security Project)** dan **NIST (National Institute of Standards and Technology)**. Berikut penjelasan mengenai kedua standar ini dan bagaimana mereka berperan dalam pengujian keamanan:

---

## OWASP (Open Web Application Security Project)

OWASP adalah organisasi nirlaba yang fokus utamanya adalah meningkatkan keamanan aplikasi web. Proyek ini memberikan berbagai panduan, alat, dan standar yang membantu pengembang dan tim keamanan memastikan keamanan aplikasi mereka. Beberapa kontribusi OWASP yang relevan dalam penetration testing meliputi:

- **OWASP Top Ten**:
    - Daftar tahunan dari sepuluh risiko keamanan aplikasi web paling kritis.
    - Contoh risiko yang umum ditemukan adalah **Injection (seperti SQL Injection)**, **Broken Authentication**, dan **Sensitive Data Exposure**.
    - Panduan ini sangat populer di kalangan pengembang aplikasi dan tim keamanan karena memberikan wawasan praktis untuk mengidentifikasi dan mengurangi risiko keamanan aplikasi web.
- **OWASP Testing Guide**:
    - Sebuah panduan metodologi lengkap untuk menguji keamanan aplikasi web.
    - Meliputi pengujian dalam berbagai area, seperti **validasi input**, **autentikasi**, **manajemen sesi**, dan **konfigurasi server**.
    - Dirancang untuk memastikan setiap aspek aplikasi web diperiksa dengan pendekatan menyeluruh dan terstruktur.

## NIST (National Institute of Standards and Technology)

NIST adalah lembaga pemerintah AS yang merilis standar dan panduan terkait teknologi informasi dan keamanan siber. Dalam konteks penetration testing, beberapa dokumen panduan yang dirilis oleh NIST adalah:

- **NIST SP 800-115 (Technical Guide to Information Security Testing and Assessment)**:
    - Menyediakan panduan langkah-langkah untuk pengujian keamanan informasi, termasuk penetration testing.
    - Melibatkan berbagai pendekatan, seperti **pengujian jaringan**, **pengujian aplikasi**, dan **pengujian sistem**.
    - Panduan ini mencakup **pengumpulan informasi**, **analisis kerentanan**, dan eksploitasi sebagai bagian dari pengujian.
- **NIST Cybersecurity Framework**:
    - Kerangka kerja yang lebih luas daripada sekadar penetration testing, tetapi relevan dalam mendukung keamanan sistem melalui **identifikasi risiko**, **perlindungan**, **deteksi**, **respons**, dan **pemulihan** dari ancaman keamanan.
    - Kerangka kerja ini sering digunakan untuk merancang strategi keamanan organisasi secara holistik.

## Perbandingan OWASP dan NIST dalam Penetration Testing

- **Cakupan Fokus**:
    - **OWASP**: Berfokus pada keamanan aplikasi web dengan pendekatan spesifik untuk menemukan kerentanan pada aplikasi berbasis web.
    - **NIST**: Memiliki cakupan yang lebih luas dan lebih berorientasi pada keamanan sistem secara keseluruhan, termasuk jaringan dan teknologi informasi selain aplikasi web.
- **Penggunaan**:
    - **OWASP** sangat berguna bagi tim pengembang aplikasi web dan tim keamanan yang berfokus pada aplikasi berbasis web.
    - **NIST** lebih relevan bagi organisasi yang membutuhkan standar pengujian keamanan yang lebih luas dan menyeluruh, termasuk infrastruktur jaringan.

## Kesimpulan

Kedua standar ini memiliki kelebihan masing-masing dan dapat digunakan secara bersamaan untuk memberikan pendekatan yang lebih komprehensif dalam pengujian keamanan. Pemilihan standar tergantung pada kebutuhan dan cakupan organisasi, tetapi pemahaman akan keduanya dapat memperkuat upaya pengamanan sistem secara menyeluruh.