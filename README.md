# Tanvir Adnan — Personal Hub

A responsive Bangla personal website starter with:
- Public profile and sample electronics project cards
- Supabase email/password sign-up and login
- Private notes stored in a database, with per-user Row Level Security
- Delete-note feature

## Important security notes
- This starter does not upload images yet; project cards are sample content.
- Do not store passwords, government IDs, financial secrets, or highly sensitive information in notes.
- Never place a Supabase `service_role` key in `app.js`. Only use the project's publishable/anon key in browser code.
- Private notes are protected by database Row Level Security (RLS). Do not disable RLS.
- The public profile and any content added to the public page can be seen by anyone.

## 1. Create the free database and login
1. Create a project at https://supabase.com/ (free tier availability/limits may change).
2. In the project dashboard, find the Project URL and publishable key (or legacy anon key).
3. Open `app.js`; replace `YOUR_SUPABASE_PROJECT_URL` and `YOUR_SUPABASE_PUBLISHABLE_OR_ANON_KEY`.
4. In Supabase, open **SQL Editor**, paste the contents of `schema.sql`, and run it.
5. In Supabase Authentication settings, configure email confirmation and your site's allowed redirect URLs. For first testing, sign up with your own email and verify it if confirmation is enabled.

## 2. Publish for free with GitHub Pages
1. Create/sign in to https://github.com/.
2. Create a new public repository, e.g. `tanvir-personal-hub`.
3. Upload `index.html`, `style.css`, `app.js`, and `schema.sql` (README optional). Do not upload any secret/service-role key.
4. In repository **Settings → Pages**, choose deploy from branch, select `main` and `/ (root)`, then save.
5. Wait for GitHub Pages to publish and open the URL shown there.
6. In Supabase Authentication URL settings, add that published URL to the allowed site/redirect URLs.

## 3. Test before sharing
- Open the public URL on your phone.
- Create your account and verify your email if required.
- Log in, save a test note, log out, then log in again.
- Check that another account cannot read your notes.
- Keep all personal/private data out of the public profile.

## 4. Customizing
Edit the text in `index.html` to update your public bio and sample projects. Do not add a home address or private phone number to the public page unless you intentionally want everyone to see it.

## Limitations
This is a starter project, not yet a full content-management system. Project cards are static sample cards; image uploads and editing public projects require additional database/storage features and policies. Hosting and database free-tier quotas can change.
