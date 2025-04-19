# GitHub Pages Kurulumu ve Google Search Console Doğrulama Adımları

GitHub repository'nizi Google Search Console ile doğrulamak için GitHub Pages'i etkinleştirmeniz gerekiyor. Bu sayede meta etiketi içeren index.html dosyanız web üzerinden erişilebilir olacak ve Google bu etiketi doğrulayabilecektir.

## GitHub Pages'i Etkinleştirme Adımları

1. GitHub'da repository'nize gidin: `https://github.com/akmaster/context7-mcp-troubleshooting`
2. Sağ üstteki "Settings" (Ayarlar) sekmesine tıklayın
3. Sol taraftaki menüden "Pages" seçeneğine tıklayın
4. "Source" bölümünde "Deploy from a branch" seçeneğini seçin
5. "Branch" kısmında "main" veya "master" (hangisi mevcutsa), ardından "/(root)" seçeneğini seçin
6. "Save" (Kaydet) düğmesine tıklayın

GitHub Pages'in etkinleştirilmesi birkaç dakika sürebilir. Etkinleştirme tamamlandığında, sitenize aşağıdaki URL'den erişebileceksiniz:

```
https://akmaster.github.io/context7-mcp-troubleshooting/
```

## Google Search Console'da Doğrulama Adımları

1. GitHub Pages etkinleştirildikten sonra, sitenizin canlı olduğunu doğrulayın (yukarıdaki URL'yi ziyaret edin)
2. Google Search Console'a dönün
3. HTML etiketini doğrulamak için "Doğrula" düğmesine tıklayın

Doğrulama başarılı olduktan sonra:

1. Search Console'da "Site Haritaları" bölümüne gidin
2. Yeni bir site haritası eklemek için "Yeni Site Haritası" alanına basit bir site haritası girin:
   ```
   index.html
   ```
3. "Gönder" düğmesine tıklayın

Bu adımlar tamamlandığında, GitHub Pages siteniz Google Search Console ile doğrulanmış olacak ve Google, içeriğinizi indekslemeye başlayabilecektir.

## Önemli Notlar

1. Meta etiketi doğrulama eklendiğinde, bunu repoda tutmaya devam edin.
2. Mümkünse, site için sitemap.xml dosyası da oluşturun ve ekleyin.
3. Google'ın sitenizi indekslemesi birkaç gün sürebilir.
4. GitHub Pages, ücretsiz ve kolay bir çözüm olmakla birlikte bazı sınırlamaları vardır.

Google Analytics eklemeyi düşünüyorsanız, index.html dosyasına Analytics izleme kodunu da ekleyebilirsiniz.
