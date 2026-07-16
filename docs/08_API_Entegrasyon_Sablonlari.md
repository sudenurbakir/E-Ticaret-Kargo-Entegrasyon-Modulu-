# 08 - API Entegrasyon Şablonları

Bu doküman, kullanıcının kargo firmalarını sisteme eklerken kullanacağı API entegrasyon yapılarını ve şablonları tanımlar.

## 1. Genel API Bilgi Şablonu

{
  "firmaAdi": "Pusula Kargo",
  "tip": "Hazir / Ozel",
  "baseUrl": "https://api.pusulakargo.com/v2",
  "apiKey": "BURAYA_API_KEY_YAZILMALIDIR",
  "apiSecret": "BURAYA_API_SECRET_YAZILMALIDIR",
  "username": "entegrasyon@magaza.com",
  "password": "••••••••••••",
  "testModu": false,
  "aktif": true,
  "sonTestTarihi": "2026-07-16T14:30:00"
}
## 2. Zorunlu ve Opsiyonel Alanlar

| Alan Adı       | Zorunlu | Açıklama                                      | Örnek Değer                        |
|----------------|---------|-----------------------------------------------|------------------------------------|
| firmaAdi       | Evet    | Görünen firma adı                             | Pusula Kargo                       |
| baseUrl        | Evet    | API temel adresi                              | https://api.ornek.com/v1           |
| apiKey         | Evet    | Genel kimlik doğrulama anahtarı               | pk_live_abc123...                  |
| apiSecret      | Hayır   | Gizli anahtar (çoğu API'de kullanılır)        | sk_live_xyz987...                  |
| username       | Hayır   | Kullanıcı adı (bazı firmalarda)               | entegrasyon@magaza.com             |
| testModu       | Evet    | Test ortamı aktif mi?                         | true / false                       |

3. Özel Kargo Firması Ekleme Örneği
JSON
{
  "firmaAdi": "Benim Özel Lojistik",
  "tip": "Ozel",
  "baseUrl": "https://api.benimloji.com/shipment",
  "apiKey": "custom_key_987654321",
  "apiSecret": "custom_secret_abc123",
  "testModu": true,
  "aktif": false
}

4. Entegrasyon Test Süreci

Kullanıcı bilgileri girdikten sonra "Test Et" butonuna basar.
Sistem şu kontrolleri yapar:
Base URL erişilebilir mi?
API Key geçerli mi?
Örnek bir kargo sorgusu başarılı mı?

Sonuç kullanıcıya net bir şekilde gösterilir.

