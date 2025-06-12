# CHANGELOG

## v1.0.0.1 - 2025-06-12

### ✅ Eklenen Özellikler

#### ICHIMOKU Cloud Indikatörleri
- **ICHIMOKU_BASIC** - Temel 5 çizgi (Tenkan, Kijun, Senkou A/B, Chikou)
- **ICHIMOKU_CLOUD** - Cloud bölgesi vurgulamalı görünüm 
- **ICHIMOKU_SIGNALS** - Trading sinyalleri (TK Cross, Cloud Breakout, Chikou)
- **ICHIMOKU_COMPLETE** - Tam sistem (çizgiler + cloud + arrows)

#### Teknik Özellikler
- ✅ FML standardında 350 satır altı kod optimizasyonu
- ✅ Türkçe açıklamalar ve parametre isimleri
- ✅ SOLID prensiplere uygun clean code
- ✅ Tam parametrik yapı (tüm değerler ayarlanabilir)
- ✅ Ana grafik ve alt panel desteği

#### Sinyal Sistemi
- 🎯 **TK Cross:** Tenkan-Kijun kesişimleri
- 🎯 **Cloud Breakout:** Fiyat cloud kırılımları
- 🎯 **Chikou Clear:** Momentum onayı
- 🎯 **Strong Buy/Sell:** Kombinasyon sinyalleri
- 🎯 **Perfect Storm:** 3 sinyal birlikte

#### Görsel Özellikler
- 🎨 Bullish Cloud (Yeşil alan)
- 🎨 Bearish Cloud (Kırmızı alan)
- 🎨 Buy/Sell arrows (Trading okları)
- 🎨 Trend durumu analizi

### 📋 Kurulum Talimatları

1. `ICHIMOKU.fml` dosyasını indirin
2. `ArTra/Plugins/` klasörüne kopyalayın
3. Uygulamayı yeniden başlatın
4. "Trend Indicators" menüsünden seçin

### 🔧 Parametreler

| Parametre | Varsayılan | Açıklama |
|-----------|------------|----------|
| TENKAN_P | 9 | Tenkan Sen periyodu |
| KIJUN_P | 26 | Kijun Sen periyodu |
| SENKOU_P | 26 | Senkou kaydırma |
| SENKOU_B_P | 52 | Senkou B periyodu |
| CHIKOU_P | 26 | Chikou kaydırma |

### 🚀 Kullanım Örnekleri

#### Bullish Sinyal
```
- Tenkan > Kijun (TK Cross)
- Fiyat > Cloud (Breakout)
- Chikou > Geçmiş fiyat (Clear)
→ STRONG BUY sinyali
```

#### Bearish Sinyal
```
- Kijun > Tenkan (TK Cross)
- Fiyat < Cloud (Breakdown)
- Chikou < Geçmiş fiyat (Block)
→ STRONG SELL sinyali
```

### 📈 Trading Stratejileri

1. **Trend Takip:** ICHIMOKU_COMPLETE kullanın
2. **Sinyal Analizi:** ICHIMOKU_SIGNALS kullanın
3. **Görsel Analiz:** ICHIMOKU_CLOUD kullanın
4. **Temel Analiz:** ICHIMOKU_BASIC kullanın

### 🔍 Test Edildi

- ✅ ArTra platformunda test edildi
- ✅ Tüm parametreler çalışıyor
- ✅ Cloud görselleştirme aktif
- ✅ Trading arrows görünür
- ✅ Ana grafik ve alt panel desteği

### 📝 Notlar

- İndikatörler SOLID prensiplerine uygun yazılmıştır
- Kod satır sayısı 350 altında tutulmuştur
- Türkçe açıklamalar ve parametre isimleri kullanılmıştır
- Clean code standartlarına uygun optimizasyon yapılmıştır

---

## Gelecek Sürümler (Roadmap)

### v1.1.0 (Planlanan)
- [ ] ICHIMOKU_ADVANCED - Kumo Twist, Perfect Storm
- [ ] Multi-timeframe desteği
- [ ] Uyarı sistemi entegrasyonu
- [ ] Daha fazla görsel özelleştirme

### v1.2.0 (Planlanan)
- [ ] Backtest desteği
- [ ] Otomatik trading sinyalleri
- [ ] Risk yönetimi parametreleri
- [ ] İstatistiksel analiz araçları

---

**Geliştirici:** [@MuradTulunay](https://github.com/MuradTulunay)  
**Tarih:** 12 Haziran 2025  
**Platform:** ArTra / FML
