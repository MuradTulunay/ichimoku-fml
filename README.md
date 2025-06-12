# ICHIMOKU Cloud Indicators for FML

Bu repo, **Ichimoku Kinko Hyo (Cloud)** teknik analiz göstergelerinin **FML (Formula Language)** formatında uygulamasını içerir. ArTra ve benzer finansal analiz yazılımlarında kullanım için tasarlanmıştır.

## 📊 İçerik

### Ichimoku Cloud Sistem Bileşenleri

1. **ICHIMOKU_BASIC** - Temel 5 çizgi
2. **ICHIMOKU_CLOUD** - Cloud bölgesi vurgulamalı görünüm  
3. **ICHIMOKU_SIGNALS** - Trading sinyalleri ve crossover analizleri
4. **ICHIMOKU_COMPLETE** - Tam sistem (çizgiler + cloud + arrows)
5. **ICHIMOKU_ADVANCED** - İleri seviye analiz (Kumo Twist, Perfect Storm)

## 🎯 Kullanım

### 1. ICHIMOKU_BASIC
**Ana grafikte temel 5 çizgiyi gösterir:**

- **Tenkan Sen** (9 periyot) - Hızlı hareket ortalaması
- **Kijun Sen** (26 periyot) - Yavaş hareket ortalaması  
- **Senkou Span A** (26 periyot ileri) - Cloud üst/alt sınırı
- **Senkou Span B** (52 periyot ileri) - Cloud üst/alt sınırı
- **Chikou Span** (26 periyot geri) - Momentum göstergesi

### 2. ICHIMOKU_CLOUD
**Cloud (Kumo) bölgesi vurgulamalı görünüm:**

- Bullish Cloud (Senkou A > Senkou B) → **Yeşil** alan
- Bearish Cloud (Senkou A < Senkou B) → **Kırmızı** alan

### 3. ICHIMOKU_SIGNALS
**Alt panelde trading sinyalleri:**

- **TK_BULLISH/BEARISH** - Tenkan-Kijun kesişimleri
- **CLOUD_BREAKOUT_UP/DOWN** - Cloud kırılım sinyalleri
- **CHIKOU_CLEAR** - Chikou Span temizlik sinyali
- **STRONG_BUY/SELL** - Güçlü alım/satım sinyalleri

### 4. ICHIMOKU_COMPLETE
**Ana grafikte tam sistem:**

- Tüm çizgiler + Cloud dolgusu
- Buy/Sell ikonları (oklar)
- Trend durumu analizi

### 5. ICHIMOKU_ADVANCED
**İleri seviye analiz:**

- **KUMO_TWIST** - Cloud renk değişimi
- **CHIKOU_ABOVE/BELOW_CLOUD** - Chikou konum analizi
- **PERFECT_STORM_BUY/SELL** - Mükemmel konfigürasyon
- **VERY_BULLISH/BEARISH** - Güçlü trend durumu

## ⚙️ Parametreler

| Parametre | Varsayılan | Açıklama |
|-----------|------------|----------|
| `TENKAN_P` | 9 | Tenkan Sen periyodu (1-50) |
| `KIJUN_P` | 26 | Kijun Sen periyodu (1-100) | 
| `SENKOU_P` | 26 | Senkou Spans kaydırma (1-50) |
| `SENKOU_B_P` | 52 | Senkou Span B periyodu (1-200) |
| `CHIKOU_P` | 26 | Chikou Span kaydırma (1-50) |

## 🚀 Kurulum

1. `ICHIMOKU.fml` dosyasını indirin
2. ArTra/Plugins klasörüne kopyalayın
3. Uygulamayı yeniden başlatın
4. İndikatör menüsünden "Ichimoku Cloud Indicators" seçin

## 📈 Trading Stratejileri

### Bullish Sinyaller
- **TK Cross:** Tenkan > Kijun kesişimi
- **Cloud Break:** Fiyat cloud üstüne çıkışı  
- **Chikou Clear:** Chikou span temiz alan
- **Perfect Storm:** 3 sinyal birlikte

### Bearish Sinyaller
- **TK Cross:** Kijun > Tenkan kesişimi
- **Cloud Break:** Fiyat cloud altına düşüşü
- **Chikou Block:** Chikou span engelli
- **Perfect Storm:** 3 bearish sinyal birlikte

### Trend Analizi
- **VERY_BULLISH:** Fiyat cloud üstü + TK bullish + Chikou clear
- **BULLISH:** 2/3 koşul sağlandı
- **NEUTRAL:** Cloud içinde + karışık sinyaller
- **BEARISH:** 2/3 koşul bearish
- **VERY_BEARISH:** Fiyat cloud altı + TK bearish + Chikou blocked

## 🎨 Görsel Özelleştirme

```fml
// Cloud şeffaflığı ayarı
CLOUD_TRANSPARENCY: 30 (10-90)

// Sinyal hassasiyeti
SIGNAL_STRENGTH: 1=Zayıf, 2=Orta, 3=Güçlü

// Trading okları
SHOW_ARROWS: 0=Kapalı, 1=Açık

// Trend filtresi  
TREND_FILTER: 0=Kapalı, 1=Açık
```

## 🔧 Teknik Detaylar

### FML Kod Örneği
```fml
// Temel Ichimoku hesaplamaları
TENKAN:(HHV(H,TENKAN_P)+LLV(L,TENKAN_P))/2;
KIJUN:(HHV(H,KIJUN_P)+LLV(L,KIJUN_P))/2;
SENKOU_A:REF((TENKAN+KIJUN)/2,-SENKOU_P);
SENKOU_B:REF((HHV(H,SENKOU_B_P)+LLV(L,SENKOU_B_P))/2,-SENKOU_P);
CHIKOU:REF(C,CHIKOU_P);

// Cloud görselleştirme
CLOUD_BULLISH:=SENKOU_A>SENKOU_B;
FILLRGN(CLOUD_BULLISH,SENKOU_A,SENKOU_B),BrushGreen;
```

### Kod Optimizasyonu
- Maksimum 350 satır/indikatör
- Tek satır FML syntax
- Efficient calculation
- Memory optimization
- Clean variable naming

## 📚 Referanslar

- **Ichimoku Kinko Hyo** - Goichi Hosoda tarafından geliştirilen
- **5 Temel Çizgi:** Tenkan, Kijun, Senkou A/B, Chikou
- **3 Ana Sinyal:** TK Cross, Cloud Breakout, Chikou Confirmation

## 🤝 Katkıda Bulunma

1. Fork edin
2. Feature branch oluşturun (`git checkout -b feature/yeniOzellik`)
3. Commit edin (`git commit -m 'Yeni özellik eklendi'`)
4. Push edin (`git push origin feature/yeniOzellik`)
5. Pull Request oluşturun

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır.

## 📞 İletişim

- **GitHub:** [@MuradTulunay](https://github.com/MuradTulunay)
- **Email:** murad.tulunay@gmail.com

---

⭐ Bu repo'yu beğendiyseniz yıldız vermeyi unutmayın!
