# ig-callback

A minimal OAuth callback page for the **Instagram Unfollowers** iOS app. When Instagram redirects back after OAuth, this page captures the query parameters and immediately deep-links the user back into the native app.

## How It Works

1. Instagram redirects to this page with query params (e.g., `?code=...`)
2. The page reads all URL params and redirects to: `instagramunfollowers://oauth/callback?<params>`
3. The user sees a brief "Redirecting back to app…" message before being taken to the app

## Tech Stack

- Plain HTML + vanilla JavaScript (single file, no dependencies)

## Deployment

Host as a static file anywhere (GitHub Pages, Vercel, Netlify, etc.) and configure the URL as the OAuth redirect URI in your Instagram app settings.
