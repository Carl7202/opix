# opix

A simple one-to-one chat app built with plain HTML, CSS and JavaScript, Supabase Auth, Postgres and Realtime.

## Features

- Email/password accounts with username profiles
- Username search and friend requests
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

The frontend is already configured for the opix Supabase project. Its publishable key is intended for browser use; the database is protected by row-level security. Never add a Supabase secret or service-role key to this repository.

## Accounts

Supabase email confirmation is enabled by default on hosted projects. New users may need to confirm their email before signing in.

## Security note

Messages are private to the two conversation participants through RLS. This app does not provide end-to-end encryption; Supabase stores message contents in the database.
