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
###Rangkaian & Instalasi
1. Siapkan ESP32 dan hubungkan ke Arduino IDE.
2. Buat rangkaian berikut.
