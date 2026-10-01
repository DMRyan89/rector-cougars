# Rector Elementary — Schedules app

A small website that staff save to their phone's home screen. Only you edit it, right here on GitHub.

## One-time setup (about 5 minutes)

1. Create a new **private or public repository** on GitHub (public is fine — the schedule isn't secret, and GitHub Pages is free for public repos). Upload every file and folder from this download, keeping the folder structure.
2. In the repo go to **Settings → Pages**. Under *Build and deployment* choose **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
3. After a minute GitHub shows your link, like `https://yourname.github.io/rector-schedules/`. That's the link you give staff.

Nobody else can change anything unless you add them as a collaborator on the repo.

## How staff install it

Send them the link. When it opens:

- **iPhone (Safari):** tap the Share button → **Add to Home Screen** → Add.
- **Android (Chrome):** tap the ⋮ menu → **Add to Home screen** (or **Install app**).

It then opens like an app, with a Rector icon. It always shows the latest thing you've posted (and still opens if they lose signal).

## Editing schedules (no coding needed)

All the content lives in three text files inside the `data` folder. Open a file on GitHub, click the pencil (Edit), make your change, then **Commit changes**. Staff see it the next time they open the app.

### `data/periods.json` — the regular daily schedule for each grade
One list per grade (`"K"` through `"6"`). Each period has a name, a start, and an end in 24-hour time:

```
{ "name": "Math", "start": "09:20", "end": "10:20" }
```

This is what drives the countdown bar at the top of the app.

### `data/days.json` — anything different on a specific date
Add a date, then say what's different for `"all"` grades or for one grade:

```
"2026-10-30": {
  "all": { "note": "Fall festival — pajama day!" },
  "2":   { "note": "Class party 1:30", "file": "files/2026-10-30-grade2.pdf" }
}
```

Each entry can include any of these:

| key | what it does |
|---|---|
| `note` | Shows a highlighted note at the top of that day |
| `file` | Shows a PDF or picture of the schedule (put the file in the `files` folder first) |
| `periods` | Replaces that day's period times (same format as periods.json) — the countdown follows it |
| `noSchool` | `true` marks the day as no school |

### `data/lunch.json` — the lunch menu
One line per date:

```
"2026-09-16": ["Chicken tenders", "Mashed potatoes", "Green beans", "Milk"],
```

You can also post the monthly menu PDF: put it in `files`, then add `"2026-10": { "file": "files/lunch-2026-10.pdf" }`.

### Uploading PDFs or pictures
Open the `files` folder on GitHub → **Add file → Upload files** → drag them in → Commit. Then reference them as `files/whatever-you-named-it.pdf`.

## Tips
- Keep the commas: every line in a list needs a comma after it except the last one. If the app says "Showing sample data," a file has a typo — GitHub highlights the line in red when you edit.
- Dates are always `YYYY-MM-DD`.
- The example dates in the files are just to show the format; delete them any time.
