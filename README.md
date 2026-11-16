<div align="center">

# Batuhan Dede
### Mekatronik Mühendisi | Donanım Tasarımı • Gömülü Sistemler • Model Tabanlı Kontrol

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/batuhan-dede)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/bthndede)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:batuhandede35@gmail.com)

*Kocaeli Üniversitesi Mekatronik Mühendisliği mezunu ve Elektrik Mühendisliği yüksek lisans öğrencisiyim. Çok katmanlı PCB tasarımı, gerçek zamanlı gömülü yazılım ve model tabanlı kontrol sistemleri geliştiriyor; prototip üretiminden donanım-yazılım doğrulama (MIL/SIL/HIL) testlerine kadar uçtan uca mühendislik çözümleri üretiyorum.*

</div>

---

### Deneyim & Liderlik

* **Model Tabanlı Yazılım Stajyeri — Musoshi (SGN)** *(Kasım 2025 – Ocak 2026)*
  * MATLAB/Simulink ve Stateflow kullanarak Araç Kontrol Ünitesi (VCU) durum makinelerini modelledim; MIL ve SIL simülasyonlarını yürüttüm.
  * Vector CANoe üzerinde test panelleri tasarlayıp DBC dosyalarını oluşturdum; HIL test altyapısına katkı sağladım ve CANalyzer üzerinden CAN mesaj analizleriyle kontrol algoritmalarını doğruladım.
* **Aviyonik Alt Sistem Sorumlusu & Takım Kaptanı — Kouspace Uzay ve Havacılık Topluluğu** *(Ekim 2021 – Halen)*
  * Aviyonik alt sistemlerin 4 katmanlı elektronik kart tasarımlarını, gömülü yazılımlarını, test ve sistem entegrasyon süreçlerini yönettim.
  * Takım kaptanı olarak proje planlaması, görev dağılımı ve yarışma süreçlerinde birimler arası teknik koordinasyonu sağladım.
* **Gömülü Yazılım ve Donanım Stajyeri — Asis Otomasyon ve Akaryakıt Sistemleri A.Ş.** *(Temmuz 2024 – Ağustos 2024)*
  * Konveyör sistemlerinde ürün tespiti için gömülü yazılım ve sensör kalibrasyonu geliştirdim; laboratuvar ortamında SMD/THT dizgi ve osiloskop ile fonksiyonel donanım testleri gerçekleştirdim.

---

### Öne Çıkan Mühendislik Projeleri

```mermaid
graph LR
    subgraph Sensör & Kontrol Katmanı
        A[IMU & LiDAR Sensörleri] --> B[STM32 / ESP32 MCU]
        C[Load Cell / Basınç / Sıcaklık] --> D[RS-485 DAQ Kartı]
    end

    subgraph Eyleyici & Haberleşme
        B -->|Modbus RTU| E[Endüstriyel Servo Sürücü & İğneli Valf]
        B -->|LoRa / CAN Bus| F[Telemetri & VCU Ağ Yapısı]
    end

    subgraph Doğrulama & Arayüz
        D --> G[Bilgisayar Veri Toplama Arayüzü]
        F --> H[CANoe / CANalyzer & Yer İstasyonu]
    end

    style B fill:#1f2937,stroke:#3b82f6,stroke-width:2px,color:#fff
    style E fill:#1f2937,stroke:#10b981,stroke-width:2px,color:#fff
    style D fill:#1f2937,stroke:#f59e0b,stroke-width:2px,color:#fff
