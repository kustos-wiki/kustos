<p align="center">
  <img src="assets/kustos-wordmark.svg" width="340" alt="Kustos">
</p>

<p align="center"><b>Plex serves it. Kustos looks after it.</b></p>
<p align="center">
  <a href="https://kustos.wiki">Website</a> ·
  <a href="https://github.com/kustos-wiki/kustos/releases/latest">Download</a> ·
  <a href="https://kustos.wiki/help">Wiki</a> ·
  <a href="https://discord.gg/awsNGHKTXD">Discord</a>
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=1m2BPqSbeyE">
    <img src="https://i.ytimg.com/vi/1m2BPqSbeyE/hqdefault.jpg" width="480" alt="Watch: the easiest Plex poster maker, no YAML required — 45 seconds">
  </a>
</p>
<p align="center"><sub><a href="https://www.youtube.com/watch?v=1m2BPqSbeyE">45 seconds of it working</a></sub></p>

Kustos manages the parts of a Plex library that Plex and the *arrs leave to you — for everyone in the house:

- **Collections** built and kept up to date by rules
- **Artwork** — posters, title cards and overlays from your own templates, with
  wordmarks drawn for titles that have none
- **Cleanup rules** across Sonarr and Radarr, with watch history as a condition,
  a countdown before anything goes, and a record of what went
- **Watch history** — one record of who watched what, merged across Plex,
  Tautulli, Trakt and Simkl, and written back to any of them
- **Requests** for people who don't want to set up Seerr

It runs on your own Windows machine as a service, next to your Plex server, and is never published to the internet.

## Download

**[Kustos-Setup.exe](https://github.com/kustos-wiki/kustos/releases/latest/download/Kustos-Setup.exe)** — latest release. Each release lists the file's SHA-256 so you can check it before running:

```powershell
Get-FileHash .\Kustos-Setup.exe -Algorithm SHA256
```

The installer isn't code-signed yet, so Windows will warn about an unknown
publisher.

It installs as a Windows service beside your Plex server, and can install and
configure Sonarr, Radarr, Prowlarr, qBittorrent, Tautulli and Overseerr for you
if you don't already have them.

## Docker

For servers already running in containers:

```
docker pull ghcr.io/kustos-wiki/kustos:latest
```

One volume (`/config`) holds the database and everything Kustos has learned.
The [install guide](https://kustos.wiki/help) has the compose file.

**If your media is on a NAS, install Sonarr and Radarr yourself** and point
Kustos at them. It cannot guess which share your library lives on, so a
container it launches for you would come up with an empty root folder rather
than an error.

## Price

30 days free, no card. Then $5.99 a month or $60 a year, plus tax.

## Coming from another tool?

Each page answers one question, and says where Kustos does **not** help:

- [Kometa, and YAML that builds nothing without erroring](https://kustos.wiki/wiki/coming-from-kometa)
- [A cleanup that deleted a series someone was half-way through](https://kustos.wiki/wiki/deleting-a-show-someone-was-half-way-through)
- [Title cards without making ten thousand by hand](https://kustos.wiki/wiki/making-plex-title-cards-automatically)
- [Feeding a 4K Sonarr or Radarr alongside your main one](https://kustos.wiki/wiki/running-a-4k-sonarr-or-radarr-alongside-your-main-one)
- [Trakt sync for everyone in the house, not just you](https://kustos.wiki/wiki/trakt-sync-for-everyone-in-the-house)

Kustos did not invent any of this. Kometa, Maintainerr, TitleCardMaker and the
rest worked out what a Plex library actually needs. Kustos puts those ideas in
one place, with a UI instead of a config file, and makes them aware of each
other.

## Help

- **Discord** — [discord.gg/awsNGHKTXD](https://discord.gg/awsNGHKTXD), the fastest way to get help
- **Wiki** — [kustos.wiki](https://kustos.wiki)

---

This repository holds releases only. Kustos is not open source.
