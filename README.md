# Jarkom_Modul1_Lapres_B4

Naufal Fajar Imani             05111940000007

Jundullah H. R.                05111940000144

Yeremia D Limantara            05111940000232

## 1. Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! #
Masukkan filter ```ip.addr==167.172.77.139 and http.server != ''``` . lalu pilih paket yang mana saja, dan lihat informasi (tcp stream) paket pada http.
![no1](https://user-images.githubusercontent.com/81339649/134804813-4393054c-3a4f-4f1b-a776-1c17fad104f1.png)

## 2. Temukan paket dari web-web yang menggunakan basic authentication method! #
Masukkan filter ```http.authbasic``` .
![no2](https://user-images.githubusercontent.com/81339649/134805003-06875b96-5609-495e-a2c0-f529f608d84f.png)

![no2 2](https://user-images.githubusercontent.com/81339649/134804957-9a3e7bb2-b4eb-4dd1-8a56-f0513e25aeb9.png)

## 3. Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng! #
 Buka webnya, lalu akan dimintai auth. Untuk mendapatkan basic auth, kemali ke wireshark dan masukkan display filter ```ip.addr==167.172.77.139 and http.authbasic``` . Lihat pada kolom tengah bagian http authorization akan terdapat credentials. Lalu kerjakan soal yang diberikan dari web tadi setelah masuk.
![no3](https://user-images.githubusercontent.com/81339649/134805009-6e532c35-77be-47c3-8179-cc35bf07eb28.png)

![no3 2](https://user-images.githubusercontent.com/81339649/134805015-32b0af6a-05ab-46bb-a0a4-bc7a27eb3d40.png)
## 4. Temukan paket mysql yang mengandung perintah query select! #
Masukkan filter ```mysql.query matches select```.
![no4](https://user-images.githubusercontent.com/81339649/134805024-dc4227f7-8068-42a8-9446-0ae269c9d292.png)
## 5. Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap! #
Masukkan filter ```mysql.query matches insert```.
![no5](https://user-images.githubusercontent.com/81339649/134805031-ba85bcdb-f943-4430-8638-255e6f4a0180.png)

![no5 2](https://user-images.githubusercontent.com/81339649/134805039-7e29bf1b-d33f-40ef-b5a4-a38684db5523.png)
## 6. Cari username dan password ketika melakukan login ke FTP Server! #
Masukkan filter ```ftp.request.command matches user or ftp.request.command matches pass```.
![no6](https://user-images.githubusercontent.com/81339649/134805051-a09e6fae-c3ec-4e0d-867d-d70c2a9bafec.png)
## 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf") #
Masukkan filter ```ftp-data.command contains .zip and ftp-data contains Real.pdf```.
![no7](https://user-images.githubusercontent.com/81339649/134805056-b9dcd6f4-fc8b-464b-8c18-90a0e56f2201.png)
## 8. Cari paket yang menunjukan pengambilan file dari FTP tersebut! #
Masukkan filter ```ftp.request.command matches retr```.
![no8](https://user-images.githubusercontent.com/81339649/134805064-1c5c2ed6-0b41-4ac9-aa58-0a91db12ff7a.png)
## 9. Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut! #
Masukkan filter ```ftp-data.command contains secret```.
![no9](https://user-images.githubusercontent.com/81339649/134805080-631930da-6766-4263-afc4-369215a087da.png)
## 10 .Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"! #
Masukkan filter ```ftp-data.command contains history```
![no10](https://user-images.githubusercontent.com/81339649/134805105-0191b441-68d8-4fbc-b951-5c58e97232f6.png)

Masukkan filter ```ftp-data.command contains bukanapaapa.txt```
![no10 2](https://user-images.githubusercontent.com/81339649/134805123-ad2cb932-31a9-4eb7-a75a-2eebcd2297eb.png)

## 11. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!  #
Masukkan filter ```src port 80```.
![no11](https://user-images.githubusercontent.com/81339649/134805135-78b004ac-5112-4eac-a228-38cab156dd79.png)

## 12. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21! #
Masukkan filter ```tcp.port==21```.
![no12](https://user-images.githubusercontent.com/81339649/134805141-046d590f-41ac-4c92-ba92-c3e5a3e6851b.png)

## 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443! #
Masukkan filter ```dst port 443```.
![no13](https://user-images.githubusercontent.com/81339649/134805148-581264ae-d97f-4ed8-b57a-fc773285b272.png)
![no13 2](https://user-images.githubusercontent.com/81339649/134805146-ccf7b883-217f-4858-9601-077feb0b363e.png)

## 14. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id! #
Masukkan filter ```dst host  103.7.13.247 ```(ip kemenag.go.id).
![no13 2](https://user-images.githubusercontent.com/81339649/134805146-ccf7b883-217f-4858-9601-077feb0b363e.png)

## 15. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian! #
Masukkan filter ```src host 192.168.1.2```(ip yeremia).
![no15](https://user-images.githubusercontent.com/81339649/134805162-fc25b755-ac17-47b3-84ed-05b13038c825.png)

## Kendala #
  - Indihom/telkom lemottt


