# Katkıda Bulunma Rehberi

Bu proje, Context7 MCP kurulumu ve sorun gidermesi hakkında topluluk katkılarına açıktır. Katkıda bulunmak için aşağıdaki yönergeleri izleyin.

## Nasıl Katkıda Bulunabilirsiniz?

Context7 MCP Troubleshooting projesine katkıda bulunmanın birçok yolu vardır:

### 1. Dokümantasyon İyileştirmeleri

- Mevcut rehberlerdeki hata veya eksiklikleri düzeltme
- Yeni kullanım senaryoları veya örnekler ekleme
- Adım adım talimatları iyileştirme veya netleştirme
- Dil veya formatlama düzeltmeleri

### 2. Yeni İçerik

- Ek sorun giderme rehberleri
- Farklı ortamlar için yapılandırma örnekleri (Linux, macOS vb.)
- Farklı IDE'ler veya AI asistanları için entegrasyon adımları
- Sık sorulan sorular (SSS) eklemeleri

### 3. Teknik İyileştirmeler

- Jekyll tema özelleştirmeleri
- SEO optimizasyonları
- Erişilebilirlik iyileştirmeleri
- GitHub Pages işlevselliği eklemeleri

## Katkıda Bulunma Süreci

### 1. Bir Issue Açın

Büyük değişiklikler yapmadan önce, lütfen bir GitHub Issue açın ve ne yapacağınızı açıklayın. Bu, çaba tekrarını önlemeye ve değişikliklerinizin projenin hedefleriyle uyumlu olmasını sağlamaya yardımcı olur.

### 2. Fork ve Clone

1. Bu depoyu (repository) kendi GitHub hesabınıza fork edin
2. Fork'unuzu yerel makinenize klonlayın:
   ```
   git clone https://github.com/[kullanıcı-adınız]/context7-mcp-troubleshooting.git
   cd context7-mcp-troubleshooting
   ```

### 3. Branch Oluşturun

Değişiklikleriniz için yeni bir branch oluşturun:
```
git checkout -b [branch-adı]
```

Branch adınızın değişikliğinizi tanımlamasına dikkat edin, örneğin:
- `feature/vscode-integration`
- `fix/windows-path-typo`
- `docs/linux-installation`

### 4. Değişiklikleri Yapın

- Jekyll yapısına dikkat edin
- Mevcut formatlamayı ve stilleri takip edin
- Açık ve anlaşılır dokümantasyon yazın
- Gerektiğinde ekran görüntüleri veya diyagramlar ekleyin

### 5. Test Edin

Değişikliklerinizi yerel olarak test edin. Jekyll ile şu şekilde bir test sunucusu çalıştırabilirsiniz:

```
bundle exec jekyll serve
```

### 6. Commit ve Push

Değişikliklerinizi commit edin ve branch'inizi GitHub'a push edin:

```
git add .
git commit -m "Açıklayıcı commit mesajı"
git push origin [branch-adı]
```

### 7. Pull Request Oluşturun

GitHub'da fork'unuzdan ana depoya bir Pull Request oluşturun.
PR açıklamanızda:
- Değişikliklerinizin ne olduğunu açıklayın
- İlgili Issue numarasını belirtin (varsa)
- Hangi sorunu çözdüğünüzü veya hangi özelliği eklediğinizi belirtin

## Kod ve Dokümantasyon Standartları

- Açık ve tutarlı Markdown formatlaması kullanın
- Teknik terimler için tutarlı terminoloji kullanın
- Çevrilmemesi gereken teknik terimleri İngilizce olarak bırakın
- Komutları ve kod bloklarını kod formatında işaretleyin
- Ekran görüntüleri eklerken net ve odaklanmış olmasına dikkat edin

## Tartışmalara Katılın

Sorularınız veya önerileriniz varsa [Discussions](https://github.com/akmaster/context7-mcp-troubleshooting/discussions) bölümünü kullanarak toplulukla etkileşime geçebilirsiniz.

## Lisans

Bu projeye katkıda bulunarak, katkılarınızı projenin [MIT Lisansı](LICENSE) altında lisansladığınızı kabul edersiniz.

---

Değerli katkılarınız için şimdiden teşekkür ederiz!
