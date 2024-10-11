# Setting-MikroTik
1. Membuka MikroTik di WinBox
Buka aplikasi dan login melalui WinBox dengan klik bagian Mac Address.
Isi login: admin dan kata sandi: [kosong], lalu klik Connect.
2. Mengatur DHCP Client Ether1
Bila telah berhasil login konfigurasi sebelumnya, pilih menu IP → DHCP Client → klik ikon tambah (+) → isi form interface: ether1.
Kemudian, hilangkan ceklis pada Use Peer DNS yang artinya MikroTik tidak akan memakai DNS bawaan dari ISP, lalu pilih Apply → OK.
3. Tes Ping Internet
buka menu New Terminal → ketik ping google.com lalu klik Enter.
4. Setting IP Address Ether2
klik tambah (+) pada menu IP Addresses.
Dialog baru akan muncul, Anda dapat mengisinya dengan IP address beserta prefiksnya (…/24) pada form Address dan pilih Interface: ether2, lalu pilih Apply → OK.
5. Setting DNS MikroTik
masuk kembali ke menu IP → DNS → isi pada kolom Servers: 8.8.8.8 dan 8.8.4.4, kemudian beri ceklis pada Allow Remote Requests dan klik Apply → OK.
6. Setting NAT MikroTik
Selanjutnya, klik Firewall pada menu IP → NAT → tambah (+) → kemudian isi form Chain: srcnat dan Out. Interface: ether1.
Jika sudah, pada tab Action klik Action: masquerade dan pilih Apply → OK
7. Setting DHCP Server MikroTik
masuk pada IP → DHCP Server → klik menu DHCP Setup yang berada di atas.
Pilih Interface ether2 → Next.
Pilih DHCP Address Space, pada langkah ini, form tersebut akan terisi secara otomatis → Next.
Tentukan gateway yang dibutuhkan, tahapan ini juga terisi otomatis oleh IP Address ether2 → Next.
Tentukan IP pool yang nantinya akan dipakai oleh client, serta terisi otomatis sesuai hosts pada prefiks yang digunakan, misalnya 192.168.1.2 → Next.
Kemudian, isi DNS Google: 8.8.8.8 dan 8.8.4.4 → Next.
Terakhir pada cara setting MikroTik yakni menentukan Lease Time → Next yang merupakan berapa lama IP address akan diakses oleh pengguna
