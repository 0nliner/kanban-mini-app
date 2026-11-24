# Kanban for Nextbrowser

A standalone example for [Nextbrowser Mini Apps v1](docs/mini-apps-v1.md). Create and edit tasks, move them between To do, In progress and Done, and keep the board across desktop restarts. The app requests permission to store its own board on this device.

## Install

Download [kanban.nbmini.json](https://github.com/0nliner/kanban-mini-app/releases/download/v1.0.0/kanban.nbmini.json). In a Nextbrowser desktop build with Mini Apps, open **Extensions → Mini Apps → Install from file**, select the downloaded file, and confirm. You can also select **Install** on the Kanban card in the desktop catalog.

## Build your own mini app

Clone or fork this repository and change the ID and name in `manifest.json` for your app. Edit `index.html`, `board.css` and `board.js`, then run the following command with Node.js 22. The build uses only Node's standard library.

```sh
npm run build
```

Import the resulting `<id>.nbmini.json` in Nextbrowser. The [v1 standard](docs/mini-apps-v1.md) describes the manifest, permissions, storage API, quotas and error handling. The [desktop integration](https://github.com/nextbrowser-oss/nextbrowser-app/pull/353) includes the host and a smoke test that installs the package and exercises the board in Electron.

Licensed under [AGPL-3.0-only](LICENSE), as in the upstream Nextbrowser project.
