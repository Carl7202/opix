# opix

A simple one-to-one chat app built with plain HTML, CSS and JavaScript, Supabase anonymous Auth, Postgres and Realtime.

## Features

- Opens straight into chat with no signup or login screen
- Automatic guest identity with an editable display name
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

The frontend is already configured for the opix Supabase project. Its publishable key is intended for browser use; the database is protected by row-level security. Never add a Supabase secret or service-role key to this repository.

## Guest identity

Opix creates a guest session automatically and stores it in the browser. There is no email, password, signup, or login flow. A guest account cannot be recovered after clearing browser data or switching devices, so keep the same browser data to retain access to that identity.

## Security note

Messages are private to the two conversation participants through RLS. This app does not provide end-to-end encryption; Supabase stores message contents in the database.
