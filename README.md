# Gatau saya mau sharing aja
Pengen sharing aja saya mah bener ga pengen yang lain

# Cara-cara Pentest
Sederhananya ada 3 tahapan penting di Pentest yaitu information gathering, exploit dan reporting.
### 1. Information Gathering

Merupakan tahapan dimana kita sudah tau objek mana yang akan kita jadikan target, ya kalo belum pastiin dulu aja targetnya apa, dimana dan fungsinya apa. Informasi ini bakal berguna sih harusnya dalam menentukan tahapan kita selanjutnya mau ngapain terhadap target.
`Di tahap ini kita tuh bebas deh ngapain aja untuk cari tau informasi yang lebih supaya kita bisa cari celah dari aplikasi tersebut, baik kita eksplor dulu appsnya atau misalnya pake teknik-teknik apa gitu buat nemuin informasi lain yang terhubung sama aplikasi itu.`
 Misalnya kalo di web nih, kalo targetnya adalah aplikasi target.com berarti kita bisa mulai dari ini target pake web server apa, trus mungkin OS yang dijalankan dan lainnya. Kalo pas di dalem aplikasinya sendiri kita liat komunikasi antara client dan server, apakah ada server lain selain target.com yang dijadikan acuan oleh aplikasi? Kalo iya yaa itu juga bisa dibilang bagian dari scope kita, my friend.

Gampangnya information gathering ini diperlukan untuk extend visibility kita akan sesuatu. Contoh, misalnya mau beli mobil. Kalo kita liat mobil dari merk aja atau dari foto aja atau dari luarnya aja, mungkin kita akan miss dibagian mesin padahal ternyata dibagian mesin ini ada yang kurang. Nah biasanya kalo mau pentest atau bug hunt itu, kita akan dikasih akses dan informasi minim banget tentang target. Biasanya dikasih cuman domain-domain yang masuk kedalam target. Lalu, gimana kita extend visibilitynya? Ya get creative. Kita harus sekreatif mungkin untuk cari informasi menggunakan intelligence / informasi yang tersebar di internet menggunakan tools yang ada gitu.

[Information Gathering](https://github.com/sibabiat/pengen-sharing-aja/blob/main/information-gathering.md)

### 2. Exploitation

Eksploitasi ini tahapan yang penting banget sih, dimana di tahap ini yang membedakan proses pentest dan vulnerability assessment. Pada umumnya VA tuh cara kerjanya dia cocoklogi, contoh kalo scanner nemuin ada OS versi 5, ternyata di OS versi 5 ini menurut database si scanner ada vulnerablity. Nah, secara otomatis scanner akan kasih result, 'Vulnerability A at OS versi 5'. Bedanya dengan pentest adalah kita ada proses dimana memvalidasi temuan dari scanner tersebut yaitu dengan menjalakan proses eksploitasi yang dapat dilakukan pada vulnerability tersebut, gitu geng.

Saya gamau terlalu banyak tentang ini, karena kalian pasti jago-jago lah ya.

### 3. Reporting

Reporting atau menulis laporan adalah tahap paling-paling penting dalam proses pentest. Kenapa paling penting? Karena di sini adalah cara kita untuk menkomunikasikan temuan kita. Sederhananya, kalo kita ngomong sama seseorang dan masing-masing dari kita gapaham konteksnya ya akan ga nyambung dan cenderung masuk kuping kanan keluar kuping kiri. Nah makanya kalo report kita ga jelas, ya jangan salahin client atau user kita kalo mereka neglect rekomendasi dari kita, orang kita ngomong aja remed, ibaratnya gitu.

[Reporting](https://github.com/sibabiat/pengen-sharing-aja/blob/main/reporting.md)

## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://id.linkedin.com/in/ijel)<br>
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/iambabiat)

