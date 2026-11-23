# Reddit source

| Field | Value |
| --- | --- |
| Plugin ID | `org.wallpaper.source.reddit` |
| Status | Experimental |
| Access | Registered app and OAuth Data API |
| Capabilities | List |

Enter `oauth_token` on each desktop source-instance card. Optional `client_id`, `client_secret` and
`oauth_refresh_token` let the host refresh an expiring access token silently and remember the result
in the same portable database. No token is read from an environment variable or OS credential store.
Configure `source_type`, `name`, `sort`, `period`, and `allow_nsfw`. Deleted posts and non-image
submissions are ignored; NSFW is off by default. The Bearer token is injected only into
`oauth.reddit.com` requests and is never forwarded to image CDNs.

Each Reddit instance can contain multiple subreddit or user definitions, and multiple Reddit
instances keep authorization and download directories separate.

Direct HTTPS images from `i.redd.it`, `preview.redd.it` and `i.imgur.com` are
supported. When present, the direct original is preferred over Reddit's resized
preview; preview dimensions are not attached to the original. Otherwise a Reddit
image preview can be used. Imgur album pages and extensionless share pages are not
treated as image files. User listings send the selected sort and top time range.
