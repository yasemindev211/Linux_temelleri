5) Linux Temelleri
 1. Terminal Komutları

Terminal, Linux’un kalbidir. Grafik arayüzden çok daha güçlüdür.

Temel Komutlar

 Dosya & Klasör:

ls        # klasördeki dosyaları gösterir
cd klasor # klasöre girer
pwd       # bulunduğun yeri gösterir
mkdir test  # klasör oluşturur

Dosya işlemleri:

cp a.txt b.txt   # kopyala
mv a.txt b.txt   # taşı / yeniden adlandır
rm a.txt         # sil (dikkat!)
🔍 Arama (grep)
grep "kelime" dosya.txt

 Dosyada geçen kelimeleri bulur

ls | grep ".txt"

 Sadece .txt dosyalarını filtreler

 Yetki değiştirme (chmod)
chmod 755 script.sh

 Dosyaya çalıştırma izni verir

 Sistem izleme (top)
top

 Anlık CPU / RAM kullanımı gösterir
Alternatif: htop (daha görsel)

 2. Paket Yönetimi

Linux’ta programlar “paket yöneticisi” ile kurulur.

 Debian / Ubuntu

APT

sudo apt update
sudo apt install nginx
 Arch Linux

pacman

sudo pacman -S nginx
 Fedora / RedHat

DNF

sudo dnf install nginx

 Mantık aynı:

paket bul
indir
kur
güncelle
 3. Dosya İzinleri

Linux’ta her dosyanın 3 tür yetkisi vardır:

r (read) → okuma
w (write) → yazma
x (execute) → çalıştırma
Örnek:
-rwxr-xr-x

Bu şu demek:

sahibi: her şeyi yapabilir
grup: okur + çalıştırır
diğerleri: okur + çalıştırır
 Sayısal karşılık:
7 = rwx
6 = rw-
5 = r-x
chmod 755 dosya.sh
⚙️ 4. Servisler (systemctl)

Linux’ta arka planda çalışan şeylere servis denir
(örnek: web server, veritabanı)

Bunları yönetmek için:

systemctl

sudo systemctl start nginx     # başlat
sudo systemctl stop nginx      # durdur
sudo systemctl restart nginx   # yeniden başlat
sudo systemctl status nginx    # durumunu gör
Otomatik başlatma:
sudo systemctl enable nginx
 Genel Mantık

Linux şu mantıkla çalışır:

Her şey bir dosyadır
Küçük komutları birleştirirsin
Terminal = kontrol merkezi
Yetki sistemi = güvenlik
 Kazanç

Bu konuları öğrendiğinde:

✔ Sunucu yönetebilirsin
✔ Yazılım projelerini rahat çalıştırırsın
✔ DevOps / Backend için temel atmış olursun
✔ SSH ile uzak makineleri kontrol edebilirsin