<div align="center">

# Batuhan Dede
### Gömülü Sistemler • Aviyonik & Uçuş Kontrol • Elektrikli Mobilite

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/batuhandede)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/bthndede)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:batuhan@example.com)

*Donanım ile yazılımın kesişim noktasında; yüksek güvenilirlik gerektiren gerçek zamanlı gömülü sistemler, uçuş kontrol bilgisayarları ve otonom/elektrikli araç mimarileri geliştiriyorum.*

</div>

---

### Hakkımda

Kocaeli Üniversitesi'nde sürdürdüğüm mühendislik eğitimimi, savunma/havacılık ve elektrikli araç ekosistemlerindeki saha tecrübelerimle birleştiriyorum. 

- **Aviyonik & Roket Sistemleri ([KouSpace](https://github.com/bthndede)):** TEKNOFEST ve Dikey İnişli Roket Yarışması kapsamında özgün uçuş kontrol bilgisayarlarının (UKB) donanım-yazılım mimarisi, CONOPS kurgusu, OpenRocket simülasyonları ve teknik tasarım raporları (ÖTR, KTR, AHR) üzerine çalışıyorum.
- **Elektrikli Araç Teknolojileri (Musoshi):** Mühendislik stajım süresince elektrikli araç alt sistemlerinin test, entegrasyon ve saha veri analizi süreçlerinde aktif görev aldım.
- **Gömülü Ar-Ge & Girişimcilik:** **ESP32** tabanlı kablosuz telemetri, sensör füzyonu ve RTOS mimarileri geliştiriyor; Kocaeli Teknoloji Atölyeleri ve 42 Kocaeli ekosistemlerinde edindiğim pratiği **TÜBİTAK 1812 BİGG** odağında ticarileştirilebilir teknoloji ürünlerine dönüştürüyorum.

---

### Öne Çıkan Mühendislik Mimarisi (UKB & Telemetri Akışı)

Projelerimde uyguladığım tipik gerçek zamanlı veri işleme ve uçuş kontrol döngüsü:

```mermaid
graph LR
    subgraph Sensör Katmanı
        A[IMU / 9-DOF] --> D
        B[Barometre & GPS] --> D
    end

    subgraph Uçuş Kontrol Bilgisayarı - MCU
        D[Sensör Füzyonu & Kalman Filtresi] --> E{Durum Makinesi / RTOS}
        E -->|Kritik İrtifa / Apogee| F[Kurtarma & Ateşleme Sistemi]
        E -->|Telemetri Paketi| G[RF / LoRa / Wi-Fi Modülü]
    end

    subgraph Yer İstasyonu
        G <-->|Çift Yönlü Veri| H[Telemetri Arayüzü & Uçuş Kaydı]
    end

    style D fill:#1f2937,stroke:#3b82f6,stroke-width:2px,color:#fff
    style E fill:#1f2937,stroke:#10b981,stroke-width:2px,color:#fff
    style F fill:#7f1d1d,stroke:#ef4444,stroke-width:2px,color:#fff
