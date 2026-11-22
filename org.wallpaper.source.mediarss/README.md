# MediaRSS source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.mediarss` |
| Status | Stable |
| Access | User-supplied HTTPS Media RSS, Atom, or image RSS feed |
| Capabilities | List |

Configuration: `feed_url` is required. The host only requests the configured HTTPS origin; image
URLs extracted from the feed still pass public-address, size, and image-decoding checks. Media RSS
elements, enclosures, CDATA images, and escaped HTML images are supported.

```bash
wallpaper-cli source preview org.wallpaper.source.mediarss --set feed_url=https://example.org/feed.xml
wallpaper-cli source import org.wallpaper.source.mediarss --set feed_url=https://example.org/feed.xml
```

Attribution and reuse rights come from the selected feed and remain the user's responsibility.
