# 🚀 CEH Practical Exam Preparation  
**Repositori ini mengandungi sumber pembelajaran, rujukan utama, latihan, dan persediaan untuk peperiksaan amali CEH (Certified Ethical Hacker Practical).**  

---

## 📌 Kandungan  
- [📚 Rujukan Utama](#-rujukan-utama)  
- [🛠️ Tool yang Perlu Dikuasai](#️-tool-yang-perlu-dikuasai)  
- [💡 Tips & Trick untuk Exam CEH Amali](#-tips--trick-untuk-exam-ceh-amali)  
- [🖥️ Latihan Hands-on & Platform Belajar](#️-latihan-hands-on--platform-belajar)  

---

## 📚 Rujukan Utama  
Berikut adalah sumber utama untuk pembelajaran dan latihan CEH:  

### 📖 **Buku Rujukan**  
- **[CEH v12 Certified Ethical Hacker Study Guide – Ric Messier](https://www.amazon.com/CEH-Certified-Ethical-Hacker-Study/dp/1119805269/)**  
- **[Certified Ethical Hacker (CEH) All-in-One Exam Guide – Matt Walker](https://www.amazon.com/CEH-Certified-Ethical-Hacker-Guide/dp/126045455X/)**  

### 🎥 **Kursus Video**  
- **[INE – CEH Practical Course](https://ine.com/learning/certifications/ec-council/ceh-certified-ethical-hacker)**  
- **[Udemy – Certified Ethical Hacker Bootcamp](https://www.udemy.com/course/certified-ethical-hacker-bootcamp/)**  
- **[Pluralsight – CEH Practical Exam Preparation](https://www.pluralsight.com/courses/ceh-certified-ethical-hacker-practical-exam-preparation)**  

### 📝 **Soalan Latihan & Simulasi Peperiksaan**  
- **[Boson CEH Practice Exams](https://www.boson.com/practice-exam/ceh)**  
- **[ExamTopics CEH Questions](https://www.examtopics.com/exams/ec-council/ceh/)**  
- **[Skillset CEH Practice Tests](https://www.skillset.com/certifications/certified-ethical-hacker)**  

---

## 🛠️ Tool yang Perlu Dikuasai  
Peperiksaan CEH memerlukan kemahiran dalam pelbagai tool pentesting. Berikut adalah senarai utama:  

### **📌 Footprinting & Reconnaissance**  
- **Nmap** – Network scanning & reconnaissance  
- **theHarvester** – OSINT untuk e-mel, domain & subdomain  
- **Maltego** – OSINT & analisis hubungan  

### **📌 Scanning & Enumeration**  
- **Nmap & Netcat** – Network scanning & service enumeration  
- **Gobuster / Dirb** – Web directory bruteforcing  
- **SNMP Enumeration (snmpwalk, onesixtyone)** – SNMP enumeration  

### **📌 Exploitation & Privilege Escalation**  
- **Metasploit** – Framework untuk eksploitasi sistem  
- **Mimikatz** – Dump password & credential dalam Windows  
- **PowerSploit / Windows Exploit Suggester** – Privilege escalation dalam Windows  
- **LinPEAS / Linux Exploit Suggester** – Privilege escalation dalam Linux  

### **📌 Password Cracking & Credential Attacks**  
- **John the Ripper & Hashcat** – Password cracking  
- **Hydra** – Bruteforce login untuk SSH, FTP, RDP, dan lain-lain  
- **Responder** – Menangkap NTLMv2 hash untuk serangan pass-the-hash  

### **📌 Wireless & Web Application Security**  
- **Aircrack-ng & Wireshark** – Wireless network pentesting  
- **Burp Suite** – Web application security testing  
- **SQLmap** – SQL Injection automation  

---

## 💡 Tips & Trick untuk Exam CEH Amali  
✅ **1. Latihan Hands-on adalah Kunci**  
- Gunakan platform seperti **TryHackMe, Hack The Box, dan EC-Council iLabs**.  
- Amalkan pentesting dalam **Kali Linux** dengan mesin virtual.  

✅ **2. Kuasai Teknik Footprinting & Scanning**  
- Gunakan **Google Dorking** dan **OSINT tools** untuk mengumpul maklumat.  
- Mahirkan penggunaan **Nmap, Netcat, dan enumeration tools**.  

✅ **3. Hafal Sintaks Perintah Penting**  
- `nmap -A -p- <target>` – Advanced scanning  
- `nc -lvnp <port>` – Netcat listener untuk reverse shell  
- `sqlmap -u "http://target.com/page.php?id=1" --dbs` – SQL Injection  

✅ **4. Biasakan Diri dengan Exploit Frameworks**  
- **Metasploit** (`msfconsole, search, use, exploit`)  
- **Mimikatz** (`sekurlsa::logonpasswords`)  
- **Privilege Escalation Scripts** (`linpeas.sh, winPEAS.exe`)  

✅ **5. Fahami Web & Wireless Attacks**  
- **Burp Suite** → Ujian serangan XSS, SQLi, CSRF.  
- **Aircrack-ng** → Crack Wi-Fi WPA2 dengan `airmon-ng, airodump-ng, aircrack-ng`.  

✅ **6. Guna Notes dan Cheat Sheets**  
- **[Pentestmonkey Reverse Shell Cheat Sheet](http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet)**  
- **[GTFOBins](https://gtfobins.github.io/)** untuk Linux privilege escalation  

---

## 🖥️ Latihan Hands-on & Platform Belajar  
🔹 **[TryHackMe – CEH Pathway](https://tryhackme.com/)** – Hands-on lab dengan modul CEH.  
🔹 **[Hack The Box (HTB)](https://www.hackthebox.com/)** – Mesin real-world untuk latihan pentesting.  
🔹 **[EC-Council iLabs](https://iclass.eccouncil.org/)** – Makmal rasmi untuk latihan CEH.  
🔹 **[RangeForce Cyber Range](https://www.rangeforce.com/)** – Latihan simulasi keselamatan siber.  

---

## 📢 Penyertaan & Sumbangan  
- **Pull Request** dialu-alukan! Jika ada sumber baru, sila tambahkan.  
- **Isu & cadangan** boleh dibuka di [Issues](https://github.com/your-repo/issues).  
- Sertai **komuniti cybersecurity** di Discord & Reddit untuk perbincangan lanjut.  

---

## 📜 Penafian  
🚨 **Repositori ini hanya bertujuan untuk pembelajaran dan latihan keselamatan siber secara sah. Sebarang penyalahgunaan maklumat adalah tanggungjawab individu. Gunakan dengan etika dan mematuhi undang-undang setempat.** 🚨  

---

📌 **Repo ini dikemaskini dari semasa ke semasa. Selamat belajar dan semoga berjaya dalam peperiksaan CEH amali!** 🚀
