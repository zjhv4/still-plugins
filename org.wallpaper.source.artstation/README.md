# ArtStation source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.artstation` |
| Status | Stable |
| Access | Public first-party artist `projects.json` feed |
| Capabilities | List |

Set `artist` to a username, portfolio URL or artist RSS URL such as
`https://www.artstation.com/USERNAME.rss`. These inputs resolve to the same public
portfolio JSON endpoint. Individual artwork URLs are rejected with a configuration
error rather than mistaken for an artist. `allow_nsfw` defaults to false. The adapter does not
scrape profile pages; artist, project permalink, adult flag, and original image variants come from
the public portfolio JSON response.

Each project image is a separate library item with its own asset ID. Original and
display URLs are variants of that image; different project images are never used
as resolution alternatives. The plugin pages through the complete portfolio,
including projects with multiple images, without decoding every project on each
request. Existing page-number cursors are accepted when upgrading.

```bash
wallpaper-cli source import org.wallpaper.source.artstation --limit 2 --set artist=wlop
```
