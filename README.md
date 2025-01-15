# Schengen Vize Randevu Kontrol Programı 🔍

Bu program, Schengen vizesi için randevu kontrolü yapmanızı sağlar. Program belirttiğiniz ülke ve şehir için düzenli olarak randevu kontrolü yapar ve uygun randevu bulunduğunda Telegram üzerinden bildirim gönderir.

## Özellikler ✨

- 10 Schengen ülkesi için randevu kontrolü
- Türkiye'deki tüm VFS Global merkezleri desteklenir
- Telegram üzerinden anlık bildirimler
- Kullanıcı dostu menü arayüzü
- Otomatik randevu kontrolü
- Tarih bazlı sıralama ve Türkçe tarih formatı

## Kurulum 🛠️

1. Python 3.8 veya üzeri sürümü yükleyin
2. Gerekli paketleri yükleyin:
```bash
pip install python-telegram-bot python-dotenv aiohttp
```

3. `.env` dosyası oluşturun ve Telegram bot bilgilerinizi ekleyin:
```
TELEGRAM_BOT_TOKEN=your_bot_token
TELEGRAM_CHAT_ID=your_chat_id
```

## Kullanım 📱

1. Programı başlatın:
```bash
python check_appointment.py
```

2. Ülke seçimi yapın (1-10):
   - Fransa
   - Almanya
   - Hollanda
   - İtalya
   - İspanya
   - Yunanistan
   - Belçika
   - Avusturya
   - Danimarka
   - İsveç

3. Şehir seçimi yapın:
   - Ankara
   - Istanbul
   - Izmir
   - Antalya
   - Gaziantep
   - Bursa
   - Edirne

4. Kontrol sıklığını belirleyin (1-60 dakika)

## Menü Seçenekleri 📋

- **Yeni sorgu başlat**: Yeni ülke ve şehir için randevu kontrolü başlatır
- **Mevcut sorguyu durdur**: Aktif sorguyu durdurur
- **Programdan çık**: Programı sonlandırır

## Bildirimler 📬

Program randevu bulduğunda Telegram üzerinden aşağıdaki bilgileri içeren bir bildirim gönderir:
- Ülke adı (Türkçe)
- Merkez bilgisi
- En yakın randevu tarihi (örn: 7 Şubat 2025)
- Vize kategorisi
- Alt kategori (varsa)
- Randevu linki

## Kısayollar ⌨️

- **Ctrl+C**: Menüye dönmek için
- **3**: Programdan çıkmak için

## Notlar 📝

- Program her kontrol sonrası belirlediğiniz süre kadar bekler
- Randevular tarih sırasına göre listelenir
- Telegram bildirimleri için bot token ve chat ID gereklidir
- Program kesintisiz çalışabilir, istediğiniz zaman menüden kontrol edebilirsiniz

## Hata Durumları ⚠️

Program aşağıdaki durumlarda sizi bilgilendirir:
- API bağlantı hataları
- Geçersiz ülke/şehir seçimleri
- Telegram bildirim hataları
- Diğer beklenmeyen hatalar

## Katkıda Bulunma 🤝

1. Bu depoyu fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/amazing`)
3. Değişikliklerinizi commit edin (`git commit -m 'Yeni özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/amazing`)
5. Pull Request oluşturun 