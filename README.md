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

## 2.6.0'da neler var

**MorphMerge artık bir sayfa düzenleyici.** Birleştirilecek dosyaları
eklerken **hangi sayfaların alınacağını seçebilirsiniz**: bir dosyadan
yalnızca kapak sayfalarını, ötekinden içeriği, üçüncüsünden kaynakçayı.
Sayfalar tek tek tıklanarak, sürüklenerek ya da `1-3, 7, 10-` gibi bir
aralık yazılarak seçilir; 59 dosya da eklense tek pencere açılır.

**Kart görünümü.** Bütün sayfalar kartlar hâlinde yan yana dizilir.
Sürükleyerek sıralayabilir, farklı dosyaların sayfalarını birbirinin arasına
koyabilir, döndürebilir, çoğaltabilir ya da silebilirsiniz. Her kartın
renkli şeridi hangi dosyadan geldiğini gösterir. Binlerce sayfada da akıcı.

**Dışarı al ve böl.** Seçili sayfaları ayrı bir PDF olarak alabilir ya da
belgeyi her N sayfada, her kaynak dosyada, seçili sayfalardan itibaren veya
elle yazdığınız aralıklarda parçalara bölebilirsiniz.

**MorphSlice'ın yeni adı MorphCompress.** Araç artık sıkıştırmaya
odaklanıyor: PDF, görsel ve Word dosyalarını hedef boyuta indirir ve **tek
dosya** olarak verir. DYS sınırına sığmayan dosyalar için parçalara bölme
isteğe bağlı bir seçenek olarak duruyor. Ayarlarınız korunur.

**Kurulum düzeltmeleri.** Kaldırma artık yalnızca Ayarlar → Uygulamalar'dan
yapılıyor; eski `.bat` kaldırıcı kurulumu yarım bırakabiliyordu, çıkarıldı.
MorphViewer, Windows'un "Varsayılan uygulamalar" listesinde PDF için
seçilebilir hâle geldi; kurulumun sonunda bu ayar sayfası açılabiliyor.

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
