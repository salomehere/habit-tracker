# Habits

A phone-first habit tracker (Habit Cloud–style). Single static page, no build step.
Habit data is stored in the browser at whatever URL you host it on — the file just
provides the starting state on a fresh device.

## One-time setup

1. **Create a new repo** (e.g. `habit-tracker`) and add these files to the root:
   - `index.html`
   - `netlify.toml`
   - `README.md`
2. **Netlify → Add new site → Import an existing project**, pick the repo.
   No build command, publish directory `.` (the `netlify.toml` already sets this).
3. Once deployed, **rename the site** in Netlify → *Site configuration → Change site name*
   to something memorable, e.g. `salome-habits` → `salome-habits.netlify.app`.
4. On your phone, open the URL → **Share → Add to Home Screen**. Launches full-screen.
5. Open it once — habits, history, holidays and Netball are already there.
6. **Settings → Export backup** and keep the file. Safety net.

## Updating later

Commit a new `index.html` to the repo. Netlify auto-deploys. Your saved data carries
over because it lives in the browser, keyed to the URL — the new file is ignored after
first run.

## Two rules that protect your data

- **One URL, forever.** Storage is bonded to the web address. Pick the site name once
  and never change it.
- **Don't also run a downloaded copy of the file.** A local file and the hosted site are
  separate storage boxes and won't share history. The hosted URL is the real app.

## Backups

`Settings → Export backup` downloads a full JSON snapshot. `Settings → Import` restores
one (it also reads native Habit Cloud exports directly).
