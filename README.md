# Jarkom_Modul1_Praktikum_B05
- Elvira Catrine Natalie (05111840000016)
- Vania Meilani Taqiyyah (05111840000045)

## A. Display Filter
#### 1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
- Request dengan `http.host == "testing.mekanis.me"`
- Klik salah satu paket yang ada, klik kanan pilih Follow HTTP Stream
<img src="https://user-images.githubusercontent.com/61219556/96326925-ff3ba000-105e-11eb-990b-0b06bb16ee54.png" width="500" height="auto">
Web Server nya adalah `nginx` 

#### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
- Klik File, lalu pilih Export Objects HTTP.
- Cari gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg", lalu klik file gambar dan save.
<img src="https://user-images.githubusercontent.com/61219556/96327425-a91d2b80-1063-11eb-8c91-a170c91452b4.jpg" width="500" height="auto">

#### 3. Cari username dan password ketika login di "ppid.dpr.go.id"!
- Ketik di Display Filter dengan `http.request.method==POST`
- Akan muncul 1 paket, lalu klik `HTML Form URL Encoded: application/x-www-form-urlencoded`. Maka disitu akan muncul username dan password yang dicari.
<img src="https://user-images.githubusercontent.com/61219556/96327643-94419780-1065-11eb-882f-94d073c84220.PNG" width="500" height="auto">

#### 4. Temukan paket dari web-web yang menggunakan basic authentication method!
Ketik pada Display Filter dengan `http.authbasic`.

<img src="https://user-images.githubusercontent.com/61219556/96327884-edaac600-1067-11eb-9074-b0b077d8aae6.PNG" width="500" height="auto">

#### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
- ketik pada Display Filter `ip.dst==157.245.50.224&&http`.
- Pilih salah satu paket yang muncul. Kemudian, pilih Hypertext Transfer Protocol.
- Pilih pada bagian Authorization. Disitu akan muncul username dan password untuk login pada `aku.pengen.pw`.
<img src="https://user-images.githubusercontent.com/61219556/96328085-88f06b00-1069-11eb-8be5-4b7fe548e450.PNG" width="500" height="auto">

- Setelah login, web akan menampilkan halaman berupa soal seperti di bawah ini 
<img src="https://user-images.githubusercontent.com/61219556/96328239-dcaf8400-106a-11eb-93e0-0a93e52548a3.PNG" width="500" height="auto">

#### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
- Ketik pada Display Filter dengan `ftp-data`. 
- Klik ctrl+f untuk mencari `Answer.zip`. Lalu, klik kanan untuk pilih follow TCP stream.
- Pada "show and save data as" ganti dengan `raw`. Lalu, save as `Answer.zip`. 
- Tahap-tahap diatas sama halnya dalam pencari file `zipkey.txt`. Buka file tersebut dan menampilkan isi password untuk meng-ekstrak folder `Answer.zip`.
<img src="https://user-images.githubusercontent.com/61219556/96352048-8f72f700-10ea-11eb-9304-3a829a5ecf5b.PNG" width="500" height="auto">

Setelah berhasil diekstrak, lalu buka file `Open This.pdf`. Hasilnya sebagai berikut 

<img src="https://user-images.githubusercontent.com/61219556/96352116-090ae500-10eb-11eb-95de-25ad8d79e5a6.png" width="500" height="auto">

#### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf".
- Ketik pada Display Filter dengan `ftp-data && frame contains "Yes.pdf"`.
<img src="https://user-images.githubusercontent.com/61219556/96352161-62731400-10eb-11eb-8392-540b6dd9ef6d.PNG" width="500" height="auto">

- Pilih salah satu folder zip, lalu klik kanan untuk pilih follow TCP stream.
- Pada "show and save data as" ganti dengan `raw`. Lalu, save as `473.zip`. 
- Ekstrak zip tersebut lalu buka file `Yes.pdf` dan hasilnya sebagai berikut 
<img src="https://user-images.githubusercontent.com/61219556/96352240-e2997980-10eb-11eb-84ab-bb4425a5a299.PNG" width="500" height="auto">

#### 8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
- Ketik pada Display Filter dengan `ftp contains "Microsoft"` untuk mendapatkan IP address dari Microsoft FTP Service.
<img src="https://user-images.githubusercontent.com/61219556/96352269-37d58b00-10ec-11eb-9fa8-3c4a92f2f7de.PNG" width="500" height="auto">

- Pilih IP bagian destination, lalu ketik kembali pada Display Filter untuk mencari objek apa saja yang didownload menggunakan `RETR`. Hasilnya seperti berikut 
<img src="https://user-images.githubusercontent.com/61219556/96352369-c2b68580-10ec-11eb-849b-3a8972aef9bb.PNG" width="500" height="auto">

#### 9. Cari username dan password ketika login FTP pada localhost!
Ketik pada Display Filter dengan `ftp.request.command==PASS || ftp.request.command==USER`. Lalu, akan muncul paket-paket dengan isi username dan password saat login FTP pada localhost.

<img src="https://user-images.githubusercontent.com/61219556/96328451-62343380-106d-11eb-9daf-37ed212a6a3b.PNG" width="500" height="auto">

#### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46".
- Ketik pada Display Filter dengan `http contains".pdf"`
<img src="https://user-images.githubusercontent.com/61219556/96352440-5b4d0580-10ed-11eb-9d2a-fe4245b3200d.PNG" width="500" height="auto">

- Klik ctrl+f untuk ketik clue `25 50 44 46`. Lalu, klik kanan untuk pilih follow TCP stream.
- Pada "show and save data as" ganti dengan `raw`. Lalu, save as `1759.pdf`. Setelah file dibuka akan menampilkan sebagai berikut
<img src="https://user-images.githubusercontent.com/61219556/96352485-a9fa9f80-10ed-11eb-94bc-9c9ceaa73d00.PNG" width="500" height="auto">

## B. Capture Filter
#### 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
#### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
#### 13.Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
#### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
#### 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
