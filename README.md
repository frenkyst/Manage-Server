# Manage-Server

### Definisi Terminal

Terminal merupakan command line atau barisan perintah untuk mengoperasikan sistem operasi tidak seperti sistem kebanyakan yang digunakan orang awam atau end user yang menggunakan GUI atau perintah dengan mengeklik tombol yang di gunakan untuk menjalankan perintah yang di inginkan pengguna terminal lebih berupa perintah sederhana yang ditulis secara langsung ke terminal tersebut.

Keuntungan menggunakan Terminal

- Lebih ringan dalam penggunaan resource perangkat
- Lebih mudah dalam melakukan automasi
- Pengoperasian bisa lebih cepat

### Command untuk text manipulation

1. __cat__ digunakan untuk menampilkan isi file ke terminal

        cat (name-file)

      ![image](https://user-images.githubusercontent.com/40049149/187897542-3973d1c1-0aec-402f-bb19-ff01e377372c.png)
      
        cat > kata1

      untuk membuat suatu file dan juga memasukan text di file tersebut (Ctrl + C jika sudah)
      
      ![image](https://user-images.githubusercontent.com/40049149/187905757-ba7b3ee8-c75e-4907-aa8c-752b704c2cbf.png)
      
        cat kata kata1 > kata2
        
      untuk menggabungkan teks dari file 1 dan file 2 ke dalam file yang ke 3
      
      ![image](https://user-images.githubusercontent.com/40049149/187906698-8cbe94a5-69da-4121-b3e9-2bc7f79eccca.png)
      
      

2. __sed__ digunakan untuk mereplace suatu text dalam file

        sed -i 's/made/make/g' kalimat

      ![image](https://user-images.githubusercontent.com/40049149/187898054-eaebda23-c214-415e-b3df-eb0483f94630.png)

3. __grep__ digunakan untuk mencari suatu text dalam file

        grep make kalimat
        
      akan mencari kata __make__ pada file __kalimat__

      ![image](https://user-images.githubusercontent.com/40049149/187898414-5157294e-8d68-4751-a65a-62d080fb65f2.png)

        grep -c make kalimat
        
      akan menghitung kata __make__ pada file __kalimat__

      ![image](https://user-images.githubusercontent.com/40049149/187900968-9f4fd45b-5102-45d7-801b-ec114e00aa93.png)

        grep make *

      akan mencari kata __make__ pada semua file yang berada di forder tersebut

      ![image](https://user-images.githubusercontent.com/40049149/187901676-60f8a5c5-3c51-4019-b5bc-b8e5e3c8dea0.png)

4. __sort__ digunakan untuk mengurutkan text

        sort nomor

      ![image](https://user-images.githubusercontent.com/40049149/187901973-e138fe91-b894-421b-9676-cc41fcf80d1e.png)

        sort -r nomor
      
      untuk mengurutkan dari yang terbesar
      
      ![image](https://user-images.githubusercontent.com/40049149/187902082-716dbed1-5adf-4f0f-9623-fce7a2acfaf1.png)

5. __echo__ digunakan untuk menampilkan text pada terminal

        echo "Hello Wed!"

      untuk mencetak kata __Hello Wed!__ di terminal
      
      ![image](https://user-images.githubusercontent.com/40049149/187903939-37c2474d-b75d-4a6a-a236-3b520f180a4d.png)

        echo "Hello Wed2!" >> kata

      untuk menambahkan kata __Hello Wed2!__ di file __kata__
      
      ![image](https://user-images.githubusercontent.com/40049149/187904258-4f90f40b-0a01-49b3-900f-3cbecc23e8b4.png)

        echo "timpa semua kata" > kata
        
      untuk menimpa semua kata/kalimat yang ada di file __kata__
      
      ![image](https://user-images.githubusercontent.com/40049149/187904496-66a02853-b07a-4fa4-bc26-846c5bb27ba4.png)


### Monitoring

Monitoring merupakan aktivitas untuk melihat kinerja sistem secara realtime. Berikut ini adalah beberapa perintah yang dapat kita gunakan untuk memonitoring sebuah server.

- htop
- nmon
- lsof
- ps

Kenapa perlu Monitoring ?​

- Untuk mengetahui apakah ada server down atau tidak.
- Untuk mengetahui resource dari server tersebut apakah penuh atau tidak.
- Untuk mengetahui tentang aplikasi yang berada di server kita itu jalan atau tidak, ataupun sudah up to date atau belum.



__htop__ merupakan perintah untuk memonitoring sistem, kita dapat melihat penggunaan memory, cpu, swap. Berikut adalah contoh penggunaan :

        htop
        
Jika pada server kalian belum terinstall, maka dapat menjalankan perintah beriku:

        sudo apt install htop -y
        htop
        
![image](https://user-images.githubusercontent.com/40049149/187908892-3ec5a8d3-c5b0-4d76-b71f-e6daf3f08b25.png)

Keterangan :

- CPU adalah berapa jumlah core yang kita miliki.
- Mem adalah total penggunaan memory.
- Swp adalah Memory cadangan.
- Tasks adalah aplikasi yang sedang berjalan di server.
- Load average adalah rata-rata aplikasi yang berjalan.
- Uptime adalah berapa lama server kita hidup.
- PID adalah nomor proses id setiap proses yang berjalan di linux.
- VIRT adalah memory yang terpakai.
- Command adalah perintah apa yang sedang di jalankan.


### nmon

__nmon__ sama halnya dengan htop digunakan untuk memonitoring kinerja dari server

Pada tampilan awal terdapat beberapa pilihan yang dapat kita gunakan, berikut hanyalah contoh penggunaannya :

Untuk instalasi nmon dapat menggunakan perintah berikut :

        sudo apt install nmon

![image](https://user-images.githubusercontent.com/40049149/187909328-f7cb7083-8354-46f9-96ed-399b1f2ebcfe.png)

Untuk menjalankan nmon kalian dapat menggunakan perintah dibawah ini

        nmon

![image](https://user-images.githubusercontent.com/40049149/187909380-32494949-1175-43c1-a1da-cf069ba33dbd.png)

Keterangan : Disini kita dapat memilih ingin memonitoring apa saja, Disini kita coba saja untuk menampilkan beberapa saja.

- c adalah CPU
- m adalah Memory
- d adalah Disk
- n adalah network

Berikut adalah tampilan dari nmon untuk menampilkan cpu, memory, disk, dan network

![image](https://user-images.githubusercontent.com/40049149/187909725-0d54874f-1676-48f8-9da6-4b90f0459a23.png)


### lsof​

__Lsof__ merupakan singkatan list open files, berfungsi untuk melihat seluruh file yang terbuka berdasarkan proses aktif yang berjalan di sistem.

Berikut adalah contoh penggunaan :

        lsof

![image](https://user-images.githubusercontent.com/40049149/187910128-6c2bea6f-5edb-4d10-95a6-b6e4dfe8b5f9.png)

keterangan : untuk menampilkan seluruh proses

        lsof -u (your-user)

![image](https://user-images.githubusercontent.com/40049149/187910183-24737bd5-102e-4c8b-8eac-e02383c8014d.png)

keterangan : menampilkan proses yang dilakukan oleh user “your-user”

        lsof -i :80

image1

keterangan : untuk menampilkan proses yang menggunakan port 80

### ps​

__Ps__ merupakan singkatan dari process status, untuk mengetahui daftar proses yang berjalan pada sistem.

Berikut adalah contoh penggunaan :

        ps -f -u (your-user)
        
![Screenshot from 2022-09-01 19-12-38](https://user-images.githubusercontent.com/40049149/187912074-94775849-ab33-4aa5-9490-9d2daf0128cd.png)

keterangan : untuk menampilkan proses pada user “your-user”

        ps -aux

![Screenshot from 2022-09-01 19-12-53](https://user-images.githubusercontent.com/40049149/187911840-be5ae84a-0cc4-41c8-a3ac-d85bd727393e.png)

keterangan : untuk menampilkan seluruh proses secara lengkap

### Bash

Script bash untuk update dan upgrade
1. Buat file baru dengan nama __autoupdate.sh__(bebas) dan isikan berikut

        #!/bin/bash

        sudo apt-get -y update
        sudo apt-get -y upgrade

![image](https://user-images.githubusercontent.com/40049149/187913821-9f6ead19-b5bd-4886-a07d-4e218e5742c1.png)

2. Tambahkan permission execute di file yang kita buat tadi __autoupdate.sh__ dengan command chmod

        chmod +x autoupdate.sh
        ls -l

![image](https://user-images.githubusercontent.com/40049149/187914189-2afc4c59-5402-436c-bfbd-f099fe4972c4.png)

3. Jalankan script dengan command berikut

        ./autoupdate.sh
        atau
        bash autoupdate.sh

![image](https://user-images.githubusercontent.com/40049149/187914424-5613bb29-b5fc-4952-ac43-b706eefd7ac5.png)







