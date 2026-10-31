# HavaTV

Android TV için açık kaynaklı hava durumu uygulaması (YoWindow + Yandex Hava tarzı özellikler).

## Özellikler
- **Hava:** anlık durum, saatlik ve 10 güne kadar tahmin, yağış beklentisi, UV, hava kalitesi, gündoğumu/günbatımı, ay evresi
- **Çoklu kaynak ortalaması:** Open-Meteo + met.no + METAR (havalimanı) değerlerinin ağırlıklı ortalaması (sıcaklık, nem, rüzgâr, basınç, yağış)
- **Canlı manzara:** gün saatine ve havaya göre değişen animasyonlu gökyüzü
- **Radar:** RainViewer yağış radarı, oynat/durdur, kaydır, yakınlaştır
- **Manyetik fırtına:** NOAA Kp indeksi, G ölçeği, 3 günlük tahmin
- **Alarmlar:** deprem (AFAD/USGS), rüzgâr, yağış, sıcak/soğuk, fırtına, kar, manyetik fırtına, hava kalitesi; sesli, eşikleri ayarlanabilir
- **Yönetici konsolu:** her ayar tek yerden (kaynak ağırlıkları, birimler, radar, alarm eşikleri...)
- **Ekran koruyucu:** canlı manzara + saat + sıcaklık, yağmurda hafif/şiddetli yağmur sesi

## Menü
Sol üstteki ☰ düğmesi: Hava durumu, Radar, Manyetik fırtına, Alarmlar ve en altta Yönetici konsolu.
Kumandada sol/sağ tuşları ayar değerini değiştirir, OK seçer, Geri çıkar.

## APK'yı alma
1. Bu klasörün içeriğini GitHub'da bir depoya (`main` dalı) yükle.
2. **Actions** sekmesinde "APK derle" çalışır (3-6 dk).
3. Bitince **Releases → latest** altında `HavaTV.apk` oluşur.
4. TV'de **Downloader** ile aç:
   `https://github.com/KULLANICI/DEPO/releases/download/latest/HavaTV.apk`

## Ekran koruyucu olarak seçme
TV **Ayarlar → Cihaz tercihleri → Ekran koruyucu → Ekran koruyucu** listesinde **HavaTV**'yi seç,
**Başlama zamanı**nı 5 dakika yap. Listede görünmezse (bilgisayardan):

    adb connect TV_IP
    adb shell settings put secure screensaver_components com.example.havatv/.HavaDream
    adb shell settings put system screen_off_timeout 300000

## Veri kaynakları
Open-Meteo, met.no, aviationweather.gov, RainViewer, NOAA SWPC, AFAD, USGS. Hepsi anahtarsız.
Ticari kullanım ve kullanım sınırları için kaynakların şartlarını kontrol et.
