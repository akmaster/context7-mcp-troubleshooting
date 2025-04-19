---
layout: default
title: "Etiketler"
permalink: /tags/
---

# İçerik Etiketleri

Rehberleri konulara göre keşfedin:

<div class="tag-cloud">
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <a href="{{ '/tags/' | append: tag[0] | relative_url }}" 
       style="font-size: {{ tag[1].size | times: 4 | plus: 80 }}%">
       {{ tag[0] }}
    </a>
  {% endfor %}
</div>

## Tüm Etiketler

<ul class="tag-list">
  {% for tag in site.tags %}
    <li>
      <a href="{{ '/tags/' | append: tag[0] | relative_url }}">
        {{ tag[0] }} ({{ tag[1].size }})
      </a>
    </li>
  {% endfor %}
</ul>

## Konu Başlıkları

### Kurulum ve Yapılandırma

- [Kurulum Rehberi]({{ '/installation-guide/' | relative_url }})
- [Yapılandırma Örnekleri]({{ '/configuration-examples/' | relative_url }})

### Sorun Giderme

- [Sorun Giderme Rehberi]({{ '/troubleshooting-guide/' | relative_url }})
- [Spawn EINVAL Hatası]({{ '/tags/spawn-einval/' | relative_url }})
- [Not Connected Hatası]({{ '/tags/not-connected/' | relative_url }})

### İşletim Sistemleri

- [Windows]({{ '/tags/windows/' | relative_url }})
- [Linux]({{ '/tags/linux/' | relative_url }})
- [macOS]({{ '/tags/macos/' | relative_url }})

### Uygulamalar

- [Cursor]({{ '/tags/cursor/' | relative_url }})
- [VS Code]({{ '/tags/vscode/' | relative_url }})
- [Claude Desktop]({{ '/tags/claude-desktop/' | relative_url }})
