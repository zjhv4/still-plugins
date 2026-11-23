# Wallhaven source

Paste a `https://wallhaven.cc/search?...` link into `query` to reuse its search,
categories, purity, sorting, ordering, resolution, aspect ratio, color, top range
and seed filters. A `https://wallhaven.cc/tag/ID` link selects that tag. Page numbers
come from Still's pagination, and API keys always come from the host credential
field; keys in copied links are ignored. Random requests override the copied sort.

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
