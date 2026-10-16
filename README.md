# MorphSuite — İndirme

**Günlük belge işlerini tek çatı altında toplayan, üyelik gerektirmeyen
bir masaüstü araç takımı.**

Belgeleriniz bilgisayarınızdan çıkmaz. Hiçbir buluta gönderilmez, kullanım
verisi toplanmaz, hesap açmanız gerekmez.

---

## İndir

| | Platform | Dosya | Boyut |
|---|---|---|---|
| 🪟 | **Windows 10 / 11** | **[MorphSuite_Kurulum.exe ⬇](../../releases/latest/download/MorphSuite_Kurulum.exe)** | 154 MB |
| 🐧 | **Pardus (.deb)** | **[MorphSuite_Pardus.deb ⬇](../../releases/latest/download/MorphSuite_Pardus.deb)** | 135 MB |
| 🐧 | **Pardus / Linux (arşiv)** | **[MorphSuite_Linux.tar.gz ⬇](../../releases/latest/download/MorphSuite_Linux.tar.gz)** (kur.sh içinde) | 181 MB |
| 📱 | **Android — MorphScan** | **[MorphScan.apk ⬇](../../releases/download/scan-v0.3.0/MorphScan.apk)** (belge tarayıcı) | 41 MB |

Bu bağlantılar **her zaman en son sürümü** verir. Tüm sürümler:
[Releases](../../releases)

---

## 2.8.0'da neler var

**Yalnız kullandığınız programları yükleyin.** Kurulum artık çok daha küçük:
MorphViewer her zaman, MorphPDF isteğe bağlı kurulur. Öteki programları
kurulum sihirbazında **seçebilir** ("Tüm programlar" ya da "Özel seçim")
ya da sonradan MorphSuite içinden **Yükle** ile ekleyip **Kaldır** ile
çıkarabilirsiniz. Gerekmeyen program diskte yer tutmaz.

**İki görünüm.** **Izgara** tüm programları gösterir; yüklü olmayanların
altında "Yükle" yazar. **Sade** yalnız yüklü programları gösterir, sağ
alttaki **+** ile program eklenir. Seçtiğiniz görünüm hatırlanır.

**MorphPDF.** Metni taşırken ya da kenarından büyütürken kopyasının
kalması, eski yerinde iz (beyaz kutu, alt çizgi) kalması ve yanındaki
metinden harf silinmesi giderildi. Seçili öğe **Delete** tuşuyla silinir.

**MorphSign.** E-postayla imza isteme (davetler imza@morphsuite.app'ten
gider, belge uçtan uca şifreli), e-imza kartıyla imzalama, Adobe Sign
gibi imza bandı, önizlemede yakınlaştırma ve sayfa şeridi.

---

## Kurulum

### Windows

İndirdiğiniz `MorphSuite_Kurulum.exe` dosyasına çift tıklayın. Kurulum
sihirbazı açılır: **herkes için mi yoksa yalnızca siz mi** kurulacağını,
**hangi klasöre** kurulacağını, **hangi programların** kurulacağını ve
**PDF dosyalarının MorphViewer ile açılmasını** isteyip istemediğinizi sorar.
Seçtiğiniz ek programlar kurulum sırasında indirilir.

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

Yönetici hakkınız yoksa: `MorphSuite_Linux.tar.gz` arşivini indirin, `kur.sh` içinde gelir:

```bash
tar -xzf MorphSuite_Linux.tar.gz
cd Morph
./kur.sh          # sadece bu kullanıcı
sudo ./kur.sh     # tüm kullanıcılar
```

Kurulum, PDF dosyalarının varsayılan olarak MorphViewer ile açılmasını **bir
kez sorar**; hayır derseniz "Birlikte aç" menüsünden her zaman seçebilirsiniz.
OCR için sistemde `tesseract-ocr` paketi gerekir.

Paket MorphViewer ve MorphPDF ile gelir; MorphSuite ilk açılışta öteki
programları seçip yükleyebileceğiniz pencereyi gösterir.

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
| **GRD** | MorphGuard | KVKK karartma (TC kimlik, IBAN, telefon, e-posta — kalıcı silme ve doğrulama), PDF şifreleme ve izinler, gizli bilgi temizliği |
| **SIGN** | MorphSign | İmza isteme (e-postayla, Adobe Sign gibi), e-imza kartıyla imzalama, imza doğrulama |
| **BATCH** | MorphBatch | Toplu işlem: karartma, damga, sıkıştırma, imza adımlarını sırayla birçok dosyaya uygular |
| **FORM** | MorphForm | PDF formlarını doldurma; bilgiler projede saklanır, asıl form değişmez |

MorphViewer dışındaki programlar isteğe bağlıdır: kurulumda seçilir ya da
MorphSuite içinden yüklenir / kaldırılır.

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
