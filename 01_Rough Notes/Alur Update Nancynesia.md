---
id: Alur Update Nancynesia
aliases: []
tags: []
---

Berikut alur langkah-langkah yang perlu Anda lakukan setiap kali Anda ingin melakukan update, seperti menambah halaman atau mengubah konten di proyek Hugo dan meng-deploy perubahan ke `rmdeploy` branch:

### 1. **Lakukan Perubahan di Lokal**

- Tambahkan atau ubah halaman, konten, atau aset di dalam proyek Hugo Anda (misalnya di dalam folder `content`, `layouts`, atau `static`).

### 2. **Jalankan Hugo untuk Membangun Website**

- Buka terminal dan navigasikan ke direktori proyek Hugo Anda.
- Jalankan perintah berikut untuk membangun website secara lokal dan memastikan tidak ada masalah:
  ```bash
  hugo
  ```

### 3. **Tambahkan Perubahan ke Git**

- Setelah memastikan perubahan sudah benar, tambahkan perubahan ke staging area dengan perintah:
  ```bash
  git add .
  ```

### 4. **Commit Perubahan**

- Commit perubahan dengan pesan yang deskriptif:
  ```bash
  git commit -m "Deskripsi perubahan yang dilakukan"
  ```

### 5. **Push Perubahan ke Branch `main`**

- Push perubahan ke branch `main` di remote (GitHub):
  ```bash
  git push origin main
  ```

### 6. **Split Branch `main` ke `rmdeploy`**

- Untuk membuat branch `rmdeploy` yang hanya berisi folder `public`, jalankan:
  ```bash
  git subtree split --prefix public -b rmdeploy
  ```

### 7. **Push Branch `rmdeploy` ke Remote**

- Push branch `rmdeploy` ke remote untuk di-deploy:
  ```bash
  git push origin rmdeploy:rmdeploy --force
  ```

### 8. **Cek Deployment di cPanel**

- Pastikan perubahan sudah berhasil di-deploy dengan memeriksa website Anda di `http://nancynesia.com`.

**Catatan:**

- Anda tidak perlu menghapus branch `rmdeploy` di lokal jika Anda ingin tetap menyimpannya. Jika ingin membersihkannya setelah push, Anda bisa menghapusnya dengan perintah:

  ```bash
  git branch -D rmdeploy
  ```

- Pastikan `.cpanel.yml` ada di branch `main` untuk memastikan bahwa konfigurasi otomatis untuk deployment berjalan dengan benar di cPanel.

Dengan mengikuti alur ini, setiap kali Anda melakukan perubahan di proyek, perubahan tersebut dapat secara otomatis di-deploy ke server cPanel setelah Anda melakukan push ke `main` dan split ke `rmdeploy`.
