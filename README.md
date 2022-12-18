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
<img src="https://camo.githubusercontent.com/80e68355e9112a2565e5dcd3c21c4e5e9901ad2f16e4d3a53a6b6128e84e1018/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313433323330363734323636313138302f412e5f52616e676b6169616e5f436170616369746976655f546f7563682e706e67" width=425px>
3. Download dan jalankan kode dari source code sesuai project.
4. Buka serial monitor untuk melihat raw data. Ubah tampilan serial monitor menjadi Serial Plotter pada menu Tools > Serial Plotter untuk menampilkan grafik.

### Keluaran
![](https://camo.githubusercontent.com/ed0e554077d8180b6ae31a33ba1583ae1aaaa447129d0dbde0a2b20aaadecc34/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313433353038393036373737383037382f412e5f436170616369746976655f546f7563682e706e67)

### Tugas A No. 6
Berdasarkan nilai treshold yang sudah didapatkan yaitu sekitar 25-30, maka pada program dibuat perkondisian jika nilai dibawah treshold maka LED akan menyala dan sebaliknya.
![](https://user-images.githubusercontent.com/49542850/206910388-c3ed11f1-e69b-497a-b94f-da8c62d86bd3.mp4)

### Tugas A No. 7
Pengembangan dari tugas no. 6, hasil dari LED menyala diubah menjadi blink setiap beberapa ms.
![](https://user-images.githubusercontent.com/49542850/206910388-c3ed11f1-e69b-497a-b94f-da8c62d86bd3.mp4)

### Tugas A No. 8
Pengembangan dari tugas no. 6, yaitu dengan menambah sebuah variabel hitungan yang akan ditambahkan 1 setiap nilai dibawah treshold.
![](https://camo.githubusercontent.com/361ae5a6f65d9267c68fb2c92137ccd90db708df8da8f160f601270dcf9ab83f/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313433383733333632383534373038332f412e5f436170616369746976655f546f7563685f5475676173332e706e67)

### Tugas A No. 9
Pengembangan dari tugas no. 6, yaitu dengan mengubah kondisi LED agar menyala secara bergantian hingga satu rotasi penuh saat dibawah nilai treshold dan mematikan seluruh LED saat lebih tinggi dari treshold.
![](https://user-images.githubusercontent.com/49542850/206910407-c9387493-d962-4701-8f93-8dfe24f04473.mp4)

## Percobaan B. Sensor DHT
### Rangkaian & Instalasi
1. Siapkan ESP32 dan hubungkan ke Arduino IDE.
2. Buat rangkaian berikut.
<img src="https://camo.githubusercontent.com/aeb8b907f26bfb37d2f21b09f8a41f684a1bc1096c1a1041af71357f6c697b2a/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313434313135343130323637333436392f422e5f52616e676b6169616e5f4448542e706e67" width=425px>
3. Download dan jalankan kode dari source code sesuai project.
4. Pastikan library DHT dan Adafruit sudah terinstal.

### Keluaran
![](https://camo.githubusercontent.com/2a5474866f3fce1ce376e1b9268ff3c6122821d748226be2591b290ff7e9073a/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313434313830383534383330323838382f422e5f53656e736f725f4448542e706e67)

### Tugas B No. 4
1. Dibawah 30 celcius

![](https://user-images.githubusercontent.com/49542850/206898685-5073100e-5814-4451-b6bf-74e835e68ad8.mp4)

3. Diatas 30 celcius

![](https://user-images.githubusercontent.com/49542850/206898713-3ffcd6a4-ea9f-4853-8dfc-1a232c3f6ccf.mp4)

## Percobaan C. Sensor DHT
### Rangkaian & Instalasi
1. Siapkan ESP32 dan hubungkan ke Arduino IDE.
2. Buat rangkaian berikut.
<img src="https://camo.githubusercontent.com/d2042014bf4b3666de9acd0d3d28ba5912d03793b2e5a5dac924f3d830793142/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313530343739363635353433313832302f432e5f52616e676b6169616e5f524649442e706e67" width=425px>
3. Download dan jalankan kode dari source code sesuai project.
4. Pastikan library MFRC522 sudah terinstal.

### Keluaran
![](https://camo.githubusercontent.com/3ef08546295d0b34447b17d33d886a60057f21a0e79b487fcc6e662b1ed5d188/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313530343833363031343738343532322f432e5f524649442e706e67)

![](https://user-images.githubusercontent.com/49542850/206910208-4912f5ef-f3ea-4ebc-94e4-2878b3abd4db.mp4)

### Tugas C No. 5
1. Buat rangkaian berikut.
<img src="https://camo.githubusercontent.com/0f11583d6a2b18b9bd4f288f7ece2b5aac882959d6a2c66234bbf945599dfda6/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313530343739373038373433363932312f432e5f52616e676b6169616e5f524649445f5475676173312e706e67" width=425px>

2. Pastikan library servo sudah terinstal.
Setelah identitas kartu RFID didapatkan pada percobaan sebelumnya, maka address dimasukan pada kode sebagai address yang diterima sedangkan address lain akan ditolak. Sehingga didapatkan perkondisian baru. Pada perkondisian ini juga diberikan input LED dan servo.
Saat kartu RFID yang benar dibaca sensor, maka servo akan berputar dan LED menyala hijau. Sebaliknya hanya akan memberikan LED berwarna merah.
![](https://user-images.githubusercontent.com/49542850/206910214-d9e4f235-cc73-4322-b5b0-337dbce9be23.mp4)
