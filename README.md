# LAB-9-Upgrade-Router-OS-Downgrade-Router-OS-Package-management-extra-packages-Manajemen-Package
tanggal 13 agustus 2025

!

**Siswa mampu melakukan :**
-  Upgrade Router OS  
-  Downgrade Router OS    
-  Package management  
-  extra packages  
-  RouterBOOT
  # Upgrade Router OS  
**A. secara manual**  

    1. sebelum mendownload RouterOS yang baru, lihat dulu arsitektur prosesornya. 
       Cara lihatnya di system > resource > Architecture name,  
       nah disi saya masi mengunakan versi 6.49.13 yang akan upgrade ke versi 7  
    
![i](sem1.PNG)

    2. Setelah tau Arch nya, sekarang bisa download RouterOS nya di mikrotik.com
       Cari versi yang diinginkan dan Arch yang sesuai lalu download. filenya harus ber ekstensi *.npk

![N](sem2.PNG)

    3. jika sudah di download, Buka Windows Explorer, kemudian pada address bar ketikkan ftp://[IP Router]. Contoh ftp://10.46.1.15  
       pas pop up muncul masukan username: admin, pass kosong lalu klik log on.  

![i](sem3.PNG)

    4. copy/drag file RouterOS yang telah didownload tadi dari Windows ke Mikrotik.  

![i](sem4.PNG)

    5. kita akan mengupgrade via winbox, pergi ke Files > upload > cari dan pilih RouterOS yang sudah di download.  
    6. Selanjutnya kita tinggal reboot Mikrotiknya saja klik  System > reboot.
    7. tunggu sampai selesai dan login kembali. maka, akan terlihat di tampilan neighbors bagian version muncul upgrade tdi v7

![i](sem5.PNG)

**A. secara otomatis** 

    1. Pilih menu System -> Packages -> Check For Updates.

![i](hm.PNG)

    2. Router akan menampilkan changelog pada versi tersebut. Pilih Download & install untuk melakukan upgrade.

![i](hm1.PNG)

    3. Pastikan Router sudah terkoneksi ke internet.
    4. Proses download akan berjalan dan tunggu sampai system reboot secara otomatis.
  # Downgrade Router OS  

    1. pastikan file os versi lama masi ada, lalu buka menu system -> packages  
    2. Klik Downgrade, lalu "yes" 

![m](sim8.PNG)

    3. tunggu hingga proses reboot selesai, maka akan masuk kembali dengan versi lama 

![m](versi6.PNG)

   # Package management
   Di MikroTik, paket (package) adalah bagian modular dari RouterOS yang menambahkan fungsi tertentu ke sistem. Setiap fungsi utama di MikroTik — seperti routing, VPN, firewall, wireless, DHCP, hotspot, dll — dikemas dalam bentuk paket. untuk melihat paket,  
masuk ke **system > package**  

      system: Paket inti RouterOS (wajib).    
      advanced-tools: Menyediakan tools tambahan seperti Netwatch, Ping Tool, dll.      
      dhcp: DHCP server dan client.  
      firewall: Fitur firewall (NAT, mangle, dll).    
      hotspot: Mendukung sistem login hotspot.    
      ipv6: Dukungan protokol IPv6.    
      mpls: Fitur MPLS (digunakan untuk ISP).  
      ppp: Protokol PPP, termasuk PPPoE, PPTP, L2TP, SSTP.  
      routing: dukungan routing dinamis (OSPF, BGP, RIP).  
      security: IPsec, SSTP, firewall, dll.  
      ntp: Network Time Protocol (client dan server).  
      wireless: Dukungan perangkat wireless (AP/Client).  
      user-manager: Manajemen pengguna untuk hotspot, PPP, dan lainnya.  
      zerotier: VPN hybrid berbasis cloud.  
      ups: Monitoring UPS (Uninterruptible Power Supply).  
      lte: Dukungan modem LTE/4G.  

![m](a6.PNG)

**Manajemen paket digunakan untuk:**  

     check for update: Mengecek versi terbaru RouterOS dan paket dari MikroTik.    
     enable: Mengaktifkan paket yang sebelumnya dinonaktifkan (jika didukung). Tidak semua paket bisa dinonaktifkan.     
     disable: Menonaktifkan paket tanpa menghapusnya (jarang digunakan). Tidak semua paket bisa dinonaktifkan.  
     uninstall: Menghapus paket opsional dari RouterOS. Paket inti tidak bisa dihapus.  
     unschedule: Membatalkan jadwal update otomatis RouterOS (jika ada).  
     downgrade: Menurunkan versi RouterOS dan paket ke versi sebelumnya (jika tersedia).  
     check installation: Memverifikasi apakah paket sudah terinstal dan berfungsi dengan baik.  

   # extra packages 

   1. untuk mendapatkan ektra packages mikrotiknya kita bisa unduh file tersebut pada kedua alamat website ini,  
      https://mikrotik.com/download/archive dan https://mikrotik.com/download   
      pilih paket sesuai dengan versi router os yang anda miliki.

![m](a1.PNG)

   3. jika sudah terdownload, Untuk menginstall nya ke winbox buka file explorer masukan (ftp://[ip mikrotik]) lihat seperti yang di gambar lalu klik log on
      copy kan, dan paste tunggu hingga beres.

![m](A2.PNG)

![m](A2.PNG)

   4. Nah setelah diupload dan berhasil, file tersebut secara otomatis akan muncul di tab file list.

![m](a4.PNG)
     
   5. Untuk menerapkan instalasi/kofigurasi, kita bisa lakukan reboot, pilih system > reboot
**sebelum Reboot :**

![m](a01.PNG)

    6. Setelah proses reboot selesai, kita masuk lagi mikrotiknya melalui winbox, dan cek packages list nya, apakah bertambah?, nah setelah proses penamabahan paket berhasil, paket list        nya akan bertambah contoh pertama tadi 11 list menjadi 23.

![m](02.PNG)
      



  
   # RouterBOOT

