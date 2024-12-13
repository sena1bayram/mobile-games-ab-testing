# A/B Testi Analizi: Mobil Oyun Tutma Oranı

## 📊 Proje Genel Bakış

Bu proje, bir mobil oyunun A/B testinin sonuçlarını analiz etmektedir. Test, kullanıcıları iki gruba (gate_30 ve gate_40) ayırarak her iki grubun performansını karşılaştırmayı amaçlamaktadır. Analiz, üç ana metrik üzerine odaklanmaktadır:
- **Toplam Oyun Sayısı** (`sum_gamerounds`)
- **1. Gün Tutma Oranı** (`retention_1`)
- **7. Gün Tutma Oranı** (`retention_7`)

Veri setinde her iki grup için bu metriklerin ortalamaları ve bu metriklere dair yapılan istatistiksel testlerin sonuçları yer almaktadır.

## 📈 Hipotez

Testin amacı, aşağıdaki hipotezleri test etmektir:

- **H0 (Null Hipotezi)**: Gate 30 ve Gate 40 grupları arasında toplam oyun sayısı, 1. gün tutma oranı ve 7. gün tutma oranı açısından anlamlı bir fark yoktur.
- **H1 (Alternatif Hipotez)**: Gate 30 ve Gate 40 grupları arasında en az bir metrikte anlamlı bir fark vardır.

## 🔢 Analiz Sonuçları

### a) **Toplam Oyun Sayısı (Sum Gamerounds)**

- **Ortalamalar**:
  - Gate 30: 52.46 oyun 🎮
  - Gate 40: 51.30 oyun 🎮
  
- **T-testi Sonuçları**:
  - T-istatistiği: 0.89
  - P-değeri: 0.3729

**Sonuç**: P-değeri (0.3729) α=0.05'ten büyük olduğundan, toplam oyun sayısı açısından iki grup arasında anlamlı bir fark bulunmamaktadır. Bu, Gate 30 veya Gate 40'ın oyun süresi üzerinde önemli bir etkisi olmadığını göstermektedir. 🚫

### b) **1. Gün Tutma Oranı (Retention 1)**

- **Ortalamalar**:
  - Gate 30: %44.82 📅
  - Gate 40: %44.23 📅
  
- **T-testi Sonuçları**:
  - T-istatistiği: 1.78
  - P-değeri: 0.0744

**Sonuç**: P-değeri (0.0744) α=0.05'ten büyük olduğundan, 1. gün tutma oranları açısından iki grup arasında anlamlı bir fark bulunmamaktadır. Bu, her iki gruptaki kullanıcıların oyuna ilk gün dönme olasılığının benzediğini göstermektedir. ✅

### c) **7. Gün Tutma Oranı (Retention 7)**

- **Ortalamalar**:
  - Gate 30: %19.02 🗓️
  - Gate 40: %18.20 🗓️
  
- **T-testi Sonuçları**:
  - T-istatistiği: 3.16
  - P-değeri: 0.0016

**Sonuç**: P-değeri (0.0016) α=0.05'ten küçük olduğundan, 7. gün tutma oranları açısından iki grup arasında anlamlı bir fark bulunmaktadır. Gate 30 grubundaki kullanıcıların Gate 40 grubuna kıyasla oyuna 7. gün dönme olasılığı daha yüksektir. Bu, Gate 30'un uzun vadeli kullanıcı bağlılığını artırabileceğini göstermektedir. 🎯

---

## 📝 Genel Değerlendirme

- **Toplam Oyun Sayısı ve 1. Gün Tutma Oranı**: Her iki grupta da benzer sonuçlar elde edilmiştir. Kapı seçeneklerinin (Gate 30 ve Gate 40) bu metrikler üzerinde büyük bir etkisi olmadığı görülmektedir. 🔄
  
- **7. Gün Tutma Oranı**: Gate 30, Gate 40'a göre daha iyi performans göstermiştir. Uzun vadeli kullanıcı bağlılığı hedefleniyorsa, Gate 30'un kullanılması daha avantajlı olabilir. 🚀

- **Sonuçların Kullanımı**:
  - Geliştiriciler, oyuncuların uzun süre oyunda kalmasını teşvik etmek için Gate 30'u tercih edebilir. 🎮
  - Bununla birlikte, kısa vadeli etkiler üzerinde daha fazla test yapılarak ek veriler toplanabilir. 📊

---

## 📂 Veri Seti

Veri seti, mobil oyun kullanıcılarının davranışlarını içermektedir. Aşağıdaki metrikler veri setinde yer almaktadır:

- **sum_gamerounds**: Kullanıcı başına toplam oynanan oyun sayısı.
- **retention_1**: 1. gün tutma oranı.
- **retention_7**: 7. gün tutma oranı.
- **version**: Kullanıcıların dahil olduğu test grubu (`gate_30` veya `gate_40`).

## 📌 İstatistiksel Yöntemler

- **T-Testi**: Gruplar arasındaki farkın istatistiksel anlamlılığını değerlendirmek için iki bağımsız örneklem üzerinde yapılan T-testinden yararlanılmıştır.

---

## 🔗 Kaynaklar

- Veri seti: [Cookie Cats A/B Testi Verisi](https://www.kaggle.com)
- Python kütüphaneleri: pandas, matplotlib, scipy

---

**Not**: Bu analiz, sadece belirtilen metrikler üzerinde yapılmıştır. Farklı metrikler için daha fazla test ve analiz yapılabilir. 🔍
