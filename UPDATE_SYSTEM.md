# ZenCord update system

ZenCord checks this repository's `version.json` after launch. If the manifest hash differs from the installed build, the user gets **one update notification per released hash**. Closing Discord and reopening it does not show the same release notice again.

The updater downloads the runtime files listed in `version.json` into the existing ZenCord `dist` directory.

## Publishing a normal update

1. Make your source changes.
2. Bump the version with `pnpm bump X.Y.Z`.
3. Build with `pnpm build:release`.
4. Commit the changed source, `dist/`, and `version.json` to `main`.
5. Push to GitHub.

Clients read:

`https://raw.githubusercontent.com/dwd2rr2s/ZenCord/main/version.json`

If its hash differs from the installed build, ZenCord shows the update card once.

The website deployment is separate. Never commit its `.env`, Discord bot token, or `ADMIN_KEY`.
