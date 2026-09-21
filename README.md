# MorphSuite — İndirme

**Günlük belge işlerini tek çatı altında toplayan, tamamen çevrimdışı çalışan
bir masaüstü araç takımı.**

Belgeleriniz bilgisayarınızdan çıkmaz. Hiçbir buluta gönderilmez, kullanım
verisi toplanmaz, hesap açmanız gerekmez.

---

## İndir

| | Platform | Dosya | Boyut |
|---|---|---|---|
| 🪟 | **Windows 10 / 11** | **[MorphSuite_Kurulum.exe ⬇](../../releases/latest/download/MorphSuite_Kurulum.exe)** | 356 MB |
| 🐧 | **Pardus / Linux** | **[MorphSuite_Linux.tar.gz ⬇](../../releases/latest/download/MorphSuite_Linux.tar.gz)** + **[kur.sh ⬇](../../releases/latest/download/kur.sh)** | 382 MB |

Bu bağlantılar **her zaman en son sürümü** verir. Tüm sürümler:
[Releases](../../releases)

---

## 2.5.0'da neler var

**Sıfırdan belge oluşturma.** Artık var olan bir PDF'i açmak zorunda
değilsiniz — beş kağıt boyutu (A4, A5, A3, Letter, Legal), dikey/yatay,
500 sayfaya kadar boş belge üretip doğrudan yazmaya başlayabilirsiniz.

**Yazı tipi ailesi.** Noto Serif gömüldü; Türkçe harfleri eksiksiz. Belgedeki
gerçek font adları serif/sans olarak gruplanıyor, her belgede farklı bir liste
çıkmıyor.

**Yeni araçlar.** İmza ve serbest çizim, köprü (link), şekiller
(çizgi/ok/dikdörtgen/elips), üstü çizili, açıda adımlı döndürme.

**Sürükle-bırak.** MorphViewer, MorphWatermark ve MorphConverter'a dosyayı
pencereye bırakarak açabilirsiniz.

**Filigran temizleme yeniden yazıldı.** Artık yalnızca metin filigranları
değil, **taranmış belgelerde piksele yanmış** filigranlar da temizleniyor.
Silmeden önce **Önce/Sonra önizlemesi** gösteriliyor. Önceki sürümde bazı
resmî belgelerde filigranla birlikte gövde metni de siliniyordu — bu
düzeltildi.

**Kurulum sihirbazı.** Windows kurulumu artık yol seçimi, ilerleme çubuğu ve
PDF ilişkilendirme adımı olan gerçek bir sihirbaz. Paket 431 MB'dan 356 MB'a
indi.

---

## Kurulum

### Windows

İndirdiğiniz `MorphSuite_Kurulum.exe` dosyasına çift tıklayın. Kurulum
sihirbazı açılır: **herkes için mi yoksa yalnızca siz mi** kurulacağını,
**hangi klasöre** kurulacağını ve **PDF dosyalarının MorphViewer ile
açılmasını** isteyip istemediğinizi sorar.

> **Windows bir uyarı gösterecek.** "Windows bilgisayarınızı korudu" diyorsa
> **Ek bilgi → Yine de çalıştır** deyin. Sebebi: kurulum dosyası dijital
> olarak imzalanmamış — imza sertifikası ücretli ve donanım anahtarı
> gerektiriyor, henüz alınmadı. Dosyanın doğruluğunu aşağıdaki SHA-256 ile
> kendiniz kontrol edebilirsiniz.

Yönetici hakkınız yoksa kurulum **başarısız olmaz**, kendi kullanıcı
profilinize kurar ve aynı şekilde çalışır. Kaldırmak: Ayarlar → Uygulamalar.

### Pardus / Linux

Arşivi ve `kur.sh`'ı **aynı klasöre** indirin:

```bash
tar -xzf MorphSuite_Linux.tar.gz
./kur.sh          # sadece bu kullanıcı
sudo ./kur.sh     # tüm kullanıcılar
```

Kurulum, PDF dosyalarının varsayılan olarak MorphViewer ile açılmasını **bir
kez sorar**; hayır derseniz "Birlikte aç" menüsünden her zaman seçebilirsiniz.
OCR için sistemde `tesseract-ocr` paketi gerekir.

---

## Araçlar

| | Araç | Ne yapar |
|---|---|---|
| **PDF** | MorphPDF | Sıfırdan belge oluşturma, metin ve görsel düzenleme, imza, köprü, şekiller, tablo, bölge bazlı OCR |
| **VIEW** | MorphViewer | Hızlı görüntüleyici; düzenlemeye ve dönüştürmeye devreder |
| **SLC** | MorphSlice | PDF sıkıştırma ve bölme |
| **MRG** | MorphMerge | Birleştirme, sayfa sıralama ve numaralama |
| **WM** | MorphWatermark | Filigran temizleme (metin, görsel ve taranmış belgeler) |
| **CONV** | MorphConverter | PDF ↔ görsel, PDF → metin, Office → PDF |

Araçlar birbirine iş devredebilir: görüntüleyicide açtığınız bir PDF'i tek
tıkla düzenlemeye ya da dönüştürmeye gönderebilirsiniz.

---

## Güncelleme

MorphSuite her açılışta yeni sürüm olup olmadığına bakar. Varsa sorar;
**hayır derseniz normal çalışmaya devam eder**. Evet derseniz güncellemeyi
kendisi indirir, doğrular ve kurar — tarayıcı açılmaz, dosya aramanız
gerekmez. Bağlantı koparsa kaldığı yerden devam eder.

Sunucuya ulaşılamazsa "ulaşılamadı" der — **"güncelsiniz" demez**, çünkü
bunu bilemez.

İstek anonimdir: kimlik bilgisi taşımaz, hiçbir kullanım verisi gönderilmez.

---

## Dosya doğrulama

Her sürümün SHA-256 özeti [`surum.json`](surum.json) içinde yayınlanır.

```powershell
Get-FileHash MorphSuite_Kurulum.exe -Algorithm SHA256    # Windows
```
```bash
sha256sum MorphSuite_Linux.tar.gz                        # Linux
```

---

## Bu depo hakkında

Burada **yalnızca yayınlanan sürümler** bulunur: güncelleme manifesti
(`surum.json`) ve kurulum paketleri. Kaynak kod burada değildir.

Hata bildirimi ve öneriler için **Issues** bölümünü kullanın; programın
içinden de **Hakkında → Geri Bildirim** ile açabilirsiniz (sürüm ve sistem
bilgisi otomatik eklenir). GitHub hesabınız yoksa
**destek@morphsuite.app** adresine yazabilirsiniz.

## Lisans

**AGPL-3.0**. Lisans metni, üçüncü taraf bileşen listesi ve gizlilik
açıklaması her kurulum paketinin kökünde bulunur.
