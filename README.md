# 🏕️ Karakter Tabanlı Hayatta Kalma Oyunu (C Console Game)

Bu proje, C programlama dili kullanılarak geliştirilmiş bir **komut satırı tabanlı hayatta kalma simülasyonudur**. Oyuncu; enerji, sağlık, yemek ve sığınak gibi temel kaynaklarını yöneterek mümkün olduğunca uzun süre hayatta kalmaya çalışır.  
Oyun tamamen metin tabanlıdır ve oyuncunun verdiği komutlara göre rastgele olaylar gelişir. Bu sayede her oyun turu farklı bir senaryo sunar.

Proje, özellikle **C’nin temel yapılarının (koşullar, döngüler, switch-case, do-while, rastgelelik, giriş doğrulama)** pratik olarak öğrenilmesini hedefler. Ayrıca platformdan bağımsız çalışan ekran temizleme, karakter doğrulama, enerji/saglık yönetimi gibi birçok temel mekanik içerir.

---

## ✨ Özellikler

- **Gerçek zamanlı kaynak yönetimi:**  
  Sağlık, enerji, yemek ve sığınak durumları oyun boyunca sürekli değişir.

- **Rastgele olay sistemi:**  
  Avlanırken hayvan bulma şansı, sığınak bulma olasılığı veya tehlike dalgalarındaki hasar tamamen rastgele oluşturulur.

- **Gelişmiş dinlenme sistemi:**  
  Sığınak varsa daha fazla enerji ve sağlık kazanılır, yoksa daha az.

- **3 aşamalı tehlike dalgası (for döngüsü):**  
  Her dalgada farklı miktarda hasar alınır, sığınak varsa hasar azaltılır.

- **Şifreli sandık açma sistemi (do-while):**  
  Kullanıcının sadece sayı girmesi zorunlu tutulur, yanlış girişte enerji kaybedilir.

- **Ekran temizleme desteği:**  
  Windows ve Linux/macOS için ayrı temizleme komutları kullanılır.

- **Ölüm ve yeniden başlatma sistemi:**  
  Sağlık sıfıra inince oyuncuya yeniden başlamak isteyip istemediği sorulur.

---

## 🧭 Komutlar

| Komut | Açıklama |
|-------|----------|
| **A** | Avlan – Enerji harcar, yemek bulma şansı vardır. |
| **S** | Sığınak ara – Enerji harcar, güvenli bir yer bulmaya çalışır. |
| **R** | Dinlen – Enerji ve sağlık yeniler. |
| **E** | Mevcut durumu gösteren envanter ekranını açar. |
| **F** | Tehlike dalgası – Rastgele hasar veren 3 saldırı başlatır. |
| **P** | Şifreli sandık – 4 haneli doğru şifreyi girmeye çalışırsınız. |
| **Y** | Yemek ye – Enerji kazanmak için yemek tüketir. |
| **X** | Oyundan çıkış yapar. |

---
