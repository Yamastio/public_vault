tags: [[hacking_intermediate]] [[hacking_tools]]

## apa itu dig ?

`Domain Information Groper` adalah utilitas yang digunakan untuk melakukan query DNS. Tool ini lebih fleksibel dibandingkan `nslookup` dan dapat melakukan berbagai query, seperti pencarian tipe A, MX, dan NS.

### Penggunaan di Kali Linux

Untuk menggunakannya, cukup ketik:

```bash
dig example.com
```

### Contoh dalam Ethical Hacking

- **Menetapkan IP Address**: `dig` membantu mencari alamat IP dari domain tertentu.
- **Menetapkan Nameserver**: Berguna untuk mengetahui server DNS yang digunakan target.
- **Query MX Record**: Untuk mengetahui konfigurasi email dan server mail domain.