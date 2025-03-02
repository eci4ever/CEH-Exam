## **Modul 3: Scanning Networks - CEH**  

### **Pengenalan kepada Scanning Networks**  
**Scanning Networks** ialah fasa kedua dalam **Ethical Hacking Lifecycle**, selepas **Reconnaissance**. Dalam fasa ini, seorang ethical hacker atau penetration tester akan mengimbas rangkaian sasaran untuk mendapatkan maklumat lanjut tentang **active hosts, open ports, services, operating systems (OS), dan vulnerabilities**.  

Proses ini penting kerana ia membantu:  
- Mengenal pasti **live hosts** dalam rangkaian.  
- Mengenal pasti **open ports** dan perkhidmatan yang berjalan.  
- Mendapatkan **OS fingerprinting** untuk menentukan jenis sistem operasi sasaran.  
- Melakukan **banner grabbing** untuk mendapatkan maklumat lanjut mengenai perkhidmatan dan versi software.  
- Mengenal pasti **vulnerabilities** dalam rangkaian.  

---

## **1. Teknik Scanning Networks**  
Terdapat pelbagai teknik yang digunakan untuk mengimbas rangkaian, antaranya:  

### **a) Ping Sweep (ICMP Scanning)**  
- Digunakan untuk mengenal pasti **live hosts** dalam satu subnet.  
- Menghantar **ICMP Echo Request** kepada setiap IP dalam rangkaian dan menunggu **ICMP Echo Reply**.  
- Firewall dan IDS/IPS sering menyekat ICMP untuk mengelakkan pengimbasan ini.  

### **b) Port Scanning**  
- Mengimbas **open ports** dalam sistem untuk menentukan perkhidmatan yang sedang berjalan.  
- **Jenis Port Scanning:**  
  - **TCP Full Connect Scan** (Port **status: Open, Closed, Filtered**)  
  - **TCP SYN Scan (Half-Open Scan)** (Menghantar SYN tanpa melengkapkan **3-way handshake**)  
  - **TCP Stealth Scan** (Menggunakan fragmented packets untuk mengelak dikesan)  
  - **UDP Scan** (Mengimbas **UDP ports**, tetapi lebih perlahan kerana tiada handshake)  

### **c) OS Fingerprinting**  
- Digunakan untuk mengenal pasti **Operating System (OS)** yang digunakan oleh sasaran.  
- Teknik ini berdasarkan response unik daripada paket TCP/IP.  
- **Active OS Fingerprinting**: Menghantar paket khas untuk mendapatkan tindak balas OS.  
- **Passive OS Fingerprinting**: Mengumpul maklumat daripada lalu lintas rangkaian tanpa menghantar paket khas.  

### **d) Banner Grabbing**  
- Digunakan untuk mendapatkan maklumat lanjut tentang **services, versions, dan OS** yang sedang berjalan di sasaran.  
- Contoh tools:  
  - **Telnet** (`telnet [IP] [port]`)  
  - **Netcat** (`nc -v [IP] [port]`)  
  - **Nmap** (`nmap -sV [IP]`)  

### **e) Firewalking**  
- Digunakan untuk mengesan **firewall rules** dengan menghantar paket TTL yang diubah suai.  
- Membantu mengenal pasti **open dan closed ports** di sebalik firewall.  

---

## **2. Scanning Tools dalam CEH**  
### **a) Nmap (Network Mapper)**  
- **Tool paling popular** untuk network scanning.  
- Boleh digunakan untuk **ping sweep, port scanning, OS fingerprinting, dan vulnerability scanning**.  
- **Contoh command:**  
  - `nmap -sS [IP]` (SYN Scan)  
  - `nmap -sV [IP]` (Service Version Scan)  
  - `nmap -O [IP]` (OS Detection)  

### **b) Hping3**  
- Tool untuk **packet crafting** dan **custom scanning**.  
- Boleh digunakan untuk **DoS testing, firewall testing, dan OS fingerprinting**.  

### **c) Netcat (NC)**  
- Digunakan untuk **port scanning, banner grabbing, dan troubleshooting rangkaian**.  
- Contoh: `nc -v [IP] [port]`  

### **d) Zenmap**  
- **GUI version of Nmap**, lebih user-friendly.  

### **e) Angry IP Scanner**  
- Lightweight tool untuk **fast network scanning**.  

### **f) Nessus/OpenVAS**  
- Automated vulnerability scanners.  
- Membantu mengenal pasti **security weaknesses** berdasarkan database vulnerabilities.  

---

## **3. Cara Mengesan dan Mencegah Scanning Attacks**  
Scanning networks boleh digunakan oleh **ethical hackers** dan **malicious attackers**. Oleh itu, penting untuk mengetahui bagaimana mengesan dan mencegah aktiviti ini.  

### **a) Intrusion Detection/Prevention Systems (IDS/IPS)**  
- Mengesan dan menyekat **unusual scanning patterns** dalam rangkaian.  

### **b) Firewall Rules**  
- Menyekat **unauthorized scanning attempts** dengan membenarkan hanya port tertentu.  

### **c) Network Traffic Analysis**  
- Menggunakan tools seperti **Wireshark** untuk mengenal pasti scanning activities.  

### **d) Honeypots**  
- Fake systems yang direka untuk **menarik attackers** dan merekod scanning activities mereka.  

### **e) Rate Limiting & Packet Filtering**  
- Mengurangkan impak **aggressive scanning** dengan menghadkan jumlah permintaan dalam satu masa.  

---

## **Kesimpulan**  
**Scanning Networks** adalah fasa kritikal dalam **penetration testing dan cybersecurity defense**. Ethical hackers perlu memahami teknik scanning yang digunakan untuk **mengumpul maklumat sasaran**, manakala security professionals perlu mengimplementasikan langkah-langkah keselamatan untuk **mengesan dan mencegah scanning attacks**.  

Berikut adalah ringkasan untuk **Modul 3: Scanning Networks** dalam CEH:  

---

## **Modul 3: Scanning Networks**  

### **Pengenalan**  
Selepas fasa **Reconnaissance**, ethical hacker atau penetration tester (pen tester) akan meneruskan ke fasa **Scanning Networks**. Dalam fasa ini, mereka akan melakukan **network scanning** dan **port scanning** untuk mengenal pasti **live hosts, open ports, services, dan vulnerabilities** dalam sistem sasaran.  

Walaupun **scanning bukan serangan langsung**, ia membolehkan pen tester mendapatkan gambaran menyeluruh mengenai sasaran dan menentukan vektor serangan yang sesuai.  

---

## **Objektif Scanning Networks**  
Tujuan utama dalam fasa ini adalah:  
✅ Mengenal pasti **sistem aktif (live hosts) dan open ports**  
✅ Mengenal pasti **perkhidmatan yang berjalan dalam sistem aktif**  
✅ Melakukan **banner grabbing/OS fingerprinting**  
✅ Mengenal pasti **vulnerabilities dalam rangkaian**  

---

## **Jenis-Jenis Scanning**  
1️⃣ **Port Scanning** – Mengenal pasti **open ports dan perkhidmatan** yang berjalan.  
2️⃣ **Network Scanning** – Mengenal pasti **host aktif** dan **alamat IP dalam rangkaian**.  
3️⃣ **Vulnerability Scanning** – Mengesan **kelemahan keselamatan yang diketahui** dalam rangkaian.  

---

## **Teknik & Alat dalam Scanning Networks**  
Ethical hackers menggunakan pelbagai teknik dan alat untuk melakukan scanning:  

### **🔍 1. Host Discovery (Ping Sweep)**
✔ Gunakan **Nmap** untuk mengenal pasti **sistem aktif dalam rangkaian**.  
✔ Contoh perintah:  
```bash
nmap -sn [IP Range]
```

### **🔍 2. Port & Service Discovery**
✔ Menggunakan **Nmap** untuk mengenal pasti **open ports dan perkhidmatan** yang berjalan.  
✔ Contoh perintah:  
```bash
nmap -sS -p 1-1000 [IP]
```
✔ **UDP Scan** dilakukan dengan:  
```bash
nmap -sU -p 53,161 [IP]
```

### **🔍 3. OS Fingerprinting & Banner Grabbing**
✔ Gunakan **Nmap Script Engine (NSE)** untuk mengenal pasti OS sasaran.  
✔ Contoh perintah:  
```bash
nmap -O [IP]
```
✔ Untuk banner grabbing:  
```bash
nmap -sV [IP]
```

### **🔍 4. Bypass IDS/Firewall**
✔ Gunakan **teknik evasion** untuk melepasi **Intrusion Detection Systems (IDS) & firewalls**.  
✔ Contoh teknik:  
   - **Fragmented Packet Scan**:  
     ```bash
     nmap -f [IP]
     ```
   - **Decoy Scan** (Mengaburi IDS dengan alamat IP palsu):  
     ```bash
     nmap -D RND:10 [IP]
     ```

### **🔍 5. Advanced Scanning menggunakan AI**
✔ Gunakan **ShellGPT** untuk **automated footprinting & reconnaissance**.  
✔ Contoh perintah untuk mengimbas **DNS Enumeration** menggunakan AI:  
```bash
sgpt --chat footprint --shell “Install and use DNSRecon to perform DNS enumeration on www.certifiedhacker.com”
```

---

## **Kesimpulan**  
**Scanning Networks** adalah fasa kritikal dalam ethical hacking untuk mengenal pasti kelemahan sistem sebelum eksploitasi dilakukan. Dengan menguasai pelbagai teknik dan alat seperti **Nmap, Metasploit, dan AI-powered scanning**, pen tester dapat melakukan penilaian keselamatan rangkaian dengan lebih efektif.  

Berikut adalah ringkasan dan penerangan bagi **Lab 1: Perform Host Discovery** dalam Modul 3: Scanning Networks.  

---

# **Lab 1: Perform Host Discovery**  

## **Pengenalan**  
Sebagai **ethical hacker** atau **penetration tester**, adalah penting untuk mengenal pasti **sistem aktif dalam rangkaian sasaran**. Host discovery membantu menentukan **IP yang aktif** sebelum melakukan serangan atau penilaian lanjut.  

Host discovery adalah **langkah pertama** dalam **network scanning**, kerana ia **mengurangkan masa** untuk mengimbas semua port dan alamat IP.  

---

## **Teknik Host Discovery**  
Berikut adalah beberapa teknik **host discovery** yang digunakan dalam Nmap:  

### **1️⃣ ARP Ping Scan (-PR)**  
✔ Menghantar **ARP request** ke sasaran. Jika terdapat **ARP reply**, host adalah aktif.  
✔ Hanya berfungsi dalam **rangkaian tempatan (LAN)**.  
```bash
nmap -sn -PR 10.10.1.22
```

### **2️⃣ UDP Ping Scan (-PU)**  
✔ Menghantar **UDP packet** ke sasaran. Jika ada **response**, host adalah aktif.  
✔ Jika host tidak aktif, akan menerima mesej seperti **“host/network unreachable”**.  
```bash
nmap -sn -PU 10.10.1.22
```

### **3️⃣ ICMP ECHO Ping Scan (-PE)**  
✔ Menghantar **ICMP ECHO request** ke sasaran. Jika host hidup, ia akan menghantar **ICMP ECHO reply**.  
✔ Digunakan untuk mengenal pasti **peranti aktif** atau melihat jika **ICMP dibenarkan** melalui firewall.  
```bash
nmap -sn -PE 10.10.1.22
```

### **4️⃣ ICMP ECHO Ping Sweep (-PE [IP Range])**  
✔ Menghantar **ICMP ECHO request** ke julat IP tertentu.  
✔ Digunakan untuk **mencari semua host aktif dalam subnet**.  
```bash
nmap -sn -PE 10.10.1.2-23
```

### **5️⃣ ICMP Timestamp Ping Scan (-PP)**  
✔ Menghantar **ICMP timestamp request** ke sasaran.  
✔ Digunakan untuk mendapatkan **maklumat masa sebenar** dari sistem sasaran.  
```bash
nmap -sn -PP 10.10.1.22
```

---

## **Teknik Tambahan Host Discovery**  
Selain teknik di atas, terdapat beberapa lagi kaedah yang boleh digunakan:  

| Teknik | Keterangan | Perintah |
|--------|-----------|----------|
| **ICMP Address Mask Ping Scan** | Digunakan apabila **ICMP ECHO diblok** oleh firewall | `nmap -sn -PM 10.10.1.22` |
| **TCP SYN Ping Scan** | Menghantar **empty TCP SYN packet**, **ACK response** bermaksud host aktif | `nmap -sn -PS 10.10.1.22` |
| **TCP ACK Ping Scan** | Menghantar **empty TCP ACK packet**, **RST response** bermaksud host aktif | `nmap -sn -PA 10.10.1.22` |
| **IP Protocol Ping Scan** | Menghantar **probe packets dengan pelbagai IP protocols**, sebarang **response** bermaksud host aktif | `nmap -sn -PO 10.10.1.22` |

---

## **Soalan & Jawapan**  

### **Q1: Berapa bilangan host aktif dalam subnet 10.10.1.2-23?**  
**Jawapan:**  
Jalankan arahan berikut:  
```bash
nmap -sn -PE 10.10.1.2-23
```
Lihat jumlah **"Host is up"** dalam output.  

---

### **Q2: Cari IP bagi www.goodshopping.com menggunakan Nmap**  
**Jawapan:**  
Jalankan arahan berikut untuk mendapatkan IP bagi domain **www.goodshopping.com**:  
```bash
nmap -sn www.goodshopping.com
```
Atau gunakan `host` command:  
```bash
host www.goodshopping.com
```

---

## **Kesimpulan**  
- **Host Discovery** ialah langkah pertama dalam **Network Scanning**.  
- **Nmap** menyediakan pelbagai teknik untuk mengenal pasti **host aktif dalam rangkaian**.  
- Teknik seperti **ARP Ping Scan, UDP Ping Scan, dan ICMP ECHO** sangat berguna dalam penilaian keselamatan rangkaian.  

### **Ringkasan Lab 2: Perform Port and Service Discovery**  

Dalam **Lab 2**, kita meneroka pelbagai **teknik imbasan rangkaian menggunakan Nmap** untuk mengenal pasti port terbuka dan perkhidmatan yang berjalan pada hos dalam rangkaian sasaran. **Nmap** ialah alat yang digunakan secara meluas dalam **ujian penembusan (pentesting)** dan **pengauditan keselamatan** untuk mendapatkan maklumat mengenai sistem sasaran, termasuk perkhidmatan yang berjalan, versi perisian, dan tahap keselamatan yang diterapkan.  

---

## **Objektif Lab:**  
1. Menggunakan **Nmap** untuk mengimbas port dan mengenal pasti perkhidmatan yang aktif.  
2. Memahami **teknik imbasan yang berbeza** dan bagaimana ia berfungsi.  
3. Menentukan bagaimana **firewall dan sistem pertahanan rangkaian** mempengaruhi hasil imbasan.  
4. Memperoleh maklumat seperti **jenis peranti, sistem operasi (OS), dan perisian yang digunakan** dalam hos sasaran.  

---

## **Teknik Imbasan Nmap yang Digunakan:**  

### **1. TCP Connect Scan (-sT)**  
- Teknik ini menggunakan **TCP three-way handshake** untuk mengenal pasti port terbuka.  
- Prosesnya:  
  1. Klien menghantar **SYN** ke sasaran.  
  2. Sasaran membalas dengan **SYN-ACK** jika port terbuka.  
  3. Klien menghantar **ACK** untuk melengkapkan sambungan.  
  4. Jika port ditutup, sasaran menghantar **RST** sebagai respons.  
- Kelemahan: Teknik ini mudah dikesan oleh firewall dan sistem log kerana ia **melengkapkan sambungan** sebelum ditamatkan.  

### **2. Stealth Scan / Half-Open Scan (-sS)**  
- Juga dikenali sebagai **TCP SYN scan**, ia hanya menghantar **SYN packet** tanpa melengkapkan three-way handshake.  
- Jika sasaran membalas dengan **SYN-ACK**, ini menunjukkan port terbuka. Tetapi sebelum sambungan lengkap, **klien menghantar RST** untuk menutup sambungan.  
- Kelebihan:  
  - Kurang dikesan oleh firewall dan sistem log kerana sambungan tidak lengkap.  
  - Lebih pantas daripada **TCP Connect Scan**.  

### **3. Xmas Scan (-sX)**  
- Menggunakan paket khas dengan **FIN, URG, dan PUSH flags** dihidupkan.  
- Jika port **tertutup**, sasaran membalas dengan **RST**. Jika **terbuka**, tiada respons diterima.  
- Teknik ini lebih sesuai untuk **sistem UNIX/Linux** kerana Windows **tidak mengikuti** RFC 793 dalam menjawab imbasan ini.  

### **4. TCP Maimon Scan (-sM)**  
- Mirip dengan **Xmas Scan**, tetapi ia menggunakan **FIN/ACK flags** untuk menentukan sama ada port terbuka atau ditapis.  
- Jika **tiada respons**, port dianggap **Open|Filtered**. Jika **Sasaran menghantar RST**, port ditutup.  

### **5. ACK Flag Probe Scan (-sA)**  
- Digunakan untuk menentukan **kehadiran firewall** dalam rangkaian.  
- Jika tiada respons, bermakna port ditapis oleh **firewall stateful**.  
- Jika mendapat **RST**, port dianggap tidak ditapis.  

### **6. UDP Scan (-sU)**  
- Berbeza dengan **TCP scan**, UDP tidak mempunyai **three-way handshake**.  
- Jika tiada respons, port dianggap **terbuka**. Jika **ICMP Port Unreachable** diterima, port dianggap tertutup.  
- UDP scan lebih perlahan kerana kebanyakan peranti hadkan kadar penghantaran ICMP untuk mengelakkan **DoS attack**.  

### **7. Service Version Detection (-sV)**  
- Mengimbas port terbuka dan cuba mengenal pasti **versi perisian yang sedang berjalan**.  
- Sangat berguna dalam mengenal pasti **kerentanan** kerana kita boleh mengetahui versi perkhidmatan dan melihat sama ada ia mempunyai kelemahan keselamatan.  

### **8. Aggressive Scan (-A)**  
- Menggabungkan beberapa teknik seperti:  
  - **OS detection (-O)** – untuk mengenal pasti sistem operasi.  
  - **Version scanning (-sV)** – untuk mendapatkan maklumat versi perkhidmatan.  
  - **Script scanning (-sC)** – menggunakan skrip Nmap untuk eksplorasi lanjut.  
  - **Traceroute (--traceroute)** – menentukan laluan paket dalam rangkaian.  
- Sesuai digunakan jika anda ingin **memperoleh maklumat menyeluruh**, tetapi boleh menimbulkan syak wasangka di firewall dan sistem keselamatan.  

---

## **Langkah-Langkah Utama dalam Lab:**  
1. **Menjalankan TCP Connect Scan (-sT)** untuk mendapatkan maklumat asas tentang port terbuka.  
2. **Menjalankan Stealth Scan (-sS)** untuk melihat perbezaan hasil apabila firewall diaktifkan.  
3. **Menguji teknik imbasan khas seperti Xmas Scan (-sX), Maimon Scan (-sM), dan ACK Flag Probe Scan (-sA)** untuk mengenal pasti bagaimana firewall mempengaruhi hasil imbasan.  
4. **Menjalankan UDP Scan (-sU)** untuk mengimbas port UDP, yang biasanya digunakan oleh perkhidmatan seperti **DNS, DHCP, dan SNMP**.  
5. **Menggunakan Service Version Detection (-sV)** untuk mengenal pasti versi perkhidmatan yang berjalan.  
6. **Menjalankan Aggressive Scan (-A)** untuk mendapatkan maklumat mendalam mengenai hos sasaran.  
7. **Menguji kesan firewall dengan menghidupkan dan mematikan Windows Defender Firewall** di Windows Server 2022 dan melihat perubahan hasil imbasan.  

---

## **Penemuan dan Analisis:**  
- Apabila firewall dihidupkan, sesetengah imbasan seperti **Xmas Scan dan ACK Scan** menunjukkan port sebagai **filtered**, menandakan kehadiran firewall yang menyekat respons.  
- **Stealth Scan (-sS)** lebih sesuai untuk mengelak daripada dikesan kerana ia tidak melengkapkan three-way handshake.  
- **UDP Scan (-sU)** mengambil masa lebih lama kerana ketiadaan respons bukan semestinya bermaksud port tertutup.  
- **Service Version Detection (-sV)** membolehkan kita mengenal pasti versi perisian yang digunakan, yang penting dalam mencari eksploitasi.  

---

## **Kesimpulan:**  
Lab ini memberi pemahaman mendalam tentang **pelbagai teknik imbasan rangkaian** menggunakan **Nmap**. Setiap teknik mempunyai kelebihan dan kelemahan bergantung kepada **konfigurasi rangkaian, firewall, dan sistem keselamatan**.  

- **Jika sasaran tiada firewall**, TCP Connect Scan atau UDP Scan boleh digunakan untuk mendapatkan maklumat lengkap.  
- **Jika firewall diaktifkan**, teknik seperti **Stealth Scan, Xmas Scan, dan ACK Scan** lebih sesuai untuk mengenal pasti perkhidmatan yang ada.  
- **Service Version Detection (-sV) dan Aggressive Scan (-A)** sangat membantu dalam mengenal pasti perisian yang digunakan serta potensi kelemahan keselamatan.  

Lab ini menunjukkan betapa pentingnya **pemilihan teknik imbasan yang betul** dalam melakukan **pengujian keselamatan** tanpa menarik perhatian sistem pertahanan rangkaian.  

---

### **Ringkasan Lab 3: Perform OS Discovery**  

Dalam **Lab 3**, kita meneroka teknik **OS discovery (pengenalpastian sistem operasi)** menggunakan **Nmap dan Nmap Scripting Engine (NSE)**. Mengenal pasti OS pada sistem sasaran adalah penting dalam **ujian penembusan (pentesting)** kerana ia membolehkan kita:  
- **Menilai kerentanan sistem** berdasarkan versi OS yang digunakan.  
- **Menentukan eksploitasi yang sesuai** untuk serangan lanjut.  

---

## **Konsep OS Discovery dan Banner Grabbing**  

OS discovery, atau **banner grabbing**, ialah teknik untuk mengenal pasti sistem operasi yang berjalan pada hos sasaran. Terdapat **dua jenis banner grabbing**:  

### **1. Active Banner Grabbing**  
- Menghantar **paket khas** ke sasaran dan menganalisis respons.  
- Setiap OS mempunyai **cara tersendiri** dalam menangani permintaan rangkaian, yang membolehkan kita menentukan jenis OS.  
- Contoh parameter yang diperhatikan:  
  - **Time To Live (TTL):** Menentukan berapa lama paket boleh berada dalam rangkaian sebelum tamat.  
  - **TCP Window Size:** Saiz tetingkap TCP dalam sesi pertama, yang berbeza mengikut OS.  

### **2. Passive Banner Grabbing**  
- Tidak menghantar paket khas, tetapi mengumpul maklumat daripada:  
  - **Mesej ralat (error messages)** yang dihantar oleh sasaran.  
  - **Pemerhatian trafik rangkaian (sniffing network traffic).**  
  - **Jenis sambungan yang diterima oleh hos (seperti sambungan halaman web).**  
- Lebih **sukar dikesan** oleh firewall kerana tidak melibatkan aktiviti imbasan langsung.  

---

## **Teknik OS Discovery menggunakan Nmap**  

Nmap menyediakan beberapa kaedah untuk mengenal pasti sistem operasi, termasuk penggunaan parameter khas dan skrip NSE.  

### **1. Aggressive Scan (-A)**
- Menggunakan kombinasi pelbagai teknik untuk mendapatkan maklumat terperinci.  
- Perintah:  
  ```bash
  nmap -A 10.10.1.22
  ```  
- **Maklumat yang diperoleh:**  
  - Port terbuka dan perkhidmatan yang berjalan.  
  - Versi perisian yang digunakan.  
  - Nama komputer dan nama domain.  
  - NetBIOS dan Workgroup jika sistem menyokong SMB.  

---

### **2. OS Discovery (-O)**
- Khusus untuk mengenal pasti sistem operasi berdasarkan **TTL dan TCP Window Size**.  
- Perintah:  
  ```bash
  nmap -O 10.10.1.22
  ```  
- **Maklumat yang diperoleh:**  
  - Versi OS yang digunakan.  
  - Kemungkinan varian sistem operasi (contohnya, Windows Server 2022 atau versi Windows lain).  

---

### **3. OS Discovery melalui SMB dengan NSE**
- Menggunakan skrip **smb-os-discovery.nse** untuk mendapatkan maklumat OS melalui protokol SMB (port 445 atau 139).  
- Perintah:  
  ```bash
  nmap --script smb-os-discovery.nse 10.10.1.22
  ```  
- **Maklumat yang diperoleh:**  
  - Nama OS.  
  - Nama komputer dan domain.  
  - Workgroup dan masa sistem.  

---

## **Kesimpulan**  
- Teknik **active banner grabbing** memberikan maklumat lebih pantas tetapi boleh dikesan oleh firewall.  
- Teknik **passive banner grabbing** lebih sukar dikesan tetapi mungkin mengambil masa lebih lama.  
- **Nmap -A dan -O** digunakan untuk mendapatkan maklumat OS secara langsung.  
- **Skrip NSE smb-os-discovery** memberikan maklumat tambahan melalui SMB.  

Lab ini menunjukkan bagaimana kita boleh menggunakan **Nmap dan NSE** untuk mengenal pasti OS sasaran dengan tepat, membantu dalam **perancangan ujian penembusan yang lebih efektif**.

---
Berikut adalah huraian untuk **Lab 4: Scan Beyond IDS and Firewall**  

---

### **Pengenalan**
Selepas mengenal pasti sistem operasi (OS) pada sistem sasaran, langkah seterusnya dalam ujian penembusan (penetration testing) ialah melakukan pengimbasan rangkaian tanpa dikesan oleh sistem keselamatan seperti **Intrusion Detection System (IDS)** dan **Firewall**. Walaupun IDS dan firewall bertujuan untuk mencegah akses yang tidak dibenarkan, ia masih mempunyai kelemahan yang boleh dieksploitasi dengan pelbagai teknik pengelakan (evasion techniques).  

Dalam makmal ini, kita akan menggunakan **Nmap** untuk mengimbas sistem yang dilindungi oleh firewall dan IDS dengan beberapa teknik khas.  

---

### **Objektif Makmal**
- Melakukan pengimbasan yang melepasi IDS dan firewall menggunakan teknik pengelakan.

---

### **Konsep Pengimbasan Beyond IDS dan Firewall**
IDS dan firewall adalah mekanisme keselamatan yang direka untuk menyekat akses yang tidak dibenarkan. Namun, terdapat beberapa kelemahan yang membolehkan penggodam melepasi perlindungan ini menggunakan teknik seperti:  

1. **Packet Fragmentation**  
   - Memecahkan paket data menjadi kepingan kecil untuk mengelak pengesanan IDS.  
   - Dilakukan dengan `-f` dalam Nmap.  

2. **Source Routing**  
   - Menentukan laluan tertentu untuk paket supaya ia mengelak sekatan firewall.  

3. **Source Port Manipulation**  
   - Menggunakan nombor port yang biasa digunakan oleh perkhidmatan sah (contohnya, HTTP - port 80) untuk mengelak sekatan firewall.  
   - Dilakukan dengan `-g` dalam Nmap.  

4. **IP Address Decoy**  
   - Menyamar dengan menggunakan beberapa alamat IP palsu supaya IDS tidak dapat mengenal pasti IP sebenar penyerang.  
   - Dilakukan dengan `-D` dalam Nmap.  

5. **IP Address Spoofing**  
   - Menukar alamat IP sumber kepada alamat lain supaya aktiviti pengimbasan kelihatan seolah-olah datang dari sumber lain.  

6. **Creating Custom Packets**  
   - Menghantar paket khas dengan data yang diubah suai untuk mengelak sekatan.  

7. **Randomizing Host Order**  
   - Mengimbas hos dalam urutan rawak supaya IDS sukar mengenal pasti corak serangan.  

8. **Sending Bad Checksums**  
   - Menghantar paket dengan nilai checksum yang salah untuk mengelakkan pengesanan oleh IDS.  

9. **Proxy Servers**  
   - Menggunakan rangkaian proksi untuk menyembunyikan alamat IP sebenar semasa melakukan pengimbasan.  

10. **Anonymizers**  
   - Menggunakan perkhidmatan seperti VPN atau Tor untuk menyembunyikan identiti semasa pengimbasan.  

---

### **Langkah-langkah Makmal**
#### **1. Packet Fragmentation**
- Teknik ini membahagikan paket kepada bahagian kecil supaya IDS tidak dapat mengesan keseluruhan paket.  
- Jalankan perintah berikut di **Parrot Security Machine**:  
  ```bash
  nmap -f 10.10.1.11
  ```
- Perhatikan di **Wireshark (Windows 11)** bahawa paket telah dipecahkan menjadi bahagian kecil.  

---

#### **2. Source Port Manipulation**
- Menggunakan nombor port yang biasa digunakan oleh perkhidmatan lain untuk mengelak firewall.  
- Jalankan perintah:  
  ```bash
  nmap -g 80 10.10.1.11
  ```
- Semak di **Wireshark** bahawa trafik berasal dari port 80.  

---

#### **3. Menggunakan MTU (Maximum Transmission Unit)**
- MTU menentukan saiz maksimum paket yang boleh dihantar.  
- Pengurangan saiz MTU boleh mengelak sekatan firewall.  
- Jalankan perintah:  
  ```bash
  nmap -mtu 8 10.10.1.11
  ```
- Semak di **Wireshark** bahawa paket dihantar dalam saiz kecil (8 byte).  

---

#### **4. IP Address Decoy**
- Menggunakan alamat IP palsu untuk menyukarkan IDS mengenal pasti alamat sebenar.  
- Jalankan perintah:  
  ```bash
  nmap -D RND:10 10.10.1.11
  ```
- Semak di **Wireshark** bahawa terdapat pelbagai alamat IP dalam sumber paket.  

---

#### **5. MAC Address Spoofing**
- Menyamar sebagai peranti lain dalam rangkaian dengan menukar alamat MAC.  
- Jalankan perintah:  
  ```bash
  nmap -sT -Pn --spoof-mac 0 10.10.1.11
  ```
- Semak di **Wireshark** bahawa alamat MAC telah diubah.  

---

### **Kesimpulan**
Dalam makmal ini, kita telah mempelajari beberapa teknik untuk mengelak IDS dan firewall semasa melakukan pengimbasan rangkaian. Teknik ini penting untuk menguji keselamatan sesebuah rangkaian dan memastikan perlindungan IDS serta firewall dikonfigurasi dengan betul.  

---

Berikut adalah huraian untuk **Lab 5: Perform Network Scanning using Various Scanning Tools**  

---

### **Pengenalan**  
Makmal ini memberi fokus kepada kaedah pengimbasan rangkaian menggunakan pelbagai alat untuk mendapatkan maklumat tentang hos yang aktif, port terbuka, perkhidmatan yang berjalan, dan sistem operasi pada rangkaian sasaran.  

Sebagai seorang **ethical hacker** dan **pen tester**, adalah penting untuk mengumpul sebanyak mungkin maklumat tentang sasaran bagi mengenal pasti kelemahan yang berpotensi dieksploitasi. Dalam makmal ini, kita akan menggunakan **Metasploit Framework** sebagai alat utama untuk melakukan pengimbasan rangkaian.  

---

### **Objektif Makmal**  
1. Melakukan pengimbasan rangkaian menggunakan **Metasploit** untuk mengenal pasti:  
   - Hos yang aktif  
   - Port terbuka  
   - Perkhidmatan yang berjalan  
   - Maklumat sistem operasi (OS) pada rangkaian sasaran  

---

### **Alatan Pengimbasan Rangkaian**  
Pengimbas rangkaian digunakan untuk mengenal pasti hos yang aktif, port terbuka, dan perkhidmatan yang sedang berjalan dalam sesuatu rangkaian. Antara maklumat yang boleh diperoleh termasuk:  
- **Alamat IP hos yang aktif**  
- **Port TCP dan UDP yang terbuka**  
- **Maklumat perkhidmatan (contohnya, versi perisian yang berjalan pada port tersebut)**  
- **Maklumat OS sasaran**  
- **Maklumat NetBIOS dan SMB**  

Maklumat ini membantu dalam **profiling** organisasi sasaran dan membolehkan pentester merancang langkah seterusnya dalam ujian keselamatan.  

---

## **Langkah-Langkah Makmal**  

### **Task 1: Scan a Target Network using Metasploit**  

#### **1. Menjalankan Metasploit Framework**  
1. Buka **Parrot Security** dan buka Terminal.  
2. Taip perintah berikut untuk mendapatkan akses root:  
   ```bash
   sudo su
   ```
   - Masukkan kata laluan: **toor** (tidak akan dipaparkan semasa ditaip).  
3. Jalankan Metasploit dengan perintah:  
   ```bash
   msfconsole
   ```
   - Ini akan membuka **Metasploit Command Line Interface (CLI)**.  

---

#### **2. Mengimbas Subnet menggunakan Nmap dalam Metasploit**  
1. Taip perintah berikut untuk mengimbas semua hos dalam subnet **10.10.1.0/24**:  
   ```bash
   nmap -Pn -sS -A -oX Test 10.10.1.0/24
   ```
   - **-Pn**: Abaikan ping dan terus imbas semua hos.  
   - **-sS**: Gunakan **SYN scan** untuk imbasan yang lebih pantas dan tidak terlalu mencurigakan.  
   - **-A**: Aktifkan pengesanan OS dan versi perkhidmatan.  
   - **-oX Test**: Simpan hasil dalam format XML dengan nama fail "Test".  
2. Proses ini mengambil kira-kira **5 minit**.  
3. Hasil imbasan akan memaparkan:  
   - Senarai hos yang aktif.  
   - Senarai port terbuka pada setiap hos.  
   - Perkhidmatan yang berjalan pada port terbuka.  
   - Maklumat OS sasaran.  

---

#### **3. Melakukan SYN Scan dengan Modul Metasploit**  
1. Taip perintah berikut untuk mencari modul **port scan**:  
   ```bash
   search portscan
   ```
2. Pilih modul **auxiliary/scanner/portscan/syn**:  
   ```bash
   use auxiliary/scanner/portscan/syn
   ```
3. Tetapkan parameter pengimbasan:  
   ```bash
   set INTERFACE eth0
   set PORTS 80
   set RHOSTS 10.10.1.5-23
   set THREADS 50
   ```
   - **PORTS**: Hanya mengimbas port 80.  
   - **RHOSTS**: Julat IP yang ingin diimbas.  
   - **THREADS**: Menetapkan jumlah benang serentak untuk mempercepatkan imbasan.  
4. Jalankan imbasan:  
   ```bash
   run
   ```
5. Hasilnya akan menunjukkan **port 80** yang terbuka pada hos dalam julat **10.10.1.5-23**.  

---

#### **4. Melakukan TCP Scan dengan Metasploit**  
1. Pilih modul **TCP port scan**:  
   ```bash
   use auxiliary/scanner/portscan/tcp
   ```
2. Paparkan pilihan modul:  
   ```bash
   show options
   ```
3. Tetapkan sasaran dan jalankan imbasan:  
   ```bash
   set RHOSTS 10.10.1.22
   run
   ```
   - Imbasan ini mengambil masa lebih lama (~20 minit).  
   - Hasilnya akan memaparkan **semua port TCP yang terbuka** pada **10.10.1.22**.  

---

#### **5. Menentukan OS Sasaran menggunakan SMB Version Scan**  
1. Kembali ke CLI utama Metasploit:  
   ```bash
   back
   ```
2. Pilih modul **SMB version scanner**:  
   ```bash
   use auxiliary/scanner/smb/smb_version
   ```
3. Tetapkan sasaran dan jalankan imbasan:  
   ```bash
   set RHOSTS 10.10.1.5-23
   set THREADS 11
   run
   ```
4. Hasil imbasan akan memaparkan:  
   - **Versi Windows** jika sistem menggunakan SMB.  
   - **Versi Samba** jika sistem adalah Linux.  
   - Maklumat ini berguna untuk mencari eksploitasi yang sesuai berdasarkan versi OS.  

---

## **Kesimpulan**  
Dalam makmal ini, kita telah menggunakan **Metasploit Framework** untuk mengimbas rangkaian sasaran dan mendapatkan maklumat penting mengenai hos yang aktif, port terbuka, perkhidmatan yang berjalan, serta sistem operasi yang digunakan.  

Maklumat ini amat berguna dalam langkah seterusnya untuk menjalankan **vulnerability analysis** bagi mengenal pasti kelemahan yang boleh dieksploitasi.  

---

### **Ringkasan Teknik yang Dipelajari**  
✅ **Nmap dalam Metasploit** untuk mengimbas subnet.  
✅ **SYN Scan** untuk mengesan port terbuka dengan cepat.  
✅ **TCP Scan** untuk melihat semua port terbuka.  
✅ **SMB Version Scan** untuk mengenal pasti OS sasaran.  

---
Berikut adalah huraian bagi **Lab 6: Perform Network Scanning using AI**  

---

## **Pengenalan**  
Dalam makmal ini, kita akan menggunakan **ShellGPT**, alat yang dikuasakan oleh AI, untuk mengimbas rangkaian sasaran dan mendapatkan maklumat berkaitan **hos aktif, port terbuka, perkhidmatan yang berjalan, dan sistem operasi**.  

AI membolehkan proses pengimbasan dilakukan dengan lebih cekap, pantas, dan tepat melalui automasi dan analisis lanjutan terhadap trafik rangkaian.  

---

## **Objektif Makmal**  
1. Menggunakan **ShellGPT** untuk mengimbas rangkaian sasaran.  
2. Menjalankan pelbagai jenis pengimbasan rangkaian menggunakan arahan AI.  
3. Mengenal pasti hos aktif, port terbuka, versi perkhidmatan, dan sistem operasi pada sasaran.  

---

## **Alatan yang Digunakan**  
1. **ShellGPT** – Alat AI untuk menjana arahan pengimbasan.  
2. **Nmap** – Pengimbas rangkaian untuk mendapatkan maklumat lanjut.  
3. **hping3** – Alat untuk melakukan imbasan paket rangkaian.  
4. **Metasploit** – Platform ujian penembusan yang digunakan untuk mengesan kelemahan.  
5. **Nikto** – Alat untuk mengimbas kelemahan dalam aplikasi web.  

---

## **Langkah-Langkah Makmal**  

### **1. Menyediakan Persekitaran**  
- Buka **Parrot Security** dan log masuk sebagai pengguna `toor`.  
- Jalankan terminal dan masukkan arahan berikut untuk mendapatkan akses root:  
  ```bash
  sudo su
  ```
- Pastikan **ShellGPT** telah disediakan mengikut dokumen **Integrate ShellGPT in Parrot Security Machine.pdf**.  

---

### **2. Melakukan Imbasan dengan ShellGPT**  

#### **a) ICMP Scan menggunakan hping3**  
Arahan:  
```bash
sgpt --chat scan --shell "Use hping3 to perform ICMP scanning on the target IP address 10.10.1.11 and stop after 10 iterations"
```
- Perintah ini akan menghantar **paket ICMP** kepada **10.10.1.11** dan berhenti selepas **10 kali ulangan**.  

#### **b) ACK Scan menggunakan hping3**  
Arahan:  
```bash
sgpt --chat scan --shell "Run a hping3 ACK scan on port 80 of target IP 10.10.1.11"
```
- Ujian ini digunakan untuk mengenal pasti **sama ada firewall aktif** pada sasaran.  

#### **c) Imbasan Subnet untuk Hos Aktif**  
Arahan:  
```bash
sgpt --chat scan --shell "Scan the target network 10.10.1.0/24 for active hosts and place only the IP addresses into a file scan1.txt"
```
- Imbasan ini akan mencari **hos yang aktif** dalam subnet **10.10.1.0/24** dan menyimpan hasilnya dalam fail `scan1.txt`.  

#### **d) Nmap Scan pada Hos Aktif**  
Arahan:  
```bash
sgpt --chat scan --shell "Run a fast but comprehensive nmap scan against scan1.txt with low verbosity and write the results to scan2.txt"
```
- Imbasan Nmap akan dilakukan terhadap IP dalam `scan1.txt`, dan hasilnya disimpan dalam `scan2.txt`.  

#### **e) ICMP ECHO Ping Sweep**  
Arahan:  
```bash
sgpt --chat scan --shell "Use nmap to perform ICMP ECHO ping sweep on the target network 10.10.1.0/24"
```
- Imbasan ini akan menghantar **ping** kepada semua IP dalam subnet untuk melihat respons.  

---

### **3. Mengimbas Port dan Perkhidmatan**  

#### **a) Mencari Port Terbuka**  
Arahan:  
```bash
sgpt --chat scan --shell "Use nmap to find open ports on target IP 10.10.1.11"
```
- Akan memaparkan **port yang terbuka** pada sistem sasaran **10.10.1.11**.  

#### **b) Stealth Scan**  
Arahan:  
```bash
sgpt --chat scan --shell "Perform stealth scan on target IP 10.10.1.11 and display the results"
```
- **Stealth scan** digunakan untuk **mengelak daripada dikesan oleh firewall atau IDS**.  

#### **c) XMAS Scan**  
Arahan:  
```bash
sgpt --chat scan --shell "Perform an XMAS scan on target IP 10.10.1.11"
```
- **XMAS scan** menghantar paket dengan **flag URG, PSH, dan FIN** untuk mengesan sistem yang tidak mematuhi piawaian TCP.  

#### **d) Imbasan Port dan Perkhidmatan terhadap Senarai IP**  
Arahan:  
```bash
sgpt --chat scan --shell "Use Nmap to scan for open ports and services against a list of IP addresses in scan1.txt and copy only the port, service and version information with the respective IP address to a new file called scan3.txt"
```
- Imbasan ini akan mendapatkan **maklumat port, perkhidmatan, dan versi**.  

#### **e) Penemuan Port menggunakan Metasploit**  
Arahan:  
```bash
sgpt --chat scan --shell "Use Metasploit to discover open ports on the IP address 10.10.1.22"
```
- **Metasploit** akan digunakan untuk **mengesan port terbuka** pada sasaran.  

---

### **4. Mengenal Pasti Sistem Operasi (OS Fingerprinting)**  

#### **a) Menggunakan Nmap untuk Versi Perkhidmatan dan OS**  
Arahan:  
```bash
sgpt --chat scan --shell "Use Nmap to scan open ports, MAC details, services running on open ports with their versions on target IP 10.10.1.11"
```
- Memaparkan **versi perkhidmatan dan maklumat OS** pada sasaran.  

#### **b) OS Discovery menggunakan TTL Value**  
Arahan:  
```bash
sgpt --chat scan --shell "Use TTL value and identify the operating system running on the target IP address 10.10.1.11, display the TTL value and OS"
```
- Menggunakan **Time-to-Live (TTL)** untuk menentukan jenis sistem operasi.  

#### **c) OS Discovery menggunakan Nmap Script Engine**  
Arahan:  
```bash
sgpt --chat scan --shell "Use Nmap script engine to perform OS discovery on the target IP addresses in scan1.txt"
```
- **Nmap Script Engine (NSE)** digunakan untuk mendapatkan maklumat OS bagi **semua IP dalam scan1.txt**.  

---

### **5. Automasi Pengimbasan dengan Skrip**  

#### **a) Membina Skrip Automasi**  
Arahan:  
```bash
sgpt --chat scan --shell "Develop a script which will automate network scanning efforts and find out live systems, open ports, running services, service versions, etc. on target IP range 10.10.1.0/24"
```
- ShellGPT akan menghasilkan skrip **untuk automasi pengimbasan**.  

#### **b) Menjalankan Skrip Nmap dan Nikto**  
Arahan:  
```bash
sgpt --chat scancode --code "Create a python script to run a fast but comprehensive Nmap scan on the IP addresses in scan1.txt and then execute vulnerability scanning using nikto against each IP address in scan1.txt"
```
- Skrip akan **mengimbas kelemahan** dalam aplikasi web menggunakan **Nikto**.  

---

## **Kesimpulan**  
Makmal ini menunjukkan bagaimana **ShellGPT boleh digunakan untuk automasi dan pemudahan proses pengimbasan rangkaian**. Ia memberikan kelebihan dari segi **ketepatan, kecekapan, dan kelajuan** dalam mengenal pasti kelemahan dalam sistem sasaran.  

Untuk soalan **3.6.1.1**, arahan berikut boleh digunakan untuk mencari servis yang berjalan pada **port 139** di Windows 11:  
```bash
sgpt --chat scan --shell "Use Nmap to check for services running on port 139 of Windows 11 virtual machine (10.10.1.11)"
```
- **Jawapan:** Port **139** digunakan oleh **NetBIOS-SSN** (**NetBIOS Session Service**). 🚀
