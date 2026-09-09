# MorphSuite — İndirme

**Günlük belge işlerini tek çatı altında toplayan, tamamen çevrimdışı çalışan
bir masaüstü araç takımı.**

Belgeleriniz bilgisayarınızdan çıkmaz. Hiçbir buluta gönderilmez, kullanım
verisi toplanmaz, hesap açmanız gerekmez.

---

## İndir

| | Platform | Dosya | Boyut |
|---|---|---|---|
| 🪟 | **Windows 10 / 11** | **[MorphSuite_Kurulum.exe ⬇](../../releases/latest/download/MorphSuite_Kurulum.exe)** | 431 MB |
| 🐧 | **Pardus / Linux** | **[MorphSuite_Linux.tar.gz ⬇](../../releases/latest/download/MorphSuite_Linux.tar.gz)** + **[kur.sh ⬇](../../releases/latest/download/kur.sh)** | 376 MB |

Bu bağlantılar **her zaman en son sürümü** verir. Tüm sürümler:
[Releases](../../releases)

---

## Kurulum

### Windows
İndirdiğiniz `MorphSuite_Kurulum.exe` dosyasına çift tıklayın.

> **Windows bir uyarı gösterecek.** "Windows bilgisayarınızı korudu" diyorsa
> **Ek bilgi → Yine de çalıştır** deyin. Sebebi: kurulum dosyası dijital
> olarak imzalanmamış — imza sertifikası ücretli ve donanım anahtarı
> gerektiriyor, henüz alınmadı. Dosyanın doğruluğunu aşağıdaki SHA-256 ile
> kendiniz kontrol edebilirsiniz.

Yönetici hakkı verirseniz `C:\Program Files\Morph`, vermezseniz kullanıcı
profilinize kurar — **ikisi de çalışır**. Kaldırmak: Ayarlar → Uygulamalar.

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
| **PDF** | MorphPDF | Metin/görsel düzenleme, sayfa işlemleri, tablo, bölge bazlı OCR |
| **VIEW** | MorphViewer | Hızlı görüntüleyici; düzenlemeye ve dönüştürmeye devreder |
| **SLC** | MorphSlice | PDF sıkıştırma ve bölme |
| **MRG** | MorphMerge | Birleştirme, sayfa sıralama ve numaralama |
| **WM** | MorphWatermark | Filigran temizleme |
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
bilgisi otomatik eklenir).

## Lisans

**AGPL-3.0**. Lisans metni, üçüncü taraf bileşen listesi ve gizlilik
açıklaması her kurulum paketinin kökünde bulunur.
