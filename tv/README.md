# TAQ Parks TV launch-screen controls

`launch-config.json` controls the two launch panels used by the Google TV app.
Changes publish centrally and do not require a new APK or reinstalling the app.

## Timing

- `defaultDurationSeconds` sets the duration of both panels when a panel does not specify its own duration.
- Add `durationSeconds` inside `poweredBy` or an individual sponsor to override the default for only that panel.
- The app accepts values from 1 through 60 seconds.

## Panel content

Both `poweredBy` and each item in `sponsors` support:

- `heading`
- `name`
- `slogan`
- `imageUrl` (HTTPS only)
- `url`
- `footer`
- optional `durationSeconds`

Keep each sponsor `id` unique. `activeDays` accepts the full English weekday names
shown in the current example. If several sponsors are eligible on the same day,
the app rotates among them by calendar day.

## Artwork

Artwork may be stored in `tv/assets/` or at another public HTTPS image address.
The app downloads and caches valid images up to 8 MB. It retains its packaged TAQ
and RLR2Disney artwork as an offline fallback.
