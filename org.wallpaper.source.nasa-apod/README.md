# NASA APOD source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.nasa-apod` |
| Status | Stable |
| Access | Official NASA APOD Basic JSON API |
| Capabilities | List, random |

The source uses [NASA APOD Basic](https://api.nasa.gov/assets/files/apod/APOD-APIs-and-RSS-info.pdf)
at `science.nasa.gov`, including its full-size image, original page, explanation and image credits.
Video entries and entries without an HTTPS image are excluded. HTML in explanations and credits
is converted to readable text.

`history_days` is 1–730. Lists page backward through this range in groups of at most 25 dates;
random requests select a date window using the host-provided random seed. The public feed needs
no API key. Updating from configuration version 1 preserves the history range and removes the
obsolete `api_key` and `hd_only` settings; credentials are never sent to the new API.

```bash
wallpaper-cli source import org.wallpaper.source.nasa-apod --operation random --limit 1
```
