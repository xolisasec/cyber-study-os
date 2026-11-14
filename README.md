# Cyber Study OS

A dark, responsive study tracker with private Supabase email/password authentication and cloud-stored study history.

## Included
- Three daily Done controls: Professor Messer (2h), Professor Messer (2h), Cisco Python (2h; choose Essentials 1 or 2).
- Live daily pie chart, daily/weekly/monthly hours, study streak, course progress, history and CSV export.
- LinkedIn daily caption helper and editable course-hour planning targets.
- Supabase authentication, per-user Row Level Security and cloud database storage.

## Setup
1. Create a project at https://supabase.com/.
2. In the project's SQL Editor, run the complete `supabase/schema.sql` file.
3. In Supabase project API settings, copy the Project URL and the publishable key (or legacy anon key).
4. Create a GitHub repository and upload `index.html`, `README.md` and the `supabase` folder.
5. In GitHub, open Settings → Pages → Deploy from a branch; select `main` and `/ (root)`.
6. Open the published GitHub Pages site. Choose Connect Supabase and paste the Project URL and publishable/anon key.
7. Create an account. If email confirmation is enabled, confirm your email and then sign in. Add the GitHub Pages URL to Supabase Authentication → URL Configuration → Redirect URLs if needed.

## Security
- Never paste a Supabase service-role or secret key into the website or GitHub. Use only the publishable/anon key.
- The included SQL enables Row Level Security and restricts each account to rows where `user_id = auth.uid()`.
- GitHub hosts the app code; Supabase stores the private journal data. Signing in on another device loads the same records.
- Keep your email and password private. Export CSV periodically as an additional backup.

## Notes
Study blocks are displayed as Professor Messer 09:00–11:00, Professor Messer 11:00–13:00, and Cisco Python 14:00–16:00. Course progress targets are editable planning estimates, not official course-duration guarantees or exam-readiness measures.
