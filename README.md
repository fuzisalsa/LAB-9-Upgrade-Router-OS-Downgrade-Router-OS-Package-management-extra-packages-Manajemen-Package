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
       nah disi saya masi mengunakan versi 6.49.23 yang akan upgrade ke versi 7  
    
!

    2. Setelah tau Arch nya, sekarang bisa download RouterOS nya di mikrotik.com
       Cari versi yang diinginkan dan Arch yang sesuai lalu download. filenya harus ber ekstensi *.npk

!

    3. jika sudah di download, Buka Windows Explorer, kemudian pada address bar ketikkan ftp://[IP Router]. Contoh ftp://10.46.1.15  
       pas pop up muncul masukan username: admin, pass kosong lalu klik log on.  
    4. copy/drag file RouterOS yang telah didownload tadi dari Windows ke Mikrotik.  
    5. kita akan mengupgrade via winbox, pergi ke Files > upload > cari dan pilih RouterOS yang sudah di download.  
    6. Selanjutnya kita tinggal reboot Mikrotiknya saja klik  System > reboot.
    7. tunggu sampai selesai dan login kembali. maka, akan terlihat di tampilan neighbors bagian version muncul upgrade tdi v7

!

**A. secara otomatis** 

    1. Pilih menu System -> Packages -> Check For Updates.

!

    2. Router akan menampilkan changelog pada versi tersebut. Pilih Download & install untuk melakukan upgrade.

!

    3. Pastikan Router sudah terkoneksi ke internet.
    4. Proses download akan berjalan dan tunggu sampai system reboot secara otomatis.
  # Downgrade Router OS  

    1. pastikan file os versi lama masi ada, lalu buka menu system -> packages
    2. Klik Downgrade, lalu "yes" 
    3. tunggu hingga proses reboot selesai, maka akan masuk kembali dengan versi lama 

