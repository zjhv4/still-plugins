# Wallhaven source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.wallhaven` |
| Status | Stable |
| Access | Official Wallhaven API v1 |
| Capabilities | List, search, random |

Filters include `query`, `sorting`, `categories`, `purity`, and `atleast`. Optional `api_key` can be
entered on each desktop source-instance card and is required by the provider for NSFW results. It is
remembered in portable SQLite and never read from the environment. Safe-only mode works without a key.

```bash
wallpaper-cli source import org.wallpaper.source.wallhaven --query landscape --limit 4
```
