# Linear Calendar

A whole-year linear calendar in a single HTML file. Each month is one row with the weekdays lined up in columns, so you can see the entire year at a glance and plan trips, projects and holidays across it.

No install, no build step, no server, and no account. Open `index.html` in a browser, or host it on GitHub Pages.

## Features

- **One year on one screen.** Weekends are shaded and today is outlined.
- **Click or drag across days to add an event.** Events can span weeks and run into the next month.
- **Click an event to edit or delete it.** Overlapping events stack in their own lanes.
- **Colour-coded categories** that you can show or hide, rename, recolour, add and delete.
- **Two layouts.** Weekdays aligned, or dates aligned (every month starts in column 1). The week can start on Monday or Sunday.
- **Themes.** Default, Gruvbox, Nord, Dracula, Solarized, Catppuccin, Tokyo Night, One (Atom), Everforest and Rosé Pine, each in a light and a dark version. Auto mode follows your system setting.
- **Auto-save to a file** of your choice (Chrome and Edge).
- **Export and import** `.json` backups, and import `.ics` files from Google Calendar or Outlook.
- **Print-ready.** The year fits on one landscape A4 page and always prints in the light version of the theme.

### Keyboard shortcuts

| Key | Action |
| --- | --- |
| `←` / `→` | Previous / next year |
| `T` | Jump to the current year |
| `Esc` | Close a dialog |

## Running it

**Locally:** double-click `index.html`.

**From anywhere (GitHub Pages):**

1. Push this folder to a GitHub repository.
2. In the repo, go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, then pick `main` and `/ (root)`.
3. After a minute or so the calendar is live at `https://<your-username>.github.io/<repo-name>/`.

On a free GitHub account, Pages only works with public repos. That's fine here, because the repo only holds the app and none of your calendar data (see below).

## Where your data lives

Your events are **never stored in this repo or on any server**. They're kept in two places:

1. **Browser storage.** This happens automatically, but each browser on each computer has its own separate copy. Clearing "cookies and site data" erases it.
2. **A data file you choose** (recommended). Click **💾 Auto-save to file…** → **Create new file…** and every change is written to that `.json` file within about half a second.

### Using it on more than one computer

Keep the data file in a synced folder (OneDrive, Dropbox, Google Drive and so on). On each computer, open the calendar, then click **💾** → **Open existing file…** and pick that file. Every computer then reads and writes the same data.

### Good to know

- **Reconnecting:** when you reopen the calendar, the browser may ask permission to edit the file again. When the button shows **⚠ Reconnect**, click it. If the browser offers **"Allow on every visit"**, choose it and you won't be asked again.
- **Nothing gets lost while you're disconnected.** Changes are kept in the browser, and when you reconnect, the newer copy (browser or file) wins.
- **Browser support:** auto-saving to a file needs **Chrome or Edge**. Firefox and Safari can still use the calendar, but use **Export** for backups there.
- **Don't commit your data file to the repo.** The included `.gitignore` excludes all `.json` files, so even a data file or backup saved inside this folder won't be committed by accident.

## Importing from other calendars

**Import** accepts:

- **`.json`**: a backup made with **Export**. Importing one replaces the current calendar (it asks you first).
- **`.ics`**: an export from Google Calendar, Outlook, Apple Calendar and so on. These events go into an **Imported** category. Only the dates are kept (times are dropped), and repeating events are brought in once only.
