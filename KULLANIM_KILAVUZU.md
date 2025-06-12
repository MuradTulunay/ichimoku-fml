# 📘 ICHIMOKU Cloud - Kurulum ve Kullanım Kılavuzu

## 🎯 Hızlı Başlangıç

### 1️⃣ Kurulum
```bash
# 1. Dosyayı indirin
wget https://raw.githubusercontent.com/MuradTulunay/ichimoku-fml/main/ICHIMOKU.fml

# 2. ArTra Plugins klasörüne kopyalayın
cp ICHIMOKU.fml "C:\repos\ArTra\ArTra\Plugins\"

# 3. ArTra'yı yeniden başlatın
```

### 2️⃣ İlk Kullanım
1. ArTra'yı açın
2. **İndikatörler** menüsünden **Trend Indicators** seçin
3. **ICHIMOKU_BASIC** ile başlayın
4. Parametreleri ihtiyacınıza göre ayarlayın

## 📊 İndikatör Türleri

### 🔵 ICHIMOKU_BASIC
**Kullanım:** Ana grafikte temel çizgiler
```
✅ Tenkan Sen (9) - Hızlı MA
✅ Kijun Sen (26) - Yavaş MA  
✅ Senkou Span A (26) - Cloud üst
✅ Senkou Span B (52) - Cloud alt
✅ Chikou Span (26) - Momentum
```

### 🟢 ICHIMOKU_CLOUD
**Kullanım:** Cloud vurgulamalı görünüm
```
✅ Tüm temel çizgiler
✅ Yeşil Cloud (Bullish)
✅ Kırmızı Cloud (Bearish)
✅ Görsel cloud fill
```

### 🟡 ICHIMOKU_SIGNALS
**Kullanım:** Alt panelde sinyal analizi
```
✅ TK_BULLISH/BEARISH
✅ CLOUD_BREAKOUT_UP/DOWN
✅ CHIKOU_CLEAR
✅ STRONG_BUY/SELL
```

### 🔴 ICHIMOKU_COMPLETE
**Kullanım:** Ana grafikte tam sistem
```
✅ Tüm çizgiler + Cloud
✅ Buy/Sell okları
✅ Trend analizi
✅ Tam trading sistemi
```

## ⚙️ Parametre Ayarları

### 📋 Standart Parametreler
| Parametre | Varsayılan | Minimum | Maksimum | Açıklama |
|-----------|------------|---------|----------|----------|
| `TENKAN_P` | 9 | 1 | 50 | Tenkan Sen periyodu |
| `KIJUN_P` | 26 | 1 | 100 | Kijun Sen periyodu |
| `SENKOU_P` | 26 | 1 | 50 | Senkou kaydırma |
| `SENKOU_B_P` | 52 | 1 | 200 | Senkou B periyodu |
| `CHIKOU_P` | 26 | 1 | 50 | Chikou kaydırma |

### 🎛️ Özel Ayarlar

#### Kısa Vadeli Trading (Scalping)
```
TENKAN_P: 5
KIJUN_P: 13
SENKOU_P: 13
SENKOU_B_P: 26
CHIKOU_P: 13
```

#### Uzun Vadeli Yatırım
```
TENKAN_P: 20
KIJUN_P: 60
SENKOU_P: 60
SENKOU_B_P: 120
CHIKOU_P: 60
```

#### Volatil Piyasalar
```
TENKAN_P: 7
KIJUN_P: 22
SENKOU_P: 22
SENKOU_B_P: 44
CHIKOU_P: 22
```

## 🎯 Trading Sinyalleri

### 📈 Bullish (Alım) Sinyalleri

#### 1. TK Cross Bullish
```
Koşul: Tenkan Sen > Kijun Sen kesişimi
Güvenilirlik: ⭐⭐⭐
Kullanım: Momentum değişimi
```

#### 2. Cloud Breakout Up
```
Koşul: Fiyat > Cloud (Senkou A & B)
Güvenilirlik: ⭐⭐⭐⭐
Kullanım: Trend başlangıcı
```

#### 3. Chikou Clear
```
Koşul: Chikou > 26 bar önceki fiyat
Güvenilirlik: ⭐⭐⭐
Kullanım: Momentum onayı
```

#### 4. Perfect Storm (En Güçlü)
```
Koşul: TK Cross + Cloud Break + Chikou Clear
Güvenilirlik: ⭐⭐⭐⭐⭐
Kullanım: Güçlü alım pozisyonu
```

### 📉 Bearish (Satım) Sinyalleri

#### 1. TK Cross Bearish
```
Koşul: Kijun Sen > Tenkan Sen kesişimi
Güvenilirlik: ⭐⭐⭐
Kullanım: Momentum zayıflaması
```

#### 2. Cloud Breakdown
```
Koşul: Fiyat < Cloud (Senkou A & B)
Güvenilirlik: ⭐⭐⭐⭐
Kullanım: Trend tersine dönüş
```

#### 3. Chikou Block
```
Koşul: Chikou < 26 bar önceki fiyat
Güvenilirlik: ⭐⭐⭐
Kullanım: Momentum zayıflığı
```

## 📊 Trend Analizi

### 🔍 Trend Belirleme

#### Very Bullish 🟢🟢
```
✅ Fiyat > Cloud
✅ Tenkan > Kijun
✅ Chikou > Geçmiş fiyat
→ Güçlü alım pozisyonu
```

#### Bullish 🟢
```
✅ 2/3 koşul sağlandı
→ Orta güçlü alım
```

#### Neutral ⚪
```
✅ Fiyat cloud içinde
✅ Karışık sinyaller
→ Bekleme pozisyonu
```

#### Bearish 🔴
```
✅ 2/3 koşul bearish
→ Orta güçlü satım
```

#### Very Bearish 🔴🔴
```
✅ Fiyat < Cloud
✅ Tenkan < Kijun  
✅ Chikou < Geçmiş fiyat
→ Güçlü satım pozisyonu
```

## 🎨 Görsel Özelleştirme

### 🖼️ Cloud Renkleri
```
Bullish Cloud: Yeşil (#00FF00)
Bearish Cloud: Kırmızı (#FF0000)
Şeffaflık: %30 (ayarlanabilir)
```

### 🏹 Trading Arrows
```
Buy Signal: Yeşil ok (Alt)
Sell Signal: Kırmızı ok (Üst)
Boyut: Otomatik
```

### 📏 Çizgi Stilleri
```
Tenkan Sen: Mavi çizgi
Kijun Sen: Kırmızı çizgi
Senkou A: Yeşil çizgi
Senkou B: Kırmızı çizgi
Chikou: Mor çizgi
```

## 🛠️ Sorun Giderme

### ❌ Yaygın Problemler

#### İndikatör Görünmüyor
```
✅ ICHIMOKU.fml dosyası Plugins klasöründe mi?
✅ ArTra yeniden başlatıldı mı?
✅ İndikatör menüsünden seçildi mi?
```

#### Cloud Gösterilmiyor
```
✅ ICHIMOKU_CLOUD kullanıyor musunuz?
✅ Senkou parametreleri doğru mu?
✅ Grafik tipi uygun mu?
```

#### Arrows Çalışmıyor
```
✅ ICHIMOKU_COMPLETE kullanıyor musunuz?
✅ Buy.Gif ve Sell.Gif dosyaları var mı?
✅ Sinyal koşulları sağlanıyor mu?
```

### 🔧 Performans Optimizasyonu

#### Yavaş Çizim
```
✅ Periyot değerlerini azaltın
✅ Veri aralığını sınırlayın
✅ Gereksiz indikatörleri kapatın
```

#### Bellek Kullanımı
```
✅ Sadece gerekli indikatörleri açın
✅ Grafik geçmişini sınırlayın
✅ Çoklu timeframe kullanmayın
```

## 📞 Destek

### 🆘 Yardım Kaynakları
- **GitHub Issues:** [Sorun bildir](https://github.com/MuradTulunay/ichimoku-fml/issues)
- **Email:** murad.tulunay@gmail.com
- **Wiki:** [Detaylı dokümantasyon](https://github.com/MuradTulunay/ichimoku-fml/wiki)

### 📝 Katkıda Bulunma
1. Repository'yi fork edin
2. Feature branch oluşturun
3. Değişikliklerinizi commit edin
4. Pull request açın

---

**💡 İpucu:** Bu kılavuzu bookmark'a ekleyin ve trading yaparken referans olarak kullanın!

**🚀 Başarılı trading dileriz!**
