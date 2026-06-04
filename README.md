# 🛡️ Wazuh Endpoint Attack Simulation

## MK2-B PAS | XI TJKT 2 | Kelompok 7

**SMK Telkom Purwokerto**  
**Teknik Jaringan Komputer dan Telekomunikasi**

---

## 📖 Gambaran Project

Repository ini berisi dokumentasi modul simulasi serangan terhadap endpoint Ubuntu Server yang telah dipantau menggunakan Wazuh Agent.

Simulasi dilakukan dari sisi attacker menggunakan Kali Linux. Aktivitas yang dilakukan meliputi validasi jaringan, reconnaissance, pengujian akses service, serta simulasi serangan terhadap beberapa layanan seperti FTP, SSH, SMB, dan Apache2.

Project ini dibuat untuk kebutuhan pembelajaran keamanan jaringan, khususnya dalam memahami bagaimana aktivitas attacker dapat menghasilkan event keamanan yang nantinya dianalisis oleh tim defender melalui Wazuh SIEM.

---

## 🎯 Tujuan Praktikum

Tujuan dari praktikum ini adalah:

- Memahami tahapan dasar reconnaissance pada jaringan lab
- Mengidentifikasi service aktif pada endpoint target
- Melakukan simulasi aktivitas attacker terhadap FTP, SSH, SMB, dan Apache2
- Menghasilkan log atau event keamanan pada endpoint
- Menjadi bahan analisis bagi tim defender menggunakan Wazuh

---

## 🧪 Skenario Pengujian

| No | Aktivitas | Tool yang Digunakan | Target | Port |
|---|---|---|---|---|
| 1 | Validasi IP attacker | `ip` | Kali Linux | - |
| 2 | Scanning service target | `nmap` | FTP, SSH, SMB, Apache2 | 21, 22, 80, 139, 445 |
| 3 | Pengujian akses web server | Browser, `curl` | Apache2 | 80 |
| 4 | Directory enumeration | `gobuster` | Apache2 | 80 |
| 5 | Anonymous login FTP | `ftp` | FTP Server / vsftpd | 21 |
| 6 | Upload file ke FTP | `ftp` | FTP Server | 21 |
| 7 | Percobaan login SSH gagal | `ssh` | OpenSSH | 22 |
| 8 | Enumerasi SMB share | `smbclient` | Samba / SMB | 139, 445 |
| 9 | Upload file ke SMB public share | `smbclient` | SMB Share | 139, 445 |

---

## 🏗️ Environment Lab

| Komponen | Keterangan |
|---|---|
| Attacker Machine | Kali Linux |
| Target Server | Ubuntu Server |
| Monitoring Agent | Wazuh Agent pada endpoint target |
| SIEM Server | Wazuh Server / Wazuh Manager |
| Layanan Target | Apache2, FTP, SSH, SMB |

---

## 🌐 Alamat IP Lab

| Perangkat | IP Address | Peran |
|---|---|---|
| Kali Linux | 175.17.0.247 | Attacker |
| Ubuntu Agent | 175.17.0.127 | Endpoint target |
| Wazuh Server | 175.17.0.234 | Server monitoring |

> Catatan: Seluruh IP address hanya digunakan pada jaringan lab internal dan tidak berlaku untuk jaringan publik.

---

## 👥 Anggota Kelompok 7

| No | Nama | Nomor Absen |
|---|---|---|
| 1 | Satria Fadhil Yaslam | 23 |
| 2 | Satria Mahendra Kusuma | 24 |
| 3 | Aisya Luthfiana Bilqis Azizah | 2 |
| 4 | Wahid Nur Rohman | 28 |

---

## 🎓 Informasi Akademik

| Keterangan | Detail |
|---|---|
| Sekolah | SMK Telkom Purwokerto |
| Jurusan | Teknik Jaringan Komputer dan Telekomunikasi |
| Mata Pelajaran | MK2-B / Cyber Security |
| Jenis Penilaian | PAS - Penilaian Akhir Semester |
| Kelas | XI TJKT 2 |
| Kelompok | Kelompok 7 |
| Tahun Ajaran | 2025/2026 |

---

## 🧰 Tools yang Digunakan

| Tool | Fungsi |
|---|---|
| `ip` | Mengecek dan memvalidasi alamat IP pada mesin attacker |
| `nmap` | Melakukan scanning port dan identifikasi service target |
| Browser | Mengakses halaman web Apache2 |
| `curl` | Mengecek respons HTTP dari web server |
| `gobuster` | Melakukan directory enumeration pada Apache2 |
| `ftp` | Melakukan login FTP dan upload file |
| `ssh` | Melakukan percobaan login SSH |
| `smbclient` | Melakukan enumerasi dan akses SMB share |
| Wazuh | Monitoring endpoint dan analisis aktivitas keamanan |

---

## 📂 Isi Repository

```text
wazuh-siem-attack-detection-lab/
├── README.md
└── Modul_Attacker_Wazuh_SIEM_Kelompok_7.pdf
```

---

## 📌 Ringkasan Hasil Simulasi

| Service | Hasil Pengujian |
|---|---|
| Apache2 | Web server dapat diakses dan memberikan respons HTTP 200 OK |
| Apache2 Directory | Directory enumeration menghasilkan beberapa path dengan status tertentu |
| FTP | Anonymous login berhasil dilakukan |
| FTP Upload | File berhasil diunggah ke direktori upload |
| SSH | Percobaan login dengan user umum menghasilkan permission denied |
| SMB | Share public ditemukan melalui enumerasi |
| SMB Upload | File berhasil diunggah ke share public |

---

## 📄 File Modul

Dokumen modul praktikum tersedia pada repository ini:

- `Modul_Attacker_Wazuh_SIEM_Kelompok_7.pdf`

---

## ✅ Kesimpulan

Berdasarkan simulasi yang dilakukan, endpoint target berhasil menghasilkan berbagai aktivitas yang dapat dianalisis dari sisi keamanan. Aktivitas tersebut meliputi scanning service, akses web server, directory enumeration, FTP anonymous login, upload file, failed login SSH, serta akses SMB public share.

Simulasi ini membantu memahami hubungan antara aktivitas attacker dan proses monitoring keamanan menggunakan Wazuh SIEM.

---

## ⚠️ Disclaimer

Seluruh aktivitas dalam modul ini hanya dilakukan untuk keperluan pembelajaran di environment lab yang terisolasi. Penggunaan teknik serupa terhadap sistem tanpa izin merupakan tindakan ilegal.
