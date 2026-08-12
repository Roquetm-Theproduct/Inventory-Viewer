# The Product

Fresh build. Separate from any other project — own repo, own Supabase project, own credentials.

## Files
- `index.html` — the app shell (login screen + nav). Open it directly in a browser to preview.
- `assets/logo.png` — your logo.

## Setup

### 1. GitHub
- Create a new **private** repo (don't reuse an existing one).
- Push these files as the first commit.

### 2. Supabase
- Create a new Supabase project at [supabase.com](https://supabase.com) — don't reuse an existing project.
- Go to **Project Settings → API** and copy:
  - **Project URL**
  - **anon public** key (not the `service_role` key — that one should never go in client-side code)
- Open `index.html`, find this block near the top of the `<script>` tag, and fill it in:

  ```js
  const SUPA_URL = '';   // paste your Project URL
  const SUPA_KEY = '';   // paste your anon public key
  ```

### 3. Run locally
Just open `index.html` in a browser — no build step needed. Once Supabase is filled in, the "Not configured" banner and status dot will clear up.

## What's next
This shell only has a login screen and an empty dashboard tab. From here we add:
- Supabase Auth wiring (real sign-in)
- Database tables (via SQL run in Supabase's SQL Editor)
- Additional nav tabs / pages, one at a time
