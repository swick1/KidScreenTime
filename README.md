# Kid Screen Time

**Practice Losing.** A calmer way to handle gaming meltdowns — a Windows app from one dad,
not a company.

It locks the computer on a schedule you set, gives your kid a short calm-down break when a
real outburst happens instead of just cutting them off, and rewards the sessions that go
well. No account, no subscription, nothing sent off your machine.

Full story, screenshots, and pricing: **[the website](https://swick1.github.io/KidScreenTime/website/)**

## Download

Grab the latest installer from [Releases](https://github.com/swick1/KidScreenTime/releases) —
it's a single self-contained `.exe`, no other software required. Free 7-day trial, then a
one-time $24 for a perpetual license.

## What it does

- **Schedule** — you set the hours the computer is usable. Outside them, it locks. No
  negotiating, because the calendar said so.
- **Frustration detection** — listens for real, repeated outbursts (not game noise, not a
  loud keyboard, not normal chatter) and gives a short, calm, mandatory break instead of a
  lecture.
- **Rewards** — a session that ends without an outburst earns a little bonus time.
- **Total Screen Time mode** (optional) — cap total daily active time on top of the schedule,
  not just specific hours.
- **Guided setup wizard** — a handful of plain-language questions on first run instead of a
  wall of settings.

## Privacy & trust

Everything runs locally. There's no network code in this app at all, no telemetry, no
auto-update check. See **[what this app actually does to your PC](https://swick1.github.io/KidScreenTime/website/security.html)**
for specifics on what gets installed, what the keyboard hook can (and can't) see, and how to
verify a download yourself.

## Project layout

| Folder | What's in it |
|---|---|
| `KidScreenTime/` | The main WPF app (C#, .NET 8). |
| `Watchdog/` | A small companion process that keeps the main app running if it's closed. |
| `installer/` | The Inno Setup script used to build the distributable installer. |
| `docs/website/` | The source for the project website (GitHub Pages). |
| `build-installer.ps1` | One-command build: publishes both apps and compiles the installer. |

## Building from source

Requires Visual Studio 2022 (or the .NET 8 SDK + MSBuild) and [Inno Setup](https://jrsoftware.org/isinfo.php)
if you want to produce an installer rather than just running the app.

```
msbuild KidScreenTime.sln
```

To build a full versioned installer:

```
powershell -ExecutionPolicy Bypass -File build-installer.ps1 -Version 1.0.0
```

## License

Use it however you want, on as many of your own family's computers as you like. Just don't
redistribute copies yourself — send people here for their own copy. No warranty, use at your
own risk. Full text in [`LICENSE`](LICENSE).
