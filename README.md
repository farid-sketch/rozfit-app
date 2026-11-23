# RozFit — free workout app (Android first)

A free personal trainer in your phone: onboarding, BMI, weekly gym or home plan, daily checklist,
rest timer, streaks, calorie/protein targets and Pakistani diet tips. Everything runs on the phone;
there is no server, no login and no running cost.

## Files
| File | What it is |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Lets Android "install" it like a normal app (icon, name, full screen) |
| `sw.js` | Makes it open without internet after the first visit |
| `icons/` | App icons |

## Cheapest launch plan

| Step | What | Cost | Who |
|---|---|---|---|
| 1 | Put the files in a new GitHub repo and turn on GitHub Pages. This gives a free https link. | Free | Claude (needs Farid's yes) |
| 2 | Share the link. On Android, Chrome shows "Install app" and it sits on the home screen like any app. | Free | Farid |
| 3 | Get 12+ friends or gym members testing it for 14 days (Google requires this for new personal Play accounts before going public). | Free | Farid |
| 4 | Wrap the same link into a Play Store app with Google's free Bubblewrap tool (Trusted Web Activity). | Free | Claude |
| 5 | Open a Google Play developer account and publish. | **$25 one time** | Farid (needs ID verification) |
| 6 | Later: own domain, e.g. rozfit.pk / .app | ~$10–15 a year (optional) | Farid |
| 7 | Later: AI how-to videos. Add each video link to the `VIDEOS` list in `index.html`. | When needed | Claude |

## How to add a video later
In `index.html`, find `const VIDEOS = {` and add a line per exercise, using the exact exercise name:

```js
"Push-ups": "https://example.com/videos/push-ups.mp4",
```

Until a video is added, the app shows "Video coming soon" plus a free YouTube search link.

## Known limits of this version
- Progress is saved on the phone only. Changing phone or clearing Chrome data loses it.
- Plans are rule-based (not AI). They cover 1–7 days a week, gym or home, beginner to advanced.
- General guidance only, not medical advice (a note says so in the app).
