# Hero graph photos

The landing page's hero animation shows 6 profile pictures and 6 life-event
photos. By default it loads real photography from the Unsplash CDN, and falls
back to built-in illustrated thumbnails if the network is unavailable.

To use your own photos instead (e.g. real app users' creations), drop files
into this folder with these exact names — they take priority automatically,
no code changes needed:

| File | Shown as |
|---|---|
| `profile-1.jpg` … `profile-6.jpg` | Circular profile pictures (square crops look best) |
| `event-sunset.jpg` | Nature / sunset polaroid |
| `event-wedding.jpg` | Wedding polaroid |
| `event-birthday.jpg` | Birthday polaroid |
| `event-festival.jpg` | Festival / Diwali polaroid |
| `event-beach.jpg` | Family day out polaroid |
| `event-balloons.jpg` | Celebration polaroid |

Keep them small (~200–400px on the short side, JPEG quality ~60) — they are
rendered at thumbnail size and the audience is on slow networks.
