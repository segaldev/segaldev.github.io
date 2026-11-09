# segaldev.github.io

Serves two things for [Hourbox](https://segaldev.github.io/hourbox/):

- `/` forwards to `/hourbox/`.
- `/__/auth/` holds Firebase's Google sign-in helper. Because it's served from the same site as the app, sign-in works in installed apps on Android, which otherwise block it.

The helper files are downloaded from the Firebase project by the **Refresh Firebase sign-in helper** workflow (`.github/workflows/auth-helper.yml`). It runs when the workflow changes, monthly, and on demand from the Actions tab. `.nojekyll` lets GitHub Pages serve the `__` folder.
