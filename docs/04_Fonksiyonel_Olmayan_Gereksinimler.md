# 04 - Fonksiyonel Olmayan Gereksinimler

## 1. Performans Gereksinimleri
- Sistem aynı anda en az 50 siparişin kargoya verilmesini sorunsuz desteklemeli
- Sayfa yüklenme süresi maksimum 2 saniye olmalı
- Kargo takibi sorguları hızlı cevap vermeli (maks. 3 saniye)

## 2. Güvenlik Gereksinimleri
- Kullanıcı API Key ve Secret gibi hassas bilgiler şifrelenerek saklanmalı
- Tüm API çağrıları HTTPS protokolü ile yapılmalı
- Kullanıcı yetkilerine göre erişim kontrolü (Mağaza yöneticisi, Operasyon, Admin)
- Tüm kritik işlemler loglanmalı

## 3. Kullanılabilirlik (Usability)
- Arayüz mevcut admin paneliyle aynı tasarım ve renk yapısına sahip olmalı
- Mobil ve tablet cihazlardan da rahat kullanılabilmeli
- Kullanıcı dostu arayüz (kolay navigasyon)

## 4. Güvenilirlik ve Dayanıklılık
- Sistemde kesinti olması durumunda kargo işlemleri kaydedilmeli
- Hata durumlarında kullanıcıya anlaşılır mesaj gösterilmeli
- Entegrasyon testleri başarısız olduğunda sistemi etkilememeli

## 5. Bakım ve Genişletilebilirlik
- Yeni kargo firması eklemek kolay olmalı
- Kod yapısı modüler tasarlanmalı (gelecekte yeni özellik eklemek kolay olsun)
- Dokümantasyon güncellenebilir yapıda olmalı

## 6. Diğer Gereksinimler
- Türkçe arayüz
- Temel erişilebilirlik standartlarına uyum
- Gelecekte gerçek kargo gönderme moduna kolay geçiş

---

