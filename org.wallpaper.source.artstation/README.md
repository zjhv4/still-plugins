# ArtStation source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.artstation` |
| Status | Stable |
| Access | Public first-party artist `projects.json` feed |
| Capabilities | List |

Set `artist` to a username or portfolio URL. `allow_nsfw` defaults to false. The adapter does not
scrape profile pages; artist, project permalink, adult flag, and original image variants come from
the public portfolio JSON response.

```bash
wallpaper-cli source import org.wallpaper.source.artstation --limit 2 --set artist=wlop
```
