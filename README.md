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













