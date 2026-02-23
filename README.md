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

- Telah merancang **Topologi Logis (Network Diagram)** yang memuat 3 entitas utama: Attacker Node (Kali Linux), Target Node (Windows 10/11 & Ubuntu Server CLI), dan Monitoring Node (Security Onion).
- Telah menyusun **Skema IP Address (IP Plan)** menggunakan subnet unik kelompok yaitu `192.168.9.0/24`.
- Melakukan **Survey Spesifikasi Target**, dan memutuskan menggunakan Ubuntu Server CLI dan Windows 10/11 Endpoint untuk mengantisipasi keterbatasan RAM laptop saat menjalankan Security Onion.
- Telah menentukan daftar port yang perlu dibuka untuk simulasi penyadapan pada Victim-Server (Port 80 HTTP, Port 21 FTP, Port 22 SSH).

**Artefak Dokumen Minggu 3:**
- [Gambar Topologi Jaringan](docs/design/Network-Popology.png)
- [Tabel IP Plan & Analisis Port](docs/design/ip_plan.md)

**Status Proyek:** On Progress

---
## Catatan
Dokumentasi teknis lanjutan, instalasi OS target (Fase Hardening), dan simulasi serangan akan dilakukan pada minggu berikutnya sesuai roadmap PBL.
