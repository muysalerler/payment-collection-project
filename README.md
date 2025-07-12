# Payment Collection Project

This is a microservices-based payment collection system developed during my internship at Turkcell. The project consists of two separate Spring Boot applications:

---

## 🔹 paymentservice/

- Starts with a main dashboard (`index.html`) that links to both invoices and stats pages.
- Allows users to create invoices manually or simulate them.
- Sends payment data (in TRY or USD) to Kafka.
- Frontend built with Thymeleaf (`index.html`, `invoices.html`)

## 🔹 tahsilatservice/

- Kafka consumer that receives the payment data.
- Stores payments in an H2 database (separated by currency).
- Provides statistics for payments (`stats.html`) and makes it accessible through the main index page.

---

## 💻 Technologies Used

- Java 17
- Spring Boot 3
- Apache Kafka
- H2 Database
- Thymeleaf
- Maven

---

## 🚀 How to Run the Project

1. Start Zookeeper and Kafka.
2. Run both microservices:
   - `paymentservice`: `localhost:8080/index`
   - `tahsilatservice`: automatically runs Kafka consumer and exposes stats at `localhost:8081/stats`
3. From `index.html`, you can navigate to:
   - **Invoices Page** for invoice creation
   - **Stats Page** to view real-time payment statistics

---

## 📸 Demo Screenshots

**Main Menu (`index.html`)**  
![Main Page](assets/index.png)

**Invoices Page (`invoices.html`)**  
![Invoices Page](assets/invoices.png)

**Stats Page (`stats.html`)**  
![Stats Page](assets/stats.png)

---

## 👨‍💻 Author

Developed by Meriç Uysalerler as part of the Turkcell internship program.

---

# 📘 Ödeme Toplama Projesi (Türkçe)

Bu proje, Turkcell stajım kapsamında geliştirdiğim mikroservis tabanlı bir ödeme toplama sistemidir. Proje iki ayrı Spring Boot uygulamasından oluşur:

---

## 🔹 paymentservice/

- Ana giriş sayfası `index.html` üzerinden başlar.
- Kullanıcılar manuel veya otomatik fatura oluşturabilir.
- TRY ve USD türündeki ödemeleri Kafka aracılığıyla gönderir.
- Arayüz Thymeleaf ile geliştirilmiştir (`index.html`, `invoices.html`)

## 🔹 tahsilatservice/

- Kafka’dan gelen ödeme mesajlarını tüketir.
- TRY ve USD türündeki ödemeleri ayrı ayrı H2 veritabanında saklar.
- `stats.html` sayfası ile ödeme istatistiklerini görselleştirir. Bu sayfaya ana menüden ulaşılabilir.

---

## 💻 Kullanılan Teknolojiler

- Java 17  
- Spring Boot 3  
- Apache Kafka  
- H2 Veritabanı  
- Thymeleaf  
- Maven  

---

## 🚀 Proje Nasıl Çalıştırılır?

1. Önce Zookeeper ve Kafka başlatılır.
2. İki uygulama çalıştırılır:
   - `paymentservice`: `localhost:8080/index` üzerinden erişilir.
   - `tahsilatservice`: Kafka mesajlarını alır ve `localhost:8081/stats` adresinde sonuçları gösterir.
3. `index.html` sayfası üzerinden:
   - **Invoices Page** ile fatura işlemleri
   - **Stats Page** ile istatistik sayfasına geçiş yapılabilir.

---

## 📸 Ekran Görüntüleri

**Ana Menü (`index.html`)**  
![Ana Menü](assets/index.png)

**Fatura Sayfası (`invoices.html`)**  
![Fatura Sayfası](assets/invoices.png)

**İstatistik Sayfası (`stats.html`)**  
![İstatistik Sayfası](assets/stats.png)

---

## 👨‍💻 Geliştirici

Bu proje, Meriç Uysalerler tarafından Turkcell staj programı kapsamında geliştirilmiştir.
