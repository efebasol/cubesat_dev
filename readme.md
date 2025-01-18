# TR/ CubeSat Projesi - Geliştirme Adımları
# EN/ CubeSat Project - Development Steps

## TR/ Proje Açıklaması
Bu proje, 1/4 U boyutunda bir CubeSat tasarlamayı ve geliştirmeyi amaçlamaktadır. CubeSat, temel olarak yörüngeye çıkabilecek bir uydu standardına uygun tasarlanacaktır. Ancak bu proje, yörüngeye fırlatılmaktan ziyade yer testleri ve prototipleme odaklıdır.

**Projenin hedefi:**
- Sensörlerden alınan verileri toplayıp işlemeyi,
- İşlenen verileri haberleşme modülü ile bir yer istasyonuna veya başka bir uyduya iletmeyi sağlamaktır.

**CubeSat, iki temel katmandan oluşacaktır:**
1. **Enerji Yönetim Katmanı:**
   - 1.1 Güneş panelleri ve bir Lipo pil yardımıyla sistemin güç ihtiyacını karşılayacak.
   - 1.2 Voltaj düzenlemeleri yapacak ve enerji tüketimini izleyecektir.
2. **Kontrol ve Haberleşme Katmanı:**
   - 2.1 Mikrodenetleyici, sensörler ve haberleşme modülü gibi temel bileşenleri içerecektir.

Projenin önceliği, düşük bütçeyle, yüksek verimli ve modüler bir tasarım gerçekleştirmektir. Bu süreçte öğrenci düzeyinde uygulanabilirlik ve geliştirme kolaylığına odaklanılmıştır.

## EN/ Project Description
This project aims to design and develop a 1/4 U CubeSat. The CubeSat will be designed to meet the standards of a satellite capable of reaching orbit. However, this project focuses on ground tests and prototyping rather than being launched into orbit.

**Project goals:**
- Collecting and processing data from sensors,
- Transmitting the processed data to a ground station or another satellite via the communication module.

**The CubeSat will consist of two main layers:**
1. **Power Management Layer:**
   - 1.1 It will manage the system's power needs using solar panels and a LiPo battery.
   - 1.2 It will regulate voltages and monitor energy consumption.
2. **Control and Communication Layer:**
   - 2.1 This will house the microcontroller, sensors, and communication module as essential components.

The project's priority is to achieve a cost-effective, highly efficient, and modular design. The focus is on student-level feasibility and ease of development.

---

## TR/ Şu Anki Durum
Proje, Araştırma ve Planlama aşamasında. Kullanılacak bileşenler belirlenmiş ve sistem tasarımı yapılmıştır. Şimdi, donanım prototipleme aşamasına geçilecektir.

## EN/ Current Status
The project is currently in the Research and Planning phase. The components to be used have been identified, and the system design has been completed. Next, the hardware prototyping phase will begin.

---

## TR/ Geliştirme Adımları
## EN/ Development Steps

### 1. TR/ Araştırma ve Planlama
1.1 CubeSat standartları ve gereksinimleri belirlenecek.
1.2 Kullanılacak bileşenler ve parçalar seçilecek.
1.3 Projenin genel tasarımı ve iş akışı oluşturulacak.

### 1. EN/ Research and Planning
1.1 CubeSat standards and requirements will be determined.
1.2 Components and parts to be used will be selected.
1.3 The overall design and workflow of the project will be created.

### 2. TR/ Donanım Prototipleme
2.1 Sensörler ve modüller breadboard üzerinde test edilecek.
2.2 STM32 geliştirme kartı ile haberleşme protokolleri doğrulanacak.

### 2. EN/ Hardware Prototyping
2.1 Sensors and modules will be tested on a breadboard.
2.2 Communication protocols will be verified using the STM32 development board.

### 3. TR/ PCB Tasarımı ve Üretimi
3.1 Prototip testlerinden sonra PCB şematik ve tasarımı yapılacak.
3.2 Üretim için Gerber dosyaları oluşturularak gönderilecek.

### 3. EN/ PCB Design and Manufacturing
3.1 After prototype testing, PCB schematics and design will be created.
3.2 Gerber files will be generated and sent for manufacturing.

### 4. TR/ Yazılım Geliştirme
4.1 STM32 için temel yapılandırma yapılacak.
4.2 Sensörler ve haberleşme modülü için gerekli yazılımlar geliştirilecek.
4.3 Sistemin tüm yazılım bileşenleri entegre edilecek.

### 4. EN/ Software Development
4.1 Basic setup for the STM32 will be completed.
4.2 Necessary software for sensors and the communication module will be developed.
4.3 All software components of the system will be integrated.

### 5. TR/ Montaj ve Test Süreci
5.1 PCB üzerinde bileşenler montajlanacak ve bağlantılar test edilecek.
5.2 Yazılım ve donanım entegrasyonu sağlanacak.
5.3 Sistemin genel testleri (haberleşme, enerji, veri işleme) gerçekleştirilecek.

### 5. EN/ Assembly and Testing Process
5.1 Components will be assembled on the PCB, and connections will be tested.
5.2 Software and hardware integration will be completed.
5.3 General tests of the system (communication, energy, data processing) will be carried out.

### 6. TR/ Sonuç ve Raporlama
6.1 Prototip değerlendirilip eksiklikler belirlenecek.
6.2 İyileştirme planları hazırlanacak ve dokümantasyon tamamlanacak.

### 6. EN/ Conclusion and Reporting
6.1 The prototype will be evaluated, and deficiencies will be identified.
6.2 Improvement plans will be prepared, and documentation will be finalized.

---

## TR/ Dosya Yapısı (Geliştirlmektedir)
## EN/ File Structure (Being Developed)

project-directory/  
├── docs/  
│   ├── project-description.md  # Detailed description of the project  
│   ├── planning.md             # Research and planning details  
│   ├── test-results.md         # Test results report  
├── firmware/  
│   ├── src/                    # Source code of the software  
│   ├── include/                # Header files  
│   └── build/                  # Build outputs  
├── hardware/  
│   ├── schematics/             # PCB schematic files  
│   ├── gerbers/                # Gerber files for manufacturing  
│   └── test/                   # Documentation for hardware testing  
└── README.md                   # Main file with project overview  