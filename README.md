# -TEK1314-2025-Kel-09-Kelas-F2-


# Logbook Proyek PBL Keamanan Siber – TEK1314

## Informasi Umum
- Kelompok : 09
- Kelas    : TEK-F
- Tahun    : 2025/2026
- Skenario : Man-in-theMiddle Hunter

## Anggota & Peran
1. Dimas Dzikra Pratama – J0404231126  
   **Peran:** Lead Analyst  
   **Tugas:** Koordinasi tim, dokumentasi GitHub, konsolidasi laporan

2. Arif Sanda Wijaksana – NIM  (MAGANG)
   **Peran:** System / Network Engineer  
   **Tugas:** Instalasi VM CyberOps & Security Onion

4. Muhammad Aqil Fazli – NIM  
   **Peran:** Network Engineer  
   **Tugas:**  Fokus pada setup VM dan konfigurasi jaringan di Packet Tracer.
   
5. Fatimah Az-Zahidah
   **Peran:** Security Analyst  
   **Tugas:** Analisis teknis & log 

---

## Update Minggu 2 – Inisialisasi Proyek
- Pembagian peran tim telah ditetapkan.
- Repository GitHub kelompok berhasil dibuat dan dapat diakses dosen/asisten.
- Instalasi VM dilakukan **hanya pada 2 laptop** sesuai instruksi:
  - 1 Laptop Utama (Laptop Arif)
  - 1 Laptop Backup (Laptop Dimas)
- Status instalasi VM:
  - CyberOps Workstation : Installed
  - Security Onion       : Installed
- Topologi jaringan **belum dibuat** sesuai ketentuan Minggu 2.

**Status Proyek:** On Progress

---

## Update Minggu 3 – Fase Setup (Design Phase)
**Target:** Perancangan Arsitektur & Skema IP

- Telah merancang **Topologi Logis (Network Diagram)** yang memuat 3 entitas utama: Attacker Node (Kali Linux), Target Node (Ubuntu Server CLI), Web Server (Ubuntu Server CLI), dan Monitoring Node (Security Onion).
- Telah menyusun **Skema IP Address (IP Plan)** menggunakan subnet unik kelompok yaitu `192.168.9.0/24`.
- Melakukan **Survey Spesifikasi Target**, dan memutuskan menggunakan Ubuntu Server CLI untuk mengantisipasi keterbatasan RAM laptop saat menjalankan Security Onion.
- Telah menentukan daftar port yang perlu dibuka untuk simulasi penyadapan pada Victim-Server (Port 80 HTTP, Port 21 FTP, Port 22 SSH).

**Artefak Dokumen Minggu 3:**
- [Gambar Topologi Jaringan](docs/design/Network-Topology.png)
- [Tabel IP Plan & Analisis Port](docs/design/ip_plan.md)

---

## Update Minggu 4-7 – Fase Hardening & Baseline (Fase 1)
**Target:** Penguatan OS (Target Node) & Dokumentasi Logging Check (Monitoring Node).

- **[Konfigurasi Identitas]** Mengatur *hostname* pada Victim-Server menjadi `SRV-WEB-KEL09` dengan alokasi IP statis `192.168.9.10`.
- **[Network Hardening]** Mengonfigurasi dan mengaktifkan UFW Firewall di Ubuntu Server dengan aturan *Default Deny incoming* dan hanya mengizinkan *port* esensial (Port 22 SSH) terbuka.
- **[MITM Hardening]** Melakukan mitigasi awal terhadap ancaman Man-in-the-Middle (ARP Spoofing) dengan mendaftarkan MAC Address Gateway secara statis (Static ARP Entry status `PERM`) pada server target.
- **[Logging Check - Skenario Plan B]** Mengingat keterbatasan alokasi memori (RAM) pada VM yang menyebabkan service Sguil/Squert di Security Onion tidak stabil, kelompok mengeksekusi *Skenario Cadangan (Plan B)* sesuai Poin 9 pada pedoman PBL. Pembuktian kapabilitas monitoring jaringan dilakukan dengan metode *Manual Analysis*:
  - **Analisis PCAP:** Menggunakan Wireshark di Security Onion untuk menyadap dan merekam trafik ICMP (Ping) secara *real-time* dari Attacker (`192.168.9.100`) ke Target (`192.168.9.10`).
  - **Log File Manual:** Merekam percobaan akses tidak sah (*SSH failed login*) dari Attacker di dalam file log sistem operasi target (`/var/log/auth.log`).

**Artefak Dokumen Minggu 4-7:**
- [Laporan Baseline & Hardening Lengkap](docs/phase-1-baseline/baseline-report.md)
- [Bukti Hardening UFW (Firewall)](docs/phase-1-baseline/assets/bukti-hardening-ufw.png)
- [Bukti Hardening ARP (Anti-MITM)](docs/phase-1-baseline/assets/bukti-hardening-arp.png)
- [Bukti Logging PCAP (Wireshark)](docs/phase-1-baseline/assets/bukti-logging-wireshark.png)
- [Bukti Log Manual (auth.log)](docs/phase-1-baseline/assets/bukti-log-manual.png)


**Status Proyek:** On Progress

---
## Catatan
Dokumentasi teknis lanjutan, Vulnerability Assessment (Fase 2), dan simulasi serangan MITM serta Incident Response (Fase 3) akan dilakukan pada minggu berikutnya sesuai roadmap PBL.
