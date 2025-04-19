---
layout: default
title: "Tags"
permalink: /tags/
---

# Content Tags

Explore guides by topics:

<div class="tag-cloud">
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <a href="{{ '/tags/' | append: tag[0] | relative_url }}" 
       style="font-size: {{ tag[1].size | times: 4 | plus: 80 }}%">
       {{ tag[0] }}
    </a>
  {% endfor %}
</div>

## All Tags

<ul class="tag-list">
  {% for tag in site.tags %}
    <li>
      <a href="{{ '/tags/' | append: tag[0] | relative_url }}">
        {{ tag[0] }} ({{ tag[1].size }})
      </a>
    </li>
  {% endfor %}
</ul>

## Topics

### Installation and Configuration

- [Installation Guide]({{ '/installation-guide/' | relative_url }})
- [Configuration Examples]({{ '/configuration-examples/' | relative_url }})

### Troubleshooting

- [Troubleshooting Guide]({{ '/troubleshooting-guide/' | relative_url }})
- [Spawn EINVAL Error]({{ '/tags/spawn-einval/' | relative_url }})
- [Not Connected Error]({{ '/tags/not-connected/' | relative_url }})

### Operating Systems

- [Windows]({{ '/tags/windows/' | relative_url }})
- [Linux]({{ '/tags/linux/' | relative_url }})
- [macOS]({{ '/tags/macos/' | relative_url }})

### Applications

- [Cursor]({{ '/tags/cursor/' | relative_url }})
- [VS Code]({{ '/tags/vscode/' | relative_url }})
- [Claude Desktop]({{ '/tags/claude-desktop/' | relative_url }})
