# Bing source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.bing` |
| Status | Experimental |
| Access | Bing homepage image archive |
| Capabilities | List |

Configuration: `market` defaults to `en-US`; `quality` is `uhd` or `1920x1080`. The copyright
notice and Bing detail link are preserved with every imported asset.

```bash
wallpaper-cli source import org.wallpaper.source.bing --limit 1 --set market=zh-CN --set quality=uhd
```
