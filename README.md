# MorphSuite — Sürümler / Releases

Bu depo **yalnızca yayınlanan sürümleri** barındırır: güncelleme manifesti
(`surum.json`) ve kurulum paketleri. Kaynak kod burada değildir.

*This repository holds published releases only — the update manifest and the
installers. No source code here.*

## İndirme / Download

En güncel sürüm: **[Releases](../../releases/latest)**

| Platform | Dosya | Boyut |
|---|---|---|
| Windows 10/11 | `MorphSuite_Kurulum.exe` | 483 MB |
| Pardus / Linux | `MorphSuite_Linux.tar.gz` + `kur.sh` | 375 MB |

## Kurulum

**Windows** — dosyayı çalıştırın. İmzasız olduğu için Windows "bilgisayarınızı
korudu" diyebilir: **Ek bilgi → Yine de çalıştır**.

**Pardus / Linux** — arşivi ve `kur.sh`'ı aynı klasöre açın:
```bash
tar -xzf MorphSuite_Linux.tar.gz
./kur.sh          # sadece bu kullanıcı
sudo ./kur.sh     # tüm kullanıcılar
```

## Güncelleme nasıl çalışıyor?

MorphSuite her açılışta bu depodaki `surum.json` dosyasını okur. Yeni sürüm
varsa sorar; hayır derseniz normal devam eder. Sunucuya ulaşılamazsa
"ulaşılamadı" der — **"güncelsiniz" demez**, çünkü bunu bilemez.

İstek anonimdir: kimlik bilgisi taşımaz, hiçbir kullanım verisi gönderilmez.

## Lisans

MorphSuite **AGPL-3.0** ile dağıtılır. Lisans metni, üçüncü taraf bileşen
listesi ve gizlilik açıklaması her kurulum paketinin kökünde bulunur.
