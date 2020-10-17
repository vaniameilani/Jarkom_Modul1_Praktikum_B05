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
- Ketik di Filter Display dengan `http.request.method==POST`
- Akan muncul 1 paket, lalu klik `HTML Form URL Encoded: application/x-www-form-urlencoded`. Maka disitu akan muncul username dan password yang dicari.
<img src="https://user-images.githubusercontent.com/61219556/96327643-94419780-1065-11eb-882f-94d073c84220.PNG" width="500" height="auto">

#### 4. Temukan paket dari web-web yang menggunakan basic authentication method!
Ketik pada Filter Display dengan `http.authbasic`
<img src="https://user-images.githubusercontent.com/61219556/96327884-edaac600-1067-11eb-9074-b0b077d8aae6.PNG" width="500" height="auto">

#### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
- ketik pada Filter Display `ip.dst==157.245.50.224&&http`.
- Pilih salah satu paket yang muncul. Kemudian, pilih Hypertext Transfer Protocol.
- Pilih pada bagian Authorization. Disitu akan muncul username dan password untuk login pada `aku.pengen.pw`.
