## **Ringkasan Modul 02: Footprinting dan Reconnaissance**  

### **Pengenalan**  
Reconnaissance merujuk kepada proses mengumpul maklumat tentang sasaran, yang merupakan langkah pertama dalam sebarang serangan ke atas sistem. Ia berasal daripada operasi ketenteraan, di mana konsep ini digunakan untuk mengumpulkan maklumat mengenai musuh. Dalam konteks keselamatan siber, reconnaissance membantu penyerang atau penguji keselamatan memahami struktur sasaran dan menentukan strategi terbaik untuk menembusi sistem tersebut.  

Sebagai seorang **ethical hacker** atau **pen tester**, langkah pertama dalam penilaian keselamatan adalah mengumpulkan maklumat sebanyak mungkin tentang sasaran sebelum memulakan ujian. Proses ini dikenali sebagai **footprinting**, di mana hasilnya akan menghasilkan “blueprint” atau gambaran lengkap tentang organisasi yang diuji.  

### **Objektif Modul**  
Modul ini bertujuan untuk mengajar teknik footprinting bagi mendapatkan maklumat penting seperti:  
✅ Maklumat organisasi: Alamat, butiran pekerja, teknologi web, paten, jenama dagangan, dan pautan laman web  
✅ Maklumat rangkaian: Domain, subdomain, alamat IP, rekod DNS, firewall, dan topologi rangkaian  
✅ Maklumat sistem: Sistem operasi, lokasi pelayan web, akaun pengguna, dan kata laluan  

### **Jenis-jenis Footprinting**  
Footprinting terbahagi kepada dua jenis utama:  
🔹 **Footprinting Pasif** – Mengumpul maklumat tanpa berinteraksi secara langsung dengan sasaran. Contoh: Menggunakan enjin carian dan media sosial.  
🔹 **Footprinting Aktif** – Mengumpul maklumat dengan berinteraksi secara langsung dengan sasaran, seperti menggunakan `ping`, `traceroute`, atau `nslookup`.  

### **Kaedah Footprinting**  
✅ **Footprinting melalui enjin carian**  
   - Menggunakan teknik Google Hacking untuk mencari maklumat sensitif tentang organisasi  

✅ **Footprinting melalui perkhidmatan penyelidikan Internet**  
   - Menggunakan **Netcraft** dan **DNSdumpster** untuk mendapatkan subdomain, DNS records, dan maklumat hos  

✅ **Footprinting melalui media sosial**  
   - Menggunakan alat seperti **Sherlock** untuk mencari akaun media sosial pekerja organisasi  

✅ **Footprinting melalui WHOIS lookup**  
   - Mendapatkan butiran pemilik domain menggunakan **DomainTools**  

✅ **Footprinting melalui DNS**  
   - Menggunakan perintah `nslookup` atau alat dalam talian untuk mendapatkan rekod DNS  

✅ **Footprinting melalui traceroute**  
   - Menjejak laluan rangkaian ke pelayan sasaran menggunakan `tracert` atau `traceroute`  

✅ **Footprinting melalui e-mel**  
   - Menggunakan **eMailTrackerPro** untuk menjejak penghantar e-mel dan lokasi pelayan  

✅ **Footprinting menggunakan alat khusus**  
   - **Recon-ng**: Platform footprinting automatik  
   - **ShellGPT**: Menggunakan AI untuk mengumpul dan menganalisis data footprinting  

### **Kesimpulan**  
Footprinting dan reconnaissance adalah langkah penting dalam keselamatan siber kerana ia membantu mengenal pasti kelemahan sistem sebelum serangan berlaku. Dengan memahami teknik yang digunakan oleh penyerang, organisasi boleh mengambil langkah pencegahan untuk melindungi maklumat sensitif dan mengurangkan risiko serangan.

### **Ringkasan Lab 1: Footprinting Melalui Enjin Carian**  

#### **Senario**  
Sebagai seorang **ethical hacker** atau **pen tester**, langkah pertama adalah mengumpulkan sebanyak mungkin maklumat tentang organisasi sasaran melalui enjin carian. Teknik ini boleh digunakan untuk mendapatkan maklumat kritikal seperti platform teknologi, butiran pekerja, halaman log masuk, portal intranet, dan maklumat hubungan organisasi. Data yang diperoleh boleh digunakan dalam serangan kejuruteraan sosial atau serangan lanjutan terhadap sistem.  

#### **Objektif Lab**  
✅ Menggunakan teknik **Google Hacking** untuk mendapatkan maklumat tersembunyi tentang sasaran.  

#### **Gambaran Enjin Carian**  
🔹 Enjin carian seperti Google, Bing, dan DuckDuckGo menggunakan **crawler** untuk mengindeks laman web yang aktif dan menyimpan hasilnya dalam pangkalan data besar.  
🔹 Apabila pengguna membuat carian, enjin akan memaparkan **Search Engine Results Pages (SERPs)** berdasarkan tahap kesesuaian maklumat.  

---

### **Tugasan: Menggunakan Teknik Google Hacking**  

1️⃣ **Mengesan Halaman Log Masuk**  
   - **Perintah:** `intitle:login site:eccouncil.org`  
   - **Fungsi:** Mendapatkan halaman log masuk dari laman web sasaran.  
   - **Kepentingan:** Penyerang boleh menggunakan serangan **bruteforce** atau **injection attack** pada halaman ini.  

2️⃣ **Mencari Dokumen Sensitif**  
   - **Perintah:** `EC-Council filetype:pdf ceh`  
   - **Fungsi:** Mencari fail PDF berkaitan CEH dalam laman EC-Council.  
   - **Kepentingan:** Dokumen seperti manual, laporan, dan fail konfigurasi boleh mengandungi maklumat sensitif tentang produk dan perkhidmatan organisasi.  

3️⃣ **Operator Google Lanjutan untuk Footprinting**  
   - `cache:www.eccouncil.org` → Paparkan versi laman yang disimpan dalam cache Google.  
   - `allinurl:EC-Council career` → Cari halaman dengan kata kunci “EC-Council” dan “career” dalam URL.  
   - `inurl:copy site:www.eccouncil.org` → Cari halaman dalam laman sasaran yang mengandungi perkataan “copy” dalam URL.  
   - `allintitle:detect malware` → Cari halaman yang mempunyai “detect” dan “malware” dalam tajuk.  
   - `inanchor:Norton` → Cari halaman yang mengandungi pautan dengan teks “Norton”.  
   - `link:www.eccouncil.org` → Cari laman web yang mempunyai pautan ke laman EC-Council.  
   - `related:www.eccouncil.org` → Cari laman web yang serupa dengan EC-Council.  
   - `info:eccouncil.org` → Dapatkan maklumat mengenai laman EC-Council.  
   - `location:EC-Council` → Dapatkan hasil carian berkaitan EC-Council berdasarkan lokasi.  

---

### **Kesimpulan**  
Teknik **Google Hacking** adalah kaedah footprinting yang berkesan untuk mendapatkan maklumat kritikal tentang sasaran. Ethical hackers boleh menggunakan teknik ini untuk menilai kelemahan keselamatan dan mengenal pasti data yang berpotensi dieksploitasi oleh penyerang. Dengan memahami cara kerja enjin carian dan operator lanjutan, pengetahuan ini dapat digunakan untuk melindungi organisasi daripada serangan siber yang merugikan.

### **Ringkasan Lab 2: Footprinting Melalui Perkhidmatan Penyelidikan Internet**  

#### **Senario**  
Sebagai **ethical hacker**, penting untuk mengumpulkan maklumat berkaitan organisasi sasaran menggunakan perkhidmatan penyelidikan internet. Maklumat yang boleh diekstrak termasuk:  
✅ **Domain & subdomain**  
✅ **Sistem operasi**  
✅ **Lokasi geografi**  
✅ **Maklumat pekerja & e-mel**  
✅ **Maklumat kewangan**  
✅ **Infrastruktur IT**  
✅ **Halaman web tersembunyi**  

Maklumat ini boleh membantu dalam membangunkan strategi serangan terhadap organisasi sasaran.  

---

### **Tugasan: Mencari Domain, Subdomain & Host Menggunakan Netcraft & DNSdumpster**  

#### **1️⃣ Mengesan Maklumat Domain & Subdomain dengan Netcraft**  
1. Layari **[https://www.netcraft.com](https://www.netcraft.com)** menggunakan Mozilla Firefox.  
2. Navigasi ke **Resources → Research Tools → Site Report**.  
3. Masukkan URL sasaran (**contoh: certifiedhacker.com**) dalam ruangan carian dan klik **LOOK UP**.  
4. Paparan laporan laman web akan muncul dengan maklumat seperti:  
   - **Infrastruktur IT**  
   - **Sejarah hosting**  
   - **Subdomain & sistem operasi**  
5. Klik pada **Domain** untuk melihat subdomain organisasi.  

📌 **Hasil**: Senarai subdomain dan sistem operasi boleh digunakan untuk mencari kelemahan organisasi.  

---

#### **2️⃣ Mencari Maklumat DNS, GeoIP & Domain Mapping dengan DNSdumpster**  
1. Layari **[https://dnsdumpster.com](https://dnsdumpster.com)**.  
2. Masukkan **certifiedhacker.com** dalam ruangan carian dan tekan **Search**.  
3. Hasil carian akan memaparkan:  
   - **GEO IP lokasi host**  
   - **Senarai DNS Servers & IP**  
   - **MX Records & Host Records (A)**  
   - **Domain mapping**  
4. Muat turun laporan **.xlsx** untuk analisis lanjut.  

📌 **Hasil**: Data ini boleh digunakan untuk merancang serangan seperti **brute-force**, **DoS**, atau **injection attacks**.  

---

### **Kesimpulan**  
🔹 **Netcraft & DNSdumpster** adalah alat footprinting penting untuk mengumpulkan maklumat tentang organisasi sasaran.  
🔹 **Penyerang** boleh menggunakan data ini untuk menyasarkan kelemahan dalam sistem organisasi.  
🔹 **Pentester** boleh menggunakan data ini untuk menguji sistem keselamatan dan meningkatkan pertahanan organisasi.  

---

#### **Soalan & Jawapan**  
✅ **Soalan 2.2.1.1**  
🔹 IP **ns2.bluehost.com** dari DNSdumpster untuk **certifiedhacker.com** → `162.159.25.175`  

✅ **Soalan 2.2.1.2**  
🔹 Sistem operasi pelayan web **www.eccouncil.org** dari Netcraft → `Linux`

### **Ringkasan Lab 3: Footprinting Melalui Laman Sosial**  

#### **Senario**  
Sebagai **ethical hacker**, penting untuk mengumpulkan maklumat peribadi pekerja organisasi sasaran melalui laman sosial seperti **LinkedIn, Facebook, Twitter, Instagram, YouTube**, dan sebagainya. Maklumat ini boleh digunakan untuk serangan **social engineering** dan serangan lanjut.  

Maklumat yang boleh dikumpulkan:  
✅ **Nama & jawatan pekerja**  
✅ **Nama syarikat & lokasi semasa**  
✅ **E-mel & nombor telefon**  
✅ **Gambar, video, dan aktiviti syarikat**  
✅ **Strategi perniagaan & projek syarikat**  

---

### **Tugasan: Mengumpul Maklumat Peribadi Menggunakan Sherlock**  

**🔹 Langkah-langkah:**  
1️⃣ **Hidupkan Parrot Security VM** dan log masuk sebagai `attacker/toor`.  
2️⃣ **Buka Terminal** dan jalankan **sudo su** untuk akses root (masukkan `toor` sebagai kata laluan).  
3️⃣ **Jalankan perintah berikut:**  
   ```bash
   sherlock "Elon Musk"
   ```  
4️⃣ Sherlock akan mencari akaun **Elon Musk** di pelbagai platform media sosial dan memaparkan URL berkaitan.  
5️⃣ **Tatal ke bawah** untuk melihat semua hasil carian.  

📌 **Hasil**: Senarai akaun dan URL boleh digunakan untuk mendapatkan lebih banyak maklumat sensitif.  

---

### **Kesimpulan**  
🔹 **Sherlock** ialah alat footprinting penting untuk mengesan kehadiran digital sasaran di laman sosial.  
🔹 **Maklumat diperoleh** boleh digunakan untuk serangan **phishing**, **impersonation**, atau **social engineering**.  
🔹 Selain Sherlock, boleh guna **[Social Searcher](https://www.social-searcher.com/)** untuk mengumpul maklumat tambahan.  

---

#### **Soalan & Jawapan**  
✅ **Soalan 2.3.1.1**  
🔹 Masukkan URL berkaitan **Elon Musk** yang diperoleh dari laman sosial **Codewars** (hasil Sherlock).

### **Ringkasan Lab 4: Whois Footprinting**  

#### **Senario**  
Sebagai **ethical hacker**, footprinting melalui **Whois lookup** membolehkan kita mendapatkan **maklumat domain** sasaran seperti:  
✅ **Pemilik domain & pendaftar (registrar)**  
✅ **Tarikh pendaftaran & tarikh tamat domain**  
✅ **Alamat IP & lokasi pelayan**  
✅ **Nama pelayan (name servers)**  
✅ **Maklumat pentadbiran & teknikal**  

Maklumat ini boleh digunakan untuk:  
🔹 **Membina peta rangkaian organisasi**  
🔹 **Serangan social engineering**  
🔹 **Mendapatkan maklumat dalaman organisasi**  

---

### **Tugasan: Melakukan Whois Lookup menggunakan DomainTools**  

**🔹 Langkah-langkah:**  
1️⃣ **Gunakan Windows 11 VM** dan buka pelayar web (contoh: Firefox).  
2️⃣ Pergi ke **[Whois DomainTools](https://whois.domaintools.com/)**  
3️⃣ Dalam kotak carian, masukkan **www.certifiedhacker.com** dan tekan **Enter**.  
4️⃣ **Analisis hasil carian**, termasuk:  
   - Maklumat pendaftar (registrar)  
   - Nama pelayan (name servers)  
   - Alamat IP & lokasi domain  
   - Tarikh pendaftaran dan tarikh tamat domain  

---

### **Kesimpulan**  
✅ **Whois lookup** ialah teknik footprinting penting untuk mendapatkan **maklumat pemilikan domain**.  
✅ Maklumat ini boleh digunakan untuk **menganalisis kelemahan organisasi** dan **merancang serangan** seperti **phishing & domain spoofing**.  
✅ Selain DomainTools, boleh gunakan:  
   - 🔹 **[SmartWhois](https://www.tamos.com)**  
   - 🔹 **[Batch IP Converter](http://www.sabsoft.com)**  

---

#### **Soalan & Jawapan**  
✅ **Soalan 2.4.1.1**  
🔹 Masukkan **URL pendaftar (registrar)** untuk **www.certifiedhacker.com** yang diperoleh daripada DomainTools Whois lookup.

### **Ringkasan Lab 5: DNS Footprinting**  

#### **Senario**  
Sebagai **ethical hacker**, footprinting melalui **DNS lookup** membolehkan kita mendapatkan **maklumat pelayan DNS** sasaran seperti:  
✅ **Rekod DNS (A, CNAME, MX, NS, AAAA, dll.)**  
✅ **Alamat IP domain**  
✅ **Nama pelayan utama (Authoritative Name Server)**  
✅ **Mail Server (MX Records)**  

Maklumat ini boleh digunakan untuk:  
🔹 **Menganalisis struktur rangkaian organisasi**  
🔹 **Membantu dalam serangan social engineering**  
🔹 **Merancang serangan seperti DoS, DDoS, dan URL Redirection**  

---

### **Tugasan: Mengumpul Maklumat DNS menggunakan nslookup dan Alat Atas Talian**  

**🔹 Langkah-langkah:**  

#### **1️⃣ Gunakan nslookup dalam Command Prompt (Windows 11)**
1. **Buka Command Prompt** dalam Windows 11.  
2. Taip **nslookup** dan tekan **Enter** untuk melihat pelayan DNS lalai yang digunakan oleh sistem.  
3. Taip **set type=a** dan tekan **Enter** untuk mencari alamat IP domain.  
4. Masukkan **www.certifiedhacker.com** dan tekan **Enter** untuk melihat hasilnya.  
   - Jika jawapan yang diterima adalah **Non-Authoritative Answer**, ini bermaksud maklumat diperoleh daripada **cache DNS**, bukan daripada pelayan sebenar.  
   - Alamat IP domain akan dipaparkan.  

#### **2️⃣ Cari Pelayan Nama Utama (Authoritative Name Server)**
5. Taip **set type=cname** dan tekan **Enter** untuk mendapatkan **CNAME Records** domain.  
6. Taip **certifiedhacker.com** dan tekan **Enter** untuk melihat **Authoritative Name Server**.  
   - Contoh output: **ns1.bluehost.com**  

#### **3️⃣ Dapatkan Alamat IP Pelayan Nama Utama**
7. Taip **set type=a** dan tekan **Enter**.  
8. Masukkan **ns1.bluehost.com** (atau pelayan utama yang diperoleh) dan tekan **Enter**.  
   - Output akan memaparkan **alamat IP pelayan DNS utama**.  

---

### **Gunakan NSLOOKUP Online**  
Selain menggunakan **Command Prompt**, anda boleh juga melakukan footprinting menggunakan **NSLOOKUP Online**:  
1. Buka pelayar web dan pergi ke **[NSLOOKUP Kloth](http://www.kloth.net/services/nslookup.php)**.  
2. Masukkan **www.certifiedhacker.com** dalam **Domain Field**.  
3. Pilih **Query Type: A (IPv4 Address)** dan klik **Look it up**.  
4. Anda juga boleh mencuba **Query Type: AAAA (IPv6 Address)** untuk melihat maklumat IPv6.  

---

### **Kesimpulan**  
✅ **DNS footprinting** ialah teknik yang penting dalam **pengumpulan maklumat domain**.  
✅ Ethical hacker boleh menggunakan maklumat DNS untuk **menganalisis struktur rangkaian organisasi**.  
✅ Maklumat pelayan DNS boleh digunakan oleh penyerang untuk **merancang serangan DoS, DDoS, dan serangan terhadap pelayan e-mel**.  
✅ Selain nslookup dan NSLOOKUP Online, boleh juga guna:  
   - 🔹 **[DNSDumpster](https://dnsdumpster.com)**  

---

#### **Soalan & Jawapan**  
✅ **Soalan 2.5.1.1**  
🔹 Gunakan **nslookup** untuk mencari **Authoritative Name Server** bagi **www.certifiedhacker.com**.

### **Ringkasan Lab 6: Network Footprinting**  

#### **📌 Senario**  
Sebagai **ethical hacker**, **Network Footprinting** digunakan untuk mendapatkan **maklumat rangkaian organisasi**, termasuk:  
✅ **Julat rangkaian (Network Range)**  
✅ **Jejak laluan (Traceroute)**  
✅ **Alamat IP setiap hop**  
✅ **TTL (Time-To-Live) values**  

Maklumat ini membantu dalam:  
🔹 **Menganalisis topologi rangkaian sasaran**  
🔹 **Mengenal pasti firewall, router, dan peranti rangkaian lain**  
🔹 **Melakukan serangan seperti Man-in-the-Middle (MitM)**  

---

### **🔹 Tugasan: Melakukan Traceroute dalam Windows & Linux**  

### **1️⃣ Traceroute dalam Windows (Command Prompt)**
1. **Buka Command Prompt** dalam Windows 11.  
2. Jalankan arahan berikut untuk melihat laluan paket ke sasaran:  
   ```bash
   tracert www.certifiedhacker.com
   ```
   - Ini akan menunjukkan **hop (peranti rangkaian) yang dilalui** sebelum sampai ke destinasi.  
3. Untuk melihat pilihan tambahan, jalankan:  
   ```bash
   tracert /?
   ```
4. Hadkan jumlah **maximum hops** kepada 5 untuk mengelakkan traceroute yang terlalu panjang:  
   ```bash
   tracert -h 5 www.certifiedhacker.com
   ```
5. **Tutup Command Prompt** selepas mendapatkan hasil.  

---

### **2️⃣ Traceroute dalam Linux (Parrot Security Terminal)**
1. **Buka Terminal** dalam Parrot Security.  
2. Jalankan arahan berikut untuk melihat hop yang dilalui:  
   ```bash
   traceroute www.certifiedhacker.com
   ```
3. Hasil akan menunjukkan **alamat IP setiap hop**, termasuk **alamat IP pelayan akhir**.  

---

### **Kesimpulan**  
✅ **Traceroute membantu dalam menganalisis topologi rangkaian** sasaran.  
✅ **Ethical hacker boleh mengenal pasti lokasi firewall, router, dan pelayan penting**.  
✅ **Maklumat ini boleh dimanfaatkan oleh penyerang** untuk serangan seperti **DoS, DDoS, atau MitM**.  
✅ **Alat alternatif:**  
   - 🔹 **[PingPlotter](https://www.pingplotter.com/)**  
   - 🔹 **[Traceroute NG](https://www.solarwinds.com/)**  

---

#### **Soalan & Jawapan**  
✅ **Soalan 2.6.1.1**  
🔹 Jalankan **traceroute** dalam **Parrot Security** untuk **www.certifiedhacker.com**.  
✅ **Jawapan:**  
🔹 **Alamat IP sasaran:** **162.241.216.11**

### **Ringkasan Lab 7: Email Footprinting**  

#### **📌 Senario**  
Sebagai **ethical hacker**, **Email Footprinting** membolehkan anda **menjejaki email** untuk mendapatkan maklumat sensitif, seperti:  
✅ **Alamat IP penghantar & penerima**  
✅ **Maklumat lokasi GPS & peta penerima**  
✅ **Waktu email dibuka & dibaca**  
✅ **Jenis server & OS penerima**  
✅ **Jika email mempunyai link atau fail berbahaya**  
✅ **Jika email telah ditetapkan untuk luput**  

Maklumat ini berguna untuk:  
🔹 **Menganalisis sumber email & mengesan serangan phishing**  
🔹 **Melakukan serangan Social Engineering**  
🔹 **Mengenal pasti server & rangkaian organisasi sasaran**  

---

### **🔹 Tugasan: Menggunakan eMailTrackerPro untuk Menjejak Email**  

### **1️⃣ Langkah-langkah Menggunakan eMailTrackerPro**
1. **Buka Windows 11** dan pergi ke lokasi fail:  
   ```
   E:\CEH-Tools\CEHv13 Module 02 Footprinting and Reconnaissance\Email Tracking Tools\eMailTrackerPro
   ```
2. **Jalankan `emt.exe`** dan ikut wizard pemasangan.  
3. Selepas pemasangan selesai, **buka eMailTrackerPro**.  
4. Klik **OK** apabila pop-up "Edition Selection" muncul.  

---

### **2️⃣ Menganalisis Header Email**  
1. Klik **My Trace Reports** untuk melihat laporan terdahulu.  
2. Klik **Trace Headers** untuk memulakan analisis email.  
3. **Salin & tampal email header** dari email yang ingin dianalisis:  
   - **Gmail:**  
     - Buka email > Klik ikon **tiga titik (More)** > Pilih **Show Original**  
   - **Outlook:**  
     - Klik **More actions (tiga titik …)** > **View message source**  
4. Tekan **Trace** untuk menganalisis.  

---

### **3️⃣ Hasil Analisis dalam eMailTrackerPro**  
🔹 **Peta lokasi penghantar** ditunjukkan dalam GUI.  
🔹 **IP setiap hop** dalam laluan email dipaparkan dalam bentuk jadual.  
🔹 **Klik "Network Whois"** untuk mendapatkan maklumat rangkaian penghantar.  

---

### **🔹 Alat Alternatif untuk Email Tracking**  
- 🔹 **[MxToolbox](https://mxtoolbox.com/)**  
- 🔹 **[Social Catfish](https://socialcatfish.com/)**  
- 🔹 **[IP2Location Email Header Tracer](https://www.ip2location.com/)**  

---

#### **Soalan & Jawapan**  
✅ **Soalan 2.7.1.1**  
🔹 Gunakan **eMailTrackerPro** untuk menganalisis header email dan periksa jika terdapat ciri **"Abuse Reporting"**.  
✅ **Jawapan:**  
🔹 **YES**

### **Ringkasan Lab 8: Perform Footprinting menggunakan Pelbagai Alat Footprinting**  

#### **Objektif Lab**  
- Menggunakan **Recon-ng** untuk mengumpul maklumat mengenai sasaran.  

#### **Pengenalan Footprinting Tools**  
- Footprinting tools digunakan untuk mengumpul maklumat asas tentang sistem sasaran bagi mengenal pasti potensi kelemahan.  
- Maklumat yang boleh diperoleh termasuk:  
  - Lokasi IP sasaran  
  - Maklumat DNS dan domain  
  - Butiran syarikat, nombor telefon, alamat, dan maklumat lain  

---

### **Tugasan 1: Footprinting menggunakan Recon-ng**  

1. **Melancarkan Recon-ng**  
   - Buka terminal di **Parrot Security**  
   - Jalankan `sudo su` untuk akses root (guna password **toor**)  
   - Gunakan `recon-ng` untuk melancarkan aplikasi  

2. **Persediaan Workspace**  
   - Buat workspace: `workspaces create CEH`  
   - Masukkan domain sasaran: `db insert domains` → **certifiedhacker.com**  
   - Paparkan domain yang telah dimasukkan: `show domains`  

3. **Mengumpul Maklumat Host**  
   - Gunakan **brute_hosts** untuk mencari subdomain:  
     ```
     modules load recon/domains-hosts/brute_hosts
     run
     ```
   - Gunakan **Bing domain search** untuk mencari lebih banyak host:  
     ```
     modules load recon/domains-hosts/bing_domain_web
     run
     ```
   - Gunakan **reverse_resolve** untuk mencari host berkaitan dengan IP yang diperoleh:  
     ```
     modules load recon/hosts-hosts/reverse_resolve
     run
     ```

4. **Menyimpan Laporan**  
   - Gunakan **reporting/html** untuk menyimpan hasil footprinting dalam bentuk laporan:  
     ```
     modules load reporting/html
     options set FILENAME /home/attacker/Desktop/results.html
     options set CREATOR [Nama Anda]
     options set CUSTOMER Certifiedhacker Networks
     run
     ```

5. **Membuka Laporan**  
   - Navigasi ke `/home/attacker/Desktop/` dan buka laporan dalam Firefox  

---

### **Tugasan 2: Mengumpul Maklumat Individu**  
1. **Buat workspace baru untuk reconnaissance**  
   - `workspaces create reconnaissance`  

2. **Gunakan Whois untuk mendapatkan maklumat individu berkaitan domain**  
   - Muatkan modul **whois_pocs**:  
     ```
     modules load recon/domains-contacts/whois_pocs
     options set SOURCE facebook.com
     run
     ```
   - Hasilnya ialah senarai individu yang berkaitan dengan domain sasaran  

---

### **Tugasan 3: Mencari Subdomain dan IP Berkaitan**  
1. **Gunakan modul hackertarget** untuk mencari subdomain dan IP yang berkaitan  
   ```
   modules load recon/domains-hosts/hackertarget
   options set SOURCE certifiedhacker.com
   run
   ```

---

### **Kesimpulan**  
- **Recon-ng** adalah alat footprinting yang sangat berguna untuk **mendapatkan maklumat domain, subdomain, IP, dan individu berkaitan dengan sasaran**.  
- Footprinting membolehkan **penggodam beretika** mengenal pasti kelemahan yang boleh dieksploitasi dalam ujian keselamatan.  
- Laporan footprinting boleh dijana dalam bentuk **HTML** untuk dianalisis kemudian.  

---

✅ **Jawapan Soalan 2.8.1.1:**  
Modul Recon-ng yang digunakan untuk mendapatkan maklumat individu ialah:  
**`recon/domains-contacts/whois_pocs`**  

### **Ringkasan Lab 9: Perform Footprinting menggunakan AI**  

#### **Objektif Lab**  
- Menggunakan **ShellGPT** untuk melakukan footprinting ke atas sasaran.  

---

### **Pengenalan kepada Footprinting menggunakan AI**  
- **AI mempercepatkan proses footprinting** dengan mengautomasikan pengumpulan dan analisis data.  
- AI boleh mengenal pasti **pola dan anomali** dalam data yang besar, membantu mengenal pasti risiko keselamatan dengan lebih cekap.  

---

### **Tugasan 1: Footprinting Sasaran menggunakan ShellGPT**  

#### **1. Mengintegrasikan ShellGPT dalam Parrot Security**  
- Pastikan ShellGPT telah diintegrasikan mengikut langkah dalam **Integrate ShellGPT in Parrot Security Machine.pdf** atau **Module 00**.  

#### **2. Mengumpul Maklumat E-mel Menggunakan theHarvester**  
Jalankan perintah berikut untuk mendapatkan e-mel berkaitan **microsoft.com**:  
```
sgpt --chat footprint --shell “Use theHarvester to gather email accounts associated with 'microsoft.com', limiting results to 200, and leveraging 'baidu' as a data source”
```
- Tekan **E** dan **Enter** untuk melaksanakan arahan.  
- Output akan memaparkan **senarai e-mel dan hos yang berkaitan**.  

---

#### **3. Footprinting Melalui Media Sosial Menggunakan Sherlock**  
Jalankan perintah berikut untuk mengumpul maklumat peribadi **Sundar Pichai**:  
```
sgpt --chat footprint --shell “Use Sherlock to gather personal information about 'Sundar Pichai' and save the result in recon2.txt”
```
- Tekan **E** dan **Enter** untuk menjalankan arahan.  
- Fail **recon2.txt** akan dicipta.  
- Gunakan arahan `pluma recon2.txt` untuk melihat kandungan fail.  

---

#### **4. Melakukan DNS Enumeration Menggunakan DNSRecon**  
Jalankan perintah berikut untuk **mendapatkan maklumat DNS bagi www.certifiedhacker.com**:  
```
sgpt --chat footprint --shell “Install and use DNSRecon to perform DNS enumeration on the target domain www.certifiedhacker.com”
```
- Tekan **E** dan **Enter** untuk menjalankan arahan.  
- Perintah ini akan mengenal pasti **rekod DNS**, termasuk **NS, MX, dan A records**.  

---

#### **5. Melakukan Traceroute ke Sasaran**  
Gunakan arahan berikut untuk mengenal pasti **laluan rangkaian** ke hos sasaran:  
```
sgpt --chat footprint --shell “Perform network tracerouting to discover the routers on the path to a target host www.certifiedhacker.com”
```
- Tekan **E** dan **Enter** untuk melihat **senarai nod perantara**.  

---

#### **6. Menjana Skrip Python untuk Footprinting Automatik**  
Gunakan ShellGPT untuk mencipta skrip Python yang melakukan footprinting secara automatik:  
```
sgpt --chat footprint --shell “Develop a Python script which will accept domain name microsoft.com as input and execute a series of website footprinting commands, including DNS lookups, WHOIS records retrieval, email enumeration, and more to gather information about the target domain”
```
- Tekan **E** dan **Enter** untuk menghasilkan dan menjalankan skrip Python.  
- Skrip ini akan melakukan footprinting secara automatik ke atas **microsoft.com**.  

---

### **Kesimpulan**  
- **ShellGPT** mengautomasikan proses footprinting dengan **menggunakan AI** untuk menganalisis data dengan lebih cekap.  
- **Alat seperti theHarvester, Sherlock, DNSRecon, dan Traceroute** membantu dalam mengenal pasti e-mel, maklumat peribadi, dan butiran rangkaian.  
- **Penggunaan Python** membolehkan footprinting dilakukan secara automatik dan lebih sistematik.  

---

✅ **Jawapan Soalan 2.9.1.1:**  
**Gunakan ShellGPT untuk melakukan DNS enumeration pada www.certifiedhacker.com:**  
```
sgpt --chat footprint --shell “Install and use DNSRecon to perform DNS enumeration on the target domain www.certifiedhacker.com”
```
**IP address of NS ns2.bluehost.com:**  
✅ **162.159.25.175**  

---