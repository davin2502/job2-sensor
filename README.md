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
<img src="https://camo.githubusercontent.com/ed0e554077d8180b6ae31a33ba1583ae1aaaa447129d0dbde0a2b20aaadecc34/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313034333436323531393333363939363839342f313035313433353038393036373737383037382f412e5f436170616369746976655f546f7563682e706e67" width=425px>
<img src="" width=425px>
<img src="" width=425px>
<img src="" width=425px>
<img src="" width=425px>
<img src="" width=425px>
<img src="" width=425px>
<img src="" width=425px>
<img src="" width=425px>
