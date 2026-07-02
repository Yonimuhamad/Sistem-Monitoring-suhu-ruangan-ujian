# Sistem Monitoring Suhu dan Kelembaban Ruangan Ujian

## Deskripsi Proyek
Proyek ini merupakan sistem monitoring suhu dan kelembaban ruangan ujian berbasis ESP32, sensor DHT22, aktuator LED dan buzzer, serta platform IoT Blynk. Sistem ini dibuat untuk memantau kondisi ruangan secara real-time dan memberikan peringatan apabila suhu atau kelembaban melewati batas yang ditentukan.

## Komponen yang Digunakan
- ESP32 DevKit V1
- Sensor DHT22
- LED Hijau
- LED Merah
- Buzzer
- Blynk IoT
- Wokwi Simulator

## Platform
- Simulator: Wokwi
- Platform IoT: Blynk
- Protokol IoT: Blynk melalui koneksi WiFi

## Pin Komponen
| Komponen | Pin ESP32 |
|---|---|
| DHT22 | GPIO 15 |
| LED Hijau | GPIO 26 |
| LED Merah | GPIO 27 |
| Buzzer | GPIO 25 |

## Datastream Blynk
| Virtual Pin | Fungsi |
|---|---|
| V0 | Suhu |
| V1 | Kelembaban |
| V2 | Status Bahaya |
| V3 | Status Alarm |
| V4 | Kontrol Alarm |
| V5 | Status Teks |

## Logika Sistem
- Jika suhu <= 30°C dan kelembaban <= 70%, maka status ruangan AMAN.
- Jika suhu > 30°C atau kelembaban > 70%, maka status ruangan TIDAK AMAN.
- Saat kondisi aman, LED hijau menyala dan buzzer mati.
- Saat kondisi tidak aman, LED merah menyala dan buzzer aktif jika alarm dinyalakan.
- Data suhu, kelembaban, dan status sistem dikirim ke dashboard Blynk secara real-time.

## Cara Menjalankan
1. Buka project di Wokwi.
2. Masukkan Template ID, Template Name, dan Auth Token Blynk pada kode program.
3. Jalankan simulasi di Wokwi.
4. Buka dashboard Blynk.
5. Ubah nilai suhu atau kelembaban pada sensor DHT22 untuk menguji sistem.
6. Amati perubahan LED, buzzer, dan dashboard Blynk.

## Catatan
Auth Token Blynk tidak ditampilkan pada repository untuk menjaga keamanan.
