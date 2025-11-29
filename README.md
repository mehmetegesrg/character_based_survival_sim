# 🌲 C ile Geliştirilmiş Metin Tabanlı Hayatta Kalma Oyunu

![Language](https://img.shields.io/badge/Language-C-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)
[![University](https://img.shields.io/badge/University-Kırklareli-red.svg)](https://www.klu.edu.tr/)

> Vahşi doğada kaynaklarınızı yönetin, doğru kararları verin ve hayatta kalın!

Bu proje, **C Programlama Dili** kullanılarak geliştirilmiş, algoritma ve veri yapıları temellerini (döngüler, koşul yapıları, rastgele sayı üretimi) pekiştirmeyi amaçlayan bir **CLI (Komut Satırı Arayüzü)** simülasyon oyunu ödevidir.

## 🎮 Oyun Hakkında

Oyuncu, ıssız bir doğada sınırlı kaynaklarla hayatta kalmaya çalışan bir karakteri yönetir. Amaç; sağlık ve enerji seviyelerini dengede tutarak, rastgele gelişen olaylara (avlanma, sığınak bulma, tehlike dalgaları) karşı stratejik kararlar vermektir.

Oyun, **Sıra Tabanlı (Turn-Based)** bir mantıkla çalışır ve her hamle oyuncunun kaynaklarını etkiler.

## 🚀 Özellikler

* **Dinamik Kaynak Yönetimi:** Sağlık, Enerji ve Yemek stoklarını sürekli kontrol etmelisiniz.
* **Rastgele Olay Algoritması:** Avlanma veya barınak arama sonuçları `rand()` fonksiyonu ile olasılık tabanlı hesaplanır. Her oyun farklı bir deneyim sunar.
* **Mini Oyun (Şifre Kırma):** Oyun içinde enerji harcayarak yemek kazanabileceğiniz, mantıksal sorgulama içeren bir sayı tahmin modülü bulunur.
* **Durum Kontrolü (State Management):** Enerjiniz bittiğinde hareket kabiliyetiniz kısıtlanır (Sadece dinlenebilirsiniz).
* **Kalıcı Döngü:** Oyun bittiğinde programdan çıkmadan yeniden başlatma (Restart) mekanizması mevcuttur.

## 🛠️ Kurulum ve Çalıştırma

Bu projeyi çalıştırmak için bilgisayarınızda bir C derleyicisinin (GCC gibi) yüklü olması gerekir.

### 1) Repoyu klonlayın
   ```bash
   git clone [https://github.com/kullaniciadiniz/survival-game-c.git](https://github.com/kullaniciadiniz/survival-game-c.git)
```
### 2) Dizine Girin
```bash
cd survival-game-c
```

### 3) Derleyin
```bash
gcc algoritma_hayatta_kalma.c -o survival_game
```

### 4) Oyunu Başlatın

**Windows:**
```bash
survival_game.exe
```

**Linux / macOS:**
```bash
./survival_game
```

---

## 🕹️ Nasıl Oynanır?

| Tuş | Komut | Açıklama |
|-----|--------|-----------|
| **A** | Avlan | Enerji harcar (-20). %60 şansla yemek bulabilirsiniz. |
| **S** | Sığınak Ara | Enerji harcar, %50 ihtimalle sığınak bulursunuz. |
| **R** | Dinlen | Enerji ve sağlık yenilenir. |
| **E** | Envanter | Tüm durumunuzu gösterir. |
| **F** | Tehlike | 3 dalga saldırı alırsınız, zor bir hayatta kalma testi. |
| **P** | Şifre | 4 haneli tahmin mini oyunu. |
| **Y** | Yemek Ye | Yemek tüketerek +25 enerji kazanırsınız. |
| **X** | Çıkış | Oyundan çıkar. |

---

## 🧠 Teknik Detaylar

- Sonsuz döngü ile oyun restart sistemi
- Do-while, for döngüsü
- Switch-case ile komutların işlenmesi  
- `rand()` ile rastgele olay sistemi  
- Kullanılan kütüphaneler:
  - `<time.h>`
  - `<ctype.h>`
  - `<stdlib.h>`

---

## 🧩 Örnek Kod Kesiti

```c
        printf("\n");
        printf("############################################################\n");
        printf("#          KARAKTER TABANLI HAYATTA KALMA OYUNU            #\n");
        printf("############################################################\n");
        printf("#  Vahsi dogadasiniz. Kaynaklariniz sinirli.               #\n");
        printf("#  Amaciniz hayatta kalmak. Basarilar!                     #\n");
        printf("############################################################\n\n");
        printf("Komutlar:\n");
        printf("[A]vlan   : Enerji harcar, yemek bulma sansi vardir.\n");
        printf("[S]iginak : Guvenli yer arar. (Enerjiniz yoksa siginak aranmaz)\n");
        printf("[R]Dinlen : Enerji ve sagligi artirir.\n");
        printf("[E]nvanter: Mevcut durumunuzu gosterir.\n");
        printf("[F]Tehlike: Tehlike dalgasini gosterir. (Saglik ve enerji kaybi yasanir)\n");
        printf("[P]Sifre  : Kilitli sandiklari acmak icin. (Hatali girisler enerji tuketir)\n");
        printf("[Y]emek Ye: Envanterdeki yemegi tuketir (+Enerji).\n");
        printf("[X]Cikis  : Oyunu sonlandirir.\n");

        // --- OYUN TUR DÖNGÜSÜ ---
        do {
            printf("\n--------------------------------\n");
            printf("Saglik: %d | Enerji: %d | Yemek: %d | Siginak: %s\n",
                   saglik, enerji, yemek, siginak ? "VAR" : "YOK");
            printf("Ne yapmak istiyorsunuz? (A/S/R/E/F/P/Y/X): ");

            scanf(" %c", &komut);
            komut = toupper(komut);
```

---

## 📸 Örnek Oyun Çıktısı

```
Saglik: 85 | Enerji: 40 | Yemek: 1 | Siginak: YOK
Ne yapmak istiyorsunuz? (A/S/R/E/F/P/Y/X): A

>> Avlanmaya ciktiniz...
>> BASARILI! Tavsan yakaladiniz. (+1 Yemek)
```
