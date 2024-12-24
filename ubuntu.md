Ubuntu
- sudo apt update && apt upgrade -y
- sudo apt install xrdp
- sudo systemctl restart xrdp
- sudo syatemctl status xrdp (cek apakah xrdp berjalan)
- sudo apt install xfce (jika mau pake xfce bukan gnome)
- sudo ufw enable
- sudo ufw allow 3389/tcp (sesuaikan port dengan yang di gunakan)
- sudo ufw status (untuk cek apa port nya sudah terbuka)
- ip -br a (untuk cek ipv4 untuk remote)

windows
- masuk ke remote desktop connection di windows masukan ip dari linux nya
- masukan username dan passsword linux

note :
- jika pakai vm (virtual machine) pastikan setting network nya bridge adapter agar bisa di remote, contoh ip yang tidak bisa di remote : (10.0.2.15)
- jika saat start xrdp gagal karena port nabrak, rubah port 3389 menjadi : 3390/3391 (command : sudo nano /etc/xrdp/xrdp.ini , rubah di bagian globals dan pilih yang port:3389 menjadi 3390/3391)
- untuk remote di windows dengan tidak memakai port default (contoh pakai port 3390, 192.168.0.100:3390)
 
