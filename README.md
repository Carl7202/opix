# opix

One shared community chat with separate text channels, voice rooms and a live online member list.

## Features

- Enter a display name and jump straight in
- No signup, email, password or login screen
- One shared community for everyone
- Text channels: #general, #memes, #gaming and #off-topic
- Voice rooms: Lounge and Gaming
- Live online member list — people already in opix appear automatically
- Live channel messages saved in Supabase
- Change your display name in Settings
- Responsive desktop and mobile layout

## Stack

- Static frontend: GitHub Pages
- Backend: Supabase Auth, Postgres and Realtime
- Voice: browser WebRTC audio

## Deploy

1. Open the repository's **Settings → Pages**.
2. Set the source to **Deploy from a branch**, choose `main` and `/ (root)`.
3. Save and wait for GitHub Pages to publish.
4. In Supabase, open **Authentication → Providers → Anonymous Sign-Ins** and enable anonymous sign-ins.

The frontend is configured for the opix Supabase project. Its publishable key is intended for browser use; the database is protected by row-level security. Never add a Supabase secret or service-role key to this repository.

## Guest identity

Visitors enter a display name once. Opix creates an anonymous guest session behind the scenes; there is no signup or login flow. The guest identity is retained in that browser, so clearing browser data or switching devices can make it inaccessible.

## Voice chat note

Voice uses direct browser-to-browser WebRTC connections with public STUN servers. Microphone permission and HTTPS are required. Some networks or routers block direct peer connections; this simple version does not include a paid TURN relay service, so voice may not connect on every network.