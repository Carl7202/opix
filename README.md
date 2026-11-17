# opix

A simple one-to-one chat app built with plain HTML, CSS and JavaScript, Supabase anonymous Auth, Postgres and Realtime.

## Features

- Enter a display name and go straight into chat
- No signup, email, password, or login screen
- Guest identity is retained in the same browser
- Change your display name in Settings
- Display-name search and friend requests
- Private one-to-one conversations
- Persistent messages with live updates
- Basic online/last-seen status
- Responsive layout for desktop and mobile

## Stack

- Static frontend: GitHub Pages
- Backend: Supabase
- Client: `@supabase/supabase-js` 2.119.0

## Deploy

1. Open the repository's **Settings → Pages**.
2. Set the source to **Deploy from a branch**, choose `main` and `/ (root)`.
3. Save and wait for GitHub Pages to publish.
4. In Supabase, open **Authentication → Providers → Anonymous Sign-Ins** and enable anonymous sign-ins.

The frontend is configured for the opix Supabase project. Its publishable key is intended for browser use; the database is protected by row-level security. Never add a Supabase secret or service-role key to this repository.

## Guest identity

Visitors simply enter a display name. Opix creates an anonymous guest session behind the scenes; there is no signup or login flow. The guest identity is stored in the browser, so clearing browser data or switching devices can make it inaccessible.

## Security note

Messages are private to the two conversation participants through RLS. This app does not provide end-to-end encryption; Supabase stores message contents in the database.
