# Self-Attendance

A daily register. Mark what you showed up for, watch the percentage move across months.

Plain HTML, CSS and JavaScript — no build step, no framework, no backend. Data is stored in
`localStorage`, which means it lives on the device you use it on and never leaves it.

## Putting it online

1. Make a GitHub account if you don't have one.
2. New repository → name it `attendance` → **Public** → Create.
3. On the repo page: **Add file → Upload files**. Drag in every file from this folder
   (`index.html`, `manifest.webmanifest`, `sw.js`, and the four `.png` icons). Commit.
4. **Settings → Pages**. Under *Build and deployment*, set Source to
   **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. Wait about a minute, then refresh. The URL appears at the top:
   `https://<your-username>.github.io/attendance/`

## Putting it on your home screen

Open that URL on your phone.

- **Android / Chrome:** menu (⋮) → *Add to Home screen* (or *Install app*).
- **iPhone / Safari:** Share → *Add to Home Screen*.

It opens without a browser bar, keeps working with no internet, and looks like any other app.

## Your data

Stored per device, per browser. Marks made on your phone don't appear on your laptop.

- **Back up** downloads a `.json` file of everything.
- **Restore** loads one back — that's how you move to a new phone.
- Clearing browser site data will wipe it. Back up occasionally.

## Changing it yourself

Everything is in `index.html`. Worth opening even if you don't touch it:

- `DEFAULTS` near the top of the `<script>` — the starting list of rows.
- `line()` — the sentence under the checklist. Change the wording to whatever you'd
  actually want to read at 1am.
- `pct()` — the attendance maths. Days count from the first day you marked anything,
  through today. Skipped days count as absent on purpose.
- `:root` in the `<style>` block — every colour in the page.

Edit the file, upload it again, and the live site updates.
