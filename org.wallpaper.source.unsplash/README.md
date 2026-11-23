# Unsplash source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.unsplash` |
| Status | Stable |
| Access | Official Unsplash API v1 |
| Capabilities | List, search, random |

Enter `access_key` on each desktop source-instance card. The host remembers it in that instance's
portable SQLite credential row; it is not read from an environment variable or OS credential store.
`mode` supports latest, random, search,
user, collection, and topic; `identifier` supplies the relevant query or ID. On import, the host
calls the provider's typed download-tracking endpoint before downloading the returned CDN URL and
never forwards the API key to the CDN.

Create as many Unsplash instances as needed, then add independent search, user, collection or topic
contents inside each instance.

`identifier` also accepts Unsplash page links: `https://unsplash.com/@USERNAME`,
`/collections/ID/NAME`, `/t/TOPIC`, or `/s/photos/QUERY`. The link selects the matching
API resource automatically; unsupported pages are reported before fetching. Page
query parameters never supply credentials. Random requests retain their random
endpoint and can filter by the linked user, collection, or topic.
