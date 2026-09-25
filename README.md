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
| 🐧 | **Pardus (.deb)** | **[MorphSuite_Pardus.deb ⬇](../../releases/latest/download/MorphSuite_Pardus.deb)** | 340 MB |
| 🐧 | **Pardus / Linux (arşiv)** | **[MorphSuite_Linux.tar.gz ⬇](../../releases/latest/download/MorphSuite_Linux.tar.gz)** + **[kur.sh ⬇](../../releases/latest/download/kur.sh)** | 386 MB |
| 📱 | **Android — MorphScan** | **[MorphScan.apk ⬇](../../releases/download/scan-v0.3.0/MorphScan.apk)** (belge tarayıcı) | 41 MB |

Bu bağlantılar **her zaman en son sürümü** verir. Tüm sürümler:
[Releases](../../releases)

---

## 2.7.0'da neler var

**Telefondan al.** Android için yeni **MorphScan** uygulamasıyla taradığınız
belgeyi, MorphSuite'teki QR kodu okutarak bilgisayara gönderirsiniz. Dosya
telefonda **uçtan uca şifrelenir**; aradaki sunucu içeriği ve dosya adını
göremez, dosyayı saklamaz. Telefonlar bir kez **eşleştirilir** (iki ekranda
aynı 6 haneli kod çıkar); yalnızca eşleşmiş telefonlar gönderebilir. İki
cihazın aynı ağda olması gerekmez.

**Ayarlar → İnternet bağlantısı.** Kapalıyken MorphSuite hiçbir sunucuya
bağlanmaz: güncellemeler denetlenmez, "Telefondan al" çalışmaz. Tamamen
çevrimdışı kullanmak isteyenler için.

**Pardus için .deb paketi.** Çift tıklayınca Pardus paket yükleyicisi açılır;
`sudo apt install ./MorphSuite_Pardus.deb` ile de kurulur,
`sudo apt remove morphsuite` ile kaldırılır. Güncellemeler yine program
içinden gelir.

**MorphScan (Android) 0.3.0.** Kâğıdın kenarlarını bulup düzelten, çok
sayfalı PDF yapan tarayıcı: fotoğrafları bozmayan belge filtresi, tam ekran
sayfa görüntüleyici, sayfa sıralama. Play Store'da değil; kurarken Android
"bilinmeyen kaynak" izni ister. Yeni sürüm çıkınca açılışta haber verir.

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

Önerilen: `MorphSuite_Pardus.deb` dosyasına çift tıklayın ya da:

```bash
sudo apt install ./MorphSuite_Pardus.deb
```

Yönetici hakkınız yoksa: arşivi ve `kur.sh`'ı **aynı klasöre** indirin:

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
| **CMP** | MorphCompress | PDF, görsel ve Word dosyalarını küçültür (DYS sınırı için) |
| **MRG** | MorphMerge | Birleştirme; hangi sayfaların alınacağını seçme, kartlarla sürükle-bırak düzenleme, bölme ve ayıklama, numaralama |
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
