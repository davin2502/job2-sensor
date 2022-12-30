Davin Marselon/4.31.20.1.07/TE-3B

# Job 2 Protokol Komunikasi dan Sensor (Capacitive Touch, Sensor DHT, dan Sensor RFID)

## Alat dan Bahan
1. ESP32
2. Arduino IDE (Terinstal ESP32)
3. Library DHT dan Adafruit unified sensor
4. Breadboard
5. Kabel Jumper
6. Resistor < 220Ω
7. LED
8. Sensor DHT
9. RFID
10. Buzzer

## Instalasi ESP-32
1. Buka Arduino IDE
   - Masuk ke Preferences
   - Isikan board url dengan link : https://dl.espressif.com/dl/package_esp32_index.json dan simpan
   - Buka Tools > Board > Boards Manager
   - Cari ESP32, by Espressif. Kemudian instal
   - Pilih flash mode DIO/QIU menyesuaikan
2. Jalankan program .ino
3. Jika terdapat error saat uploading, tekan dan tahan tombol Boot pada ESP32 saat upload, hingga Connecting selesai

## Instalasi DHT & Adafruit Libraries
1. Buka Arduino IDE
2. Buka Sketch > Include Library > Library Manager
3. Cari DHT sensor library by Adafruit, kemudian instal. Atau dapat melalui link DHT Library dan upload pada libraries di direktori projek. Rename direktori menjadi DHT_sensor_library.
4. Instal juga library Adafruit unified sensor by Adafruit. Atau dapat melalui link Adafruit Sensor dan upload pada libraries di direktori projek. Rename direktori menjadi Adafruit_Unified_Sensor.

## Instalasi Servo Libraries
1. Download Servo Library kemudian ekstrak.
2. Masukkan folder ESP32-Arduino-Servo-Library-Master ke dalam libraries projek dan rename menjadi ESP32_Arduino_Servo_Library
3. Buka ulang Arduino IDE.

## Instalasi MFRC522 (RFID) Libraries
1. Buka Arduino IDE
2. Buka Sketch > Include Library > Library Manager
3. Cari MFRC522 by GithubCommunity. Kemudian instal.

## Percobaan A. Capacitive Touch Sensor
### Rangkaian & Instalasi
1. Siapkan ESP32 dan hubungkan ke Arduino IDE.
2. Buat rangkaian berikut.

<img src="https://camo.githubusercontent.com/80e68355e9112a2565e5dcd3c21c4e5e9901ad2f16e4d3a53a6b6128e84e1018/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313433323330363734323636313138302f412e5f52616e676b6169616e5f436170616369746976655f546f7563682e706e67" width=600px>

3. Download dan jalankan kode dari source code sesuai project.
4. Buka serial monitor untuk melihat raw data. Ubah tampilan serial monitor menjadi Serial Plotter pada menu Tools > Serial Plotter untuk menampilkan grafik.

### Keluaran
<img src="https://camo.githubusercontent.com/ed0e554077d8180b6ae31a33ba1583ae1aaaa447129d0dbde0a2b20aaadecc34/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313433353038393036373737383037382f412e5f436170616369746976655f546f7563682e706e67" width=600px>

### Tugas A No. 6
Berdasarkan nilai treshold yang sudah didapatkan yaitu sekitar 25-30, maka pada program dibuat perkondisian jika nilai dibawah treshold maka LED akan menyala dan sebaliknya.

https://user-images.githubusercontent.com/118702169/210024130-a8cfa82f-a96f-4f50-a581-f607685bd79a.mp4

### Tugas A No. 7
Pengembangan dari tugas no. 6, hasil dari LED menyala diubah menjadi blink setiap beberapa ms.

https://user-images.githubusercontent.com/118702169/210024140-d71d7f2d-1ed9-47f3-a16d-319c21e78ee2.mp4

### Tugas A No. 8
Pengembangan dari tugas no. 6, yaitu dengan menambah sebuah variabel hitungan yang akan ditambahkan 1 setiap nilai dibawah treshold.
<img src="https://camo.githubusercontent.com/361ae5a6f65d9267c68fb2c92137ccd90db708df8da8f160f601270dcf9ab83f/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313433383733333632383534373038332f412e5f436170616369746976655f546f7563685f5475676173332e706e67" width=600px>

### Tugas A No. 9
Pengembangan dari tugas no. 6, yaitu dengan mengubah kondisi LED agar menyala secara bergantian hingga satu rotasi penuh saat dibawah nilai treshold dan mematikan seluruh LED saat lebih tinggi dari treshold.

https://user-images.githubusercontent.com/118702169/209097447-11905597-3096-4ebe-a3c1-88b167ae3c08.mp4

## Percobaan B. Sensor DHT
### Rangkaian & Instalasi
1. Siapkan ESP32 dan hubungkan ke Arduino IDE.
2. Buat rangkaian berikut.

<img src="https://camo.githubusercontent.com/aeb8b907f26bfb37d2f21b09f8a41f684a1bc1096c1a1041af71357f6c697b2a/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313434313135343130323637333436392f422e5f52616e676b6169616e5f4448542e706e67" width=600px>

3. Download dan jalankan kode dari source code sesuai project.
4. Pastikan library DHT dan Adafruit sudah terinstal.

### Keluaran
<img src="https://camo.githubusercontent.com/2a5474866f3fce1ce376e1b9268ff3c6122821d748226be2591b290ff7e9073a/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313434313830383534383330323838382f422e5f53656e736f725f4448542e706e67" width=600px>

### Tugas B No. 4
1. Dibawah 30 celcius

https://user-images.githubusercontent.com/118702169/210024219-6dc0e542-d297-4131-8d96-bc3c70deab91.mp4

2. Diatas 30 celcius

https://user-images.githubusercontent.com/118702169/210024233-fa20acd9-7f96-4069-bd78-a411c29c1a12.mp4

## Percobaan C. Sensor RFID
### Rangkaian & Instalasi
1. Siapkan ESP32 dan hubungkan ke Arduino IDE.
2. Buat rangkaian berikut.

<img src="https://camo.githubusercontent.com/d2042014bf4b3666de9acd0d3d28ba5912d03793b2e5a5dac924f3d830793142/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313530343739363635353433313832302f432e5f52616e676b6169616e5f524649442e706e67" width=600px>

3. Download dan jalankan kode dari source code sesuai project.
4. Pastikan library MFRC522 sudah terinstal.

### Keluaran

<img src="https://camo.githubusercontent.com/3ef08546295d0b34447b17d33d886a60057f21a0e79b487fcc6e662b1ed5d188/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313530343833363031343738343532322f432e5f524649442e706e67" width=600px>

https://user-images.githubusercontent.com/118702169/210024253-8ec60746-d690-4aa3-a180-d123b86ff05a.mp4

### Tugas C No. 5
1. Buat rangkaian berikut.
<img src="https://camo.githubusercontent.com/0f11583d6a2b18b9bd4f288f7ece2b5aac882959d6a2c66234bbf945599dfda6/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313530343739373038373433363932312f432e5f52616e676b6169616e5f524649445f5475676173312e706e67" width=600px>

2. Pastikan library servo sudah terinstal.
Setelah identitas kartu RFID didapatkan pada percobaan sebelumnya, maka address dimasukan pada kode sebagai address yang diterima sedangkan address lain akan ditolak. Sehingga didapatkan perkondisian baru. Pada perkondisian ini juga diberikan input LED dan servo.
Saat kartu RFID yang benar dibaca sensor, maka servo akan berputar dan LED menyala hijau. Sebaliknya hanya akan memberikan LED berwarna merah.

https://user-images.githubusercontent.com/118702169/210024259-7120e755-6f77-4210-9e15-8f378b01b8e2.mp4

## Kesimpulan
   - ESP32 kompatibel dengan beberapa sensor seperti DHT dan RFID serta penggerak seperti servo. Akan tetapi, beberapa alat memerlukan library atau tool yang berbeda dengan arduino dan tidak kompatibel dengan ESP. Sehingga perlu melakukan import eksternal.
   - Beberapa pin ESP32 dapat mengukur nilai kapasitif dari pin tersebut. Sehingga dapat diperlakukan seperti touch sensor. Contoh pin yang dimaksud untuk ESP32 v1 adalah pin 21, 22, 24, 12, 13, 16, 17, 18, dan 20.
   - Sensor DHT mampu mengukur suhu dan kelembaban ruangan dan dapat divariasi menjadi satuan celcius maupun farenheit untuk suhunya. Serta terdapat heat index.
   - Sensor RFID mampu membaca chip atau lempengan yang terdapat pada kartu RFID atau pin dan lain sebagainya untuk diterjemahkan menjadi address/alamat. Address tiap kartu bersifat unik dan jarang ada kesamaan, address difungsikan seperti Mac pada perangkat jaringan.
   - Address pada kartu RFID dapat digunakan sebagai identifier kartu sehingga dapat memilah kartu yang akan diberikan akses dan ditolak.
   - Sistem RFID juga digunakan pada e-KTP dan e-Toll namun dengan frekuensi yang berbeda.
   - Perangkat servo dapat bergerak porosnya sejauh 180°. Poros harus digerakan sudut demi sudut.
