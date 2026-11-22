# Google Earth View compatibility source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.google-earth-view` |
| Status | Compatibility |
| Access | Community archive or user-supplied authorized HTTPS JSON catalog |
| Capabilities | List, random |

The default `catalog_url` points to the community-maintained Earth View archive. Its array format
supplies upstream image links, map links and locations. The plugin also accepts the documented
schema v1 catalog object for custom catalogs. Optional `region` filters country or region;
both formats support pagination and seeded random selection. Catalog and image requests pass
the host HTTPS and SSRF checks.

Archive entries do not supply photographer credits or a background story. These fields remain
empty; the original map link and location are retained. Custom schema v1 catalogs retain their
provided attribution. The archive is a finite historical collection, not a live official gallery.

```bash
wallpaper-cli source import org.wallpaper.source.google-earth-view --limit 1
```

Catalog operators must have permission to distribute the catalog and its referenced imagery.
