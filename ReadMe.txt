# 🎮 Turn-Based RPG Battle System (Unity)

Bu proje Unity kullanılarak geliştirilmiş **turn-based (sıra tabanlı) RPG savaş sistemi** içermektedir.  
Oyun yapısı, klasik RPG’lerde (örn. Sonny tarzı) olduğu gibi **karaktere veya düşmana tıklayarak yetenek seçme** mantığına dayanır.

## 🚀 Özellikler

- 🎯 **Sıra Tabanlı Savaş Sistemi**
  - Oyuncu hamlesi → düşman hamlesi döngüsü
- ⚔️ **Skill Wheel (Yetenek Çarkı)**
  - Düşmana tıkla → saldırı skilleri
  - Oyuncuya tıkla → heal / buff skilleri
- 🌀 **Slot Bazlı Animasyon Sistemi**
  - Skill Slot 1 → `Attack1`
  - Skill Slot 2 → `Attack2`
  - Skill Slot 3 → `Attack3`
- 👾 **Farklı Animator Yapıları**
  - Oyuncu: `Attack1 / Attack2 / Attack3`
  - Düşman: tek `Attack`
- ❤️ **HP / MP Sistemi**
- 📊 **Slider ve Text tabanlı UI**
- 🎨 **SpriteRenderer tabanlı 2D görseller**
- 🧠 **GameManager ile merkezi veri yönetimi**

---

## 🕹️ Oynanış

1. Oyun başladığında savaş sahnesi yüklenir
2. Oyuncu:
   - **Düşmana tıklarsa** → saldırı yetenekleri çıkar
   - **Kendine tıklarsa** → iyileştirme / buff yetenekleri çıkar
3. Skill seçildiğinde:
   - İlgili **slot numarasına göre animasyon oynar**
   - Hasar veya iyileştirme uygulanır
4. Düşman kendi sırası geldiğinde otomatik saldırır
5. HP 0 olursa:
   - Oyuncu → Defeat
   - Düşman → Victory

---

## 🧩 Teknik Detaylar

- **Unity Version:** 2022.x / 2023.x (2D)
- **Dil:** C#
- **UI:** Canvas + ScrollView + Button + TMP
- **Animasyon:** Animator Controller (Trigger tabanlı)
- **Input:** Mouse Click (Collider + ClickDetector)

---

## 📁 Önemli Scriptler

- `BattleManager.cs`  
  → Savaş akışı, sıra sistemi, hasar hesaplama, animasyon tetikleme

- `SkillWheelUI.cs`  
  → Mouse pozisyonunda skill ikonlarını dairesel dizen UI sistemi

- `ClickDetector.cs`  
  → Karakter ve düşman tıklamalarını algılar

- `GameManager.cs`  
  → Oyuncu statları, skill listesi, sahne geçişleri

---

## ⚙️ Kurulum

1. Projeyi klonla veya indir
2. Unity Hub üzerinden projeyi aç
3. `Scenes/BattleScene` sahnesini çalıştır
4. Play tuşuna bas 🎮

---

## 🛠️ Geliştirme Notları

- Skill sıralaması **GameManager’daki skill listesine göre** belirlenir
- ScrollView içindeki UI objeleri için:
  - `worldPositionStays = false` kullanılmıştır
  - Anchor ve Pivot ayarları önemlidir
- Physics2D Raycaster **yalnızca Main Camera üzerinde** bulunmalıdır

---

## 📌 Gelecek Planları

- 🔮 Status Effects (Poison, Stun, Burn)
- 🧙‍♂️ Mana regen / cooldown sistemi
- 🎵 Ses efektleri ve vuruş feedback
- 💾 Save / Load sistemi

---

## 👤 Geliştirici

**Yavuz Selim Köse**  
Unity & Game Development  
Türkiye 🇹🇷

---
## 🎨 Asset & Kaynaklar (itch.io)

Bu projede kullanılan görsel ve UI assetlerinin bir kısmı **itch.io** üzerinden edinilmiştir.

### Kullanılan Asset Türleri
- 🧙‍♂️ 2D karakter sprite ve animasyonları
- 👾 Düşman sprite ve animasyonları
- 🎨 Arka plan görselleri
- 🖼️ UI ikonları ve arayüz elementleri

### Kaynak
- https://itch.io/game-assets
- Asset’ler ilgili geliştiricilerin itch.io sayfalarından indirilmiştir.

> Tüm asset’ler, itch.io üzerindeki **ücretsiz veya izin verilen lisanslar** kapsamında  
> **eğitim, portföy ve demo amaçlı** kullanılmıştır.

Eğer proje ticari amaçla kullanılacak olursa, ilgili asset sahiplerinin lisans koşulları ayrıca gözden geçirilmelidir.

> Bu proje eğitim ve portföy amaçlı geliştirilmiştir.
