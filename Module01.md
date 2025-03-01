# Module 01: Introduction to Ethical Hacking - Summary

## 1. Pengenalan kepada Ethical Hacking
Ethical hacking adalah proses menilai sistem dan rangkaian untuk mengenal pasti kelemahan yang boleh dieksploitasi oleh penyerang. Ethical hacker bertindak sebagai "white hat" hackers yang menjalankan ujian keselamatan dengan kebenaran organisasi untuk memperbaiki pertahanan siber mereka.

## 2. Jenis-jenis Hacker
- **White Hat Hackers** – Penggodam etika yang bekerja untuk mengukuhkan keselamatan sistem.
- **Black Hat Hackers** – Penyerang yang berniat jahat, mencuri data atau merosakkan sistem.
- **Grey Hat Hackers** – Penggodam yang berada di antara dua kategori; kadang-kadang melanggar undang-undang tetapi tidak mempunyai niat jahat.
- **Script Kiddies** – Individu yang tidak mempunyai kemahiran teknikal mendalam tetapi menggunakan skrip dan alat orang lain untuk menyerang sistem.
- **State-Sponsored Hackers** – Penggodam yang bekerja untuk kerajaan untuk tujuan perisikan atau peperangan siber.

## 3. Elemen Penting dalam Ethical Hacking
- **Confidentiality** – Menjaga kerahsiaan data.
- **Integrity** – Memastikan data tidak diubah tanpa kebenaran.
- **Availability** – Memastikan sistem dan data boleh diakses oleh pengguna yang dibenarkan.

## 4. Fasa dalam Proses Ethical Hacking
1. **Reconnaissance (Footprinting)** – Mengumpulkan maklumat mengenai sasaran.
2. **Scanning** – Mengenal pasti port terbuka, perkhidmatan yang berjalan, dan kelemahan.
3. **Gaining Access** – Mengeksploitasi kelemahan untuk mendapatkan kawalan sistem.
4. **Maintaining Access** – Menyediakan pintu belakang untuk akses berterusan.
5. **Covering Tracks** – Memadam jejak aktiviti untuk mengelakkan dikesan.

## 5. Perundangan dan Standard Etika
- **Computer Fraud and Abuse Act (CFAA)** – Undang-undang berkaitan jenayah siber di Amerika Syarikat.
- **General Data Protection Regulation (GDPR)** – Peraturan perlindungan data peribadi di Eropah.
- **Ethical Hacking Code of Conduct** – Standard etika yang dipatuhi oleh penggodam beretika.

## 6. Alat dan Teknik Ethical Hacking
- **Nmap** – Digunakan untuk network scanning.
- **Wireshark** – Digunakan untuk packet analysis.
- **Metasploit** – Platform eksploitasi yang membantu dalam penetration testing.
- **Burp Suite** – Digunakan untuk ujian keselamatan aplikasi web.

## 7. Peranan Ethical Hacker dalam Keselamatan Siber
Ethical hacker membantu organisasi:
- Mengenal pasti dan membetulkan kelemahan sebelum penyerang mengeksploitasinya.
- Mengukuhkan dasar keselamatan.
- Melakukan ujian penembusan secara berkala.
- Melatih pengguna tentang amalan keselamatan terbaik.

## 8. Cabaran dalam Ethical Hacking
- **Kelulusan dan Perundangan** – Memerlukan kebenaran sebelum menjalankan ujian.
- **Evolusi Ancaman Siber** – Ancaman baru sentiasa muncul dan berkembang.
- **Etika dan Tanggungjawab** – Menjalankan ujian dengan penuh integriti tanpa merosakkan sistem.

## 9. Kesimpulan
Ethical hacking memainkan peranan penting dalam dunia keselamatan siber. Dengan memahami prinsip dan teknik ethical hacking, organisasi dapat melindungi sistem mereka daripada serangan siber dan mengurangkan risiko kebocoran data.

---

Ringkasan ini memberikan gambaran keseluruhan tentang konsep asas ethical hacking. Untuk pemahaman yang lebih mendalam, pelajari modul sepenuhnya dan lakukan latihan praktikal yang disediakan!

Dalam **cybersecurity**, konsep **Red Team** dan **Blue Team** digunakan untuk menilai tahap keselamatan sesuatu organisasi melalui ujian serangan dan pertahanan. Ini adalah pendekatan yang sering digunakan dalam **penetration testing**, **incident response**, dan **cybersecurity assessments**.

---

### **🛡️ Blue Team (Pasukan Pertahanan)**
✅ **Peranan:**  
- Bertanggungjawab melindungi sistem, rangkaian, dan data organisasi daripada serangan siber.  
- Menggunakan pelbagai alat keselamatan untuk memantau, mengesan, dan bertindak balas terhadap ancaman.  
- Memastikan dasar keselamatan dipatuhi, menjalankan **patch management**, dan menguatkuasakan **access control**.

✅ **Tugas Utama:**  
- **Monitoring & Detection:** Menggunakan SIEM (Security Information and Event Management) untuk memantau aktiviti yang mencurigakan.  
- **Incident Response:** Bertindak balas terhadap insiden keselamatan dan mengurangkan kesan serangan.  
- **Threat Hunting:** Mencari ancaman yang mungkin belum dikenal pasti oleh sistem automatik.  
- **Security Hardening:** Mengukuhkan sistem dengan firewall, antivirus, IDS/IPS (Intrusion Detection/Prevention Systems).  
- **Training & Awareness:** Melatih pekerja tentang keselamatan siber untuk mengurangkan risiko **social engineering**.  

✅ **Alatan yang Digunakan oleh Blue Team:**  
- **SIEM (Splunk, ELK, QRadar, ArcSight)** → Untuk pemantauan log dan analisis ancaman.  
- **IDS/IPS (Snort, Suricata, Zeek)** → Untuk mengesan dan mencegah serangan rangkaian.  
- **EDR (CrowdStrike, SentinelOne, Microsoft Defender ATP)** → Untuk memantau endpoint devices.  
- **Firewall & WAF (Palo Alto, Fortinet, Cloudflare)** → Untuk menapis trafik berbahaya.  

---

### **🚨 Red Team (Pasukan Serangan)**
✅ **Peranan:**  
- Bertindak sebagai **penyerang** yang mensimulasikan serangan siber sebenar terhadap sistem organisasi.  
- Mencari kelemahan dalam sistem, aplikasi, dan infrastruktur.  
- Ujian ini dilakukan secara **ethical hacking**, bertujuan untuk meningkatkan keselamatan, bukan untuk memusnahkan.  

✅ **Tugas Utama:**  
- **Penetration Testing:** Menjalankan ujian serangan terhadap sistem, rangkaian, dan aplikasi.  
- **Social Engineering Attacks:** Menguji pekerja dengan simulasi serangan **phishing, baiting, pretexting**.  
- **Physical Security Testing:** Ujian keselamatan fizikal seperti cuba memasuki premis tanpa kebenaran.  
- **Exploitation & Post-Exploitation:** Menggunakan kelemahan untuk mendapatkan akses dan meningkatkan keistimewaan (privilege escalation).  

✅ **Alatan yang Digunakan oleh Red Team:**  
- **Reconnaissance (OSINT Framework, Maltego, theHarvester)** → Mengumpul maklumat awal.  
- **Exploitation (Metasploit, Cobalt Strike, Empire, Mimikatz)** → Mengeksploitasi kelemahan dalam sistem.  
- **Password Cracking (John the Ripper, Hashcat, Hydra)** → Meneka atau menyahsulit kata laluan.  
- **Wireless Attacks (Aircrack-ng, Wireshark, Kismet)** → Menganalisis dan menyerang rangkaian tanpa wayar.  
- **Social Engineering (Gophish, SET - Social Engineering Toolkit)** → Untuk ujian serangan phishing.  

---

### **🟣 Purple Team (Gabungan Red & Blue Team)**
✅ **Peranan:**  
- Bukan satu pasukan tetap, tetapi konsep **kerjasama** antara Red Team & Blue Team.  
- Red Team cuba menembusi sistem, Blue Team cuba mempertahankan, dan kedua-duanya belajar dari hasil ujian ini.  
- Tujuan utama adalah **continuous improvement** terhadap keselamatan organisasi.  

✅ **Bagaimana Purple Team Berfungsi?**  
1. **Red Team menyerang** → Cari kelemahan dan exploit sistem.  
2. **Blue Team bertahan** → Memantau dan bertindak balas terhadap serangan.  
3. **Evaluasi bersama** → Mengenal pasti kelemahan dan mencari penyelesaian yang lebih baik.  
4. **Menambah baik strategi keselamatan** → Blue Team meningkatkan pertahanan berdasarkan taktik Red Team.  

---

### **Perbandingan Red Team vs Blue Team**
| **Kategori**     | **Red Team (Penyerang)** | **Blue Team (Pertahanan)** |
|----------------|----------------|----------------|
| **Fokus** | Menyerang dan mencari kelemahan | Melindungi sistem dan mengesan serangan |
| **Pendekatan** | Ethical hacking & penetration testing | Defensive security & monitoring |
| **Alatan** | Metasploit, Cobalt Strike, Hydra | SIEM, IDS/IPS, Firewalls, EDR |
| **Matlamat** | Uji sistem dan cari kelemahan | Lindungi dan tingkatkan keselamatan |
| **Metodologi** | Simulasi serangan dunia sebenar | Mengesan, bertindak balas, dan membetulkan kelemahan |

---

### **Kesimpulan**
- **Red Team** = Cari kelemahan  
- **Blue Team** = Pertahan organisasi  
- **Purple Team** = Gabungan Red & Blue untuk tingkatkan keselamatan secara berterusan  

Untuk seorang **ethical hacker atau penetration tester**, memahami kedua-dua peranan ini sangat penting, terutama dalam peperiksaan **CEH** dan amalan sebenar dalam dunia cybersecurity.