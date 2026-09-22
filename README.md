# KuzeyPet Sipariş Sistemi - Cloudflare Pages Paketi

Bu paket statik web uygulamasıdır. GitHub reposuna tüm dosyaları yükleyip Cloudflare Pages ile yayınlayabilirsiniz.

## Yayın
- Framework preset: None
- Build command: boş bırakın
- Build output directory: `/` veya boş/root

## Mail / ek dosya çalışma mantığı
- Mobil cihazlarda `Paylaş / Mail Gönder` butonu Excel sipariş dosyasını oluşturur ve Web Share API ile cihazın paylaşım ekranını açar. Kullanıcı Gmail/Outlook/Mail uygulamasını seçerse dosya ek olarak aktarılır ve cihazdaki mail hesabı kullanılır.
- Masaüstü veya Web Share API desteklemeyen tarayıcılarda güvenlik nedeniyle `mailto:` ek dosya iliştiremez. Bu durumda dosya indirilir ve mail taslağı açılır; kullanıcı indirilen Excel’i manuel ekler.

## Ürün listesi
`data/urunler.xlsx` dosyasını aynı kolon yapısıyla güncellerseniz sistem otomatik yeni ürünleri okur.


## Gömülü kaynak
Bu sürümde yüklediğiniz `urunler.xlsx` hem `data/urunler.xlsx` olarak paket içindedir hem de `embedded-products.js` içine Base64 olarak gömülmüştür. Normalde sistem `data/urunler.xlsx` dosyasını okur; dosyaya erişilemezse gömülü kaynaktan otomatik devam eder.
