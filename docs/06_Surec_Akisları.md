# 06 - Süreç Akışları

Bu doküman, kargo modülündeki ana süreçlerin otomatikleştirilmiş hallerini tanımlar.

## 1. Ana Süreç: Siparişten Kargoya (Otomatik Akış)

1. Siparişin durumu "Hazır" olur
2. Kullanıcı sipariş(leri) seçer ve "Kargoya Ver" butonuna basar
3. Kargo firması ve hizmet tipi seçilir
4. Sistem otomatik olarak:
   - Kargo etiketini oluşturur
   - Kargo numarasını siparişe kaydeder
   - Kargo durumunu "Kargoya Verildi" yapar
   - Müşteriye kargo takip linkini içeren bildirim gönderir (e-posta/SMS)

## 2. Kargo Takip Süreci (Yarı Otomatik)

1. Sistem kargo firması API’sinden periyodik olarak durum bilgisini çeker
2. Kargo durumları otomatik olarak güncellenir (Yolda, Teslim Edildi vb.)
3. Teslim edildiğinde müşteriye otomatik “Ürün teslim edildi” bildirimi gider
4. Operasyon ekibi gerektiğinde manuel müdahale edebilir

## 3. İade Kargo Süreci (Otomatik Akış)

1. Müşteri iade talebi oluşturur
2. Operasyon ekibi talebi onaylar
3. Sistem otomatik olarak iade kargo etiketini oluşturur
4. İade takip numarası müşteriye otomatik iletilir
5. İade ürünü depoya ulaştığında:
   - Depo sorumlusu ürünü inceleyerek durumu günceller (“İade Kabul Edildi” veya “Reddedildi”)
   - Kabul edilirse stok otomatik olarak güncellenir
   - Müşteriye iade süreci hakkında bildirim gider

## 4. Yeni Kargo Firması Entegrasyonu

1. Kullanıcı Ayarlar > Kargo Entegrasyonları’na gider
2. Yeni firma bilgilerini girer
3. “Test Et” butonu ile bağlantı test edilir
4. Başarılı olursa firma sisteme aktif olarak eklenir

## 5. Dashboard ve Otomatik Raporlama

Sistem her gün otomatik olarak şu bilgileri günceller:
- Toplam kargo adedi, teslimat performansı
- Geciken kargolar (otomatik uyarı)
- Kargo firmalarına göre başarı ve maliyet analizi
- İade oranı istatistikleri

---

**Commit Mesajı Önerisi:**
```bash
git commit -m "Update: 06_Surec_Akisları.md - Süreçler daha otomatik hale getirildi (bildirim, takip, iade)"
