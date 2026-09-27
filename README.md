<div align="center">

# ZenCord

**ZenCord — Calm meets connection.**

An open-source Discord desktop client modification with plugins, themes, ZenProfile, a native Windows installer, and a GitHub-backed update channel.

[Website](https://zencord.co.uk) · [Support Server](https://discord.gg/fYxFZdzz5d)

</div>

---

## What is included

- ZenCord desktop injection/runtime source
- Native Windows installer source (`InstallerGUI.cs` and `Installer.cs`)
- ZenProfile local profile overrides
- ZenCord Settings → Support
- Plugins, themes, QuickCSS, backup/restore, and desktop injection
- GitHub-backed runtime update manifest
- One update notification per released update hash

## Windows installation

1. Download the latest ZenCord Windows package from the website.
2. Extract it fully.
3. Fully close Discord from the system tray and Task Manager.
4. Run `Install-ZenCord.bat`.
5. Choose your Discord installation and select **Install** or **Repair**.
6. Close the installer when it finishes.
7. Open Discord → **User Settings** → **ZenCord Settings**.

## Building from source

Requirements: Node.js 22+, Corepack/pnpm 11.9.0, Git.

```bash
corepack enable
corepack prepare pnpm@11.9.0 --activate
pnpm install --frozen-lockfile
pnpm build:release
```

## Updates

Installed clients check this repository's `version.json`. When its hash changes, ZenCord displays an update notice once for that released hash. Users can install from that notice or manually use **ZenCord Settings → Updater**.

See [UPDATE_SYSTEM.md](UPDATE_SYSTEM.md).

## Source bootstrap

The full source bundle is also published by the ZenCord website at:

`https://zencord.co.uk/downloads/ZenCord-Source-1.15.1.zip`

The workflow in `.github/workflows/import-source.yml` can import that source bundle into this repository after the updated website bundle is deployed.

## Security

The public repository must never contain the website bot `.env`, Discord bot token, or website `ADMIN_KEY`.

## Support

https://discord.gg/fYxFZdzz5d

## License

GPL-3.0-or-later.
