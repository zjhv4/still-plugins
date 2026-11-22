# Google Earth View compatibility source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.google-earth-view` |
| Status | Compatibility |
| Access | User-supplied authorized HTTPS JSON catalog |
| Capabilities | List, random |

The former gallery has no stable public API, so `catalog_url` is required. The plugin accepts only the
documented schema v1 catalog object. Optional `region` filters country or region. The catalog and every
image still pass host HTTPS and SSRF checks.

```bash
wallpaper-cli source import org.wallpaper.source.google-earth-view --limit 1 \
  --set catalog_url=https://example.org/authorized-earth-view.json
```

Catalog operators must have permission to distribute the catalog and its referenced imagery.
