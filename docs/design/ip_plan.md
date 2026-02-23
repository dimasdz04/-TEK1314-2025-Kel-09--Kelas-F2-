# IP Address & Network Plan - Kelompok 09

**Skenario Proyek:** Man-in-the-Middle Hunter
**Target Aset:** Network Switch / Gateway (Jaringan Lokal/LAN)

## 1. Skema Jaringan
Sesuai dengan Kontrak Kuliah Poin 3a, Kelompok 09 menggunakan segmen IP unik sebagai berikut:
* **Subnet Network:** `192.168.9.0/24`
* **Gateway Router:** `192.168.9.1`

## 2. Tabel Inventaris Asset & IP
Berikut adalah daftar Node yang direncanakan untuk simulasi proyek ini:

| Hostname | Sistem Operasi (OS) | IP Address | Peran / Deskripsi |
| :--- | :--- | :--- | :--- |
| **Attacker-Node** | Kali Linux | `192.168.9.100` | Penyerang (Menjalankan Ettercap/Bettercap) |
| **Victim-Client** | Windows 10/11 Endpoint | `192.168.9.50` | Korban 1 (User PC yang melakukan login) |
| **Victim-Server** | Ubuntu Server CLI | `192.168.9.10` | Korban 2 (Target Web/FTP Server Lokal) |
| **Monitor-Node** | Security Onion | `192.168.9.200` | IDS & Monitoring Log Jaringan |

*Catatan: Ubuntu Server CLI dipilih karena ringan untuk mengantisipasi keterbatasan RAM laptop.*

## 3. Analisis Port Terbuka (Security Analyst)
Untuk mendukung skenario penyadapan komunikasi data (username/password) antar komputer korban, port berikut perlu dibuka pada Victim-Server:
* **Port 80 (HTTP):** Untuk simulasi login web *plain-text* (tidak terenkripsi).
* **Port 21 (FTP):** Untuk simulasi transfer file.
* **Port 22 (SSH):** Untuk akses manajemen *remote* server oleh tim engineer.