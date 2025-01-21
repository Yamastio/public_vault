Tags: [[hacking_tools]] [[coding_tools]]

## Apa itu Tmux?
**Tmux** (Terminal Multiplexer) adalah alat yang memungkinkan pengguna untuk membuka beberapa terminal dalam satu sesi terminal. Dengan Tmux, Anda dapat:
1. Membagi terminal menjadi beberapa pane.
2. Membuat dan mengelola beberapa sesi terminal yang dapat ditinggalkan dan dilanjutkan di lain waktu (detach dan attach session).
3. Mempermudah pengelolaan workflow pada terminal, terutama dalam pengembangan atau administrasi sistem.

---

## Fitur Utama Tmux
1. **Session Management**: Membuat, menyimpan, dan melanjutkan sesi terminal.
2. **Pane Management**: Membagi layar menjadi beberapa bagian (horizontal atau vertikal).
3. **Window Management**: Membuka banyak jendela di dalam sesi.
4. **Customizable Key Bindings**: Mendukung konfigurasi untuk shortcut yang lebih fleksibel.
5. **Plugin Support**: Mendukung ekstensi dengan plugin seperti *Tmux Plugin Manager (TPM)*.

---

## Cheatsheet Tmux
### Session Management
1. **Start Session**
   ```bash
   tmux
   ```
   Membuka sesi default tanpa nama.

   ```bash
   tmux new -s <name_session>
   ```
   Membuka sesi baru dengan nama spesifik.

2. **Detach Session**
   - Shortcut:
     ```bash
     ctrl + b -> d
     ```
   - Membebaskan sesi agar dapat dilanjutkan di lain waktu tanpa menutupnya.

3. **Attach Session**
   ```bash
   tmux a
   ```
   Melanjutkan sesi terakhir yang aktif.

   ```bash
   tmux a -t <name_session>
   ```
   Melanjutkan sesi tertentu berdasarkan nama.

4. **Show List of Sessions**
   ```bash
   tmux ls
   ```
   Menampilkan semua sesi aktif.

5. **Kill Session**
   ```bash
   tmux kill-session -t <name_session>
   ```
   Menutup sesi berdasarkan nama.

6. **Kill All Sessions**
   ```bash
   tmux kill-server
   ```
   Menutup semua sesi Tmux yang sedang berjalan.

---

### Window Management
1. **Add New Window**
   ```bash
   ctrl + b -> c
   ```
   Membuat jendela baru di dalam sesi.

2. **Change Window**
   ```bash
   ctrl + b -> n
   ```
   Berpindah ke jendela berikutnya.

   ```bash
   ctrl + b -> p
   ```
   Berpindah ke jendela sebelumnya.

   ```bash
   ctrl + b -> w
   ```
   Menampilkan daftar jendela untuk dipilih.

3. **Rename Window**
   ```bash
   ctrl + b -> ,
   ```
   Mengganti nama jendela aktif.

4. **Kill Window**
   ```bash
   ctrl + b -> & 
   ```
   Menutup jendela aktif.

---

### Pane Management
1. **Split Pane Horizontally**
   ```bash
   ctrl + b -> %
   ```
   Membagi layar secara horizontal.

2. **Split Pane Vertically**
   ```bash
   ctrl + b -> "
   ```
   Membagi layar secara vertikal.

3. **Change Pane (Navigasi Antar Pane)**
   ```bash
   ctrl + b -> [arrow keys]
   ```
   Navigasi menggunakan tombol panah.

   ```bash
   ctrl + b -> q -> <index>
   ```
   Menampilkan nomor indeks untuk berpindah ke pane tertentu.

4. **Resize Pane**
   ```bash
   ctrl + b -> [hold arrow keys]
   ```
   Mengatur ukuran pane secara manual.

5. **Change Pane Layout**
   ```bash
   ctrl + b -> space
   ```
   Mengubah tata letak pane secara otomatis.

6. **Kill Pane**
   ```bash
   ctrl + b -> x
   ```
   Menutup pane aktif.

---

### **Shortcut Penting Lainnya**
1. **Scroll Mode**
   ```bash
   ctrl + b -> [
   ```
   Masuk ke mode scroll untuk melihat output sebelumnya.
   - Keluar dari mode scroll:
     ```bash
     q
     ```

2. **Reload Config**
   ```bash
   ctrl + b -> :source-file ~/.tmux.conf
   ```

---

### Konfigurasi Tambahan
1. **Edit Config File**
   ```bash
   nano ~/.tmux.conf
   ```

2. **Contoh Konfigurasi Dasar**
   ```bash
   # Enable mouse support
   set -g mouse on

   # Set vi-mode for pane navigation
   setw -g mode-keys vi

   # Change prefix key from ctrl+b to ctrl+a
   set-option -g prefix C-a
   unbind-key C-b
   bind-key C-a send-prefix

   # Status bar customization
   set -g status-bg black
   set -g status-fg green
   set -g status-left "[#S]"
   ```

3. **Reload Config**
   Setelah menyimpan konfigurasi, reload tanpa menutup sesi:
   ```bash
   ctrl + b -> :source-file ~/.tmux.conf
   ```

---

### Tips dan Best Practices
1. **Gunakan Plugin untuk Menambah Fitur**:
   - **Tmux Plugin Manager (TPM)**: Mempermudah instalasi dan manajemen plugin.
     ```bash
     git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
     ```
     Tambahkan konfigurasi berikut di `.tmux.conf`:
     ```bash
     # Tmux Plugin Manager
     set -g @plugin 'tmux-plugins/tpm'
     run '~/.tmux/plugins/tpm/tpm'
     ```
   - Reload konfigurasi dan tekan `ctrl + b -> I` untuk menginstal plugin.

2. **Gunakan Key Bindings yang Nyaman**:
   - Ubah shortcut default sesuai preferensi untuk meningkatkan efisiensi.

3. **Integrasi SSH**:
   - Tmux sangat berguna untuk menjaga sesi remote tetap berjalan meski koneksi SSH terputus.

4. **Gunakan Layout Otomatis**:
   - Shortcut `ctrl + b -> space` membantu mengatur layout pane dengan cepat.

