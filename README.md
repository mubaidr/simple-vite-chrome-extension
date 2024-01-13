# simple-vite-chrome-extension

[![build](https://github.com/mubaidr/simple-vite-chrome-extension/actions/workflows/build.yml/badge.svg)](https://github.com/mubaidr/simple-vite-chrome-extension/actions/workflows/build.yml) [![release](https://github.com/mubaidr/simple-vite-chrome-extension/actions/workflows/release.yml/badge.svg)](https://github.com/mubaidr/simple-vite-chrome-extension/actions/workflows/release.yml)

A [Vite](https://vitejs.dev/) powered WebExtension ([Chrome](https://developer.chrome.com/docs/extensions/reference/), [FireFox](https://addons.mozilla.org/en-US/developers/), etc.) starter template based on `manifest 3`.

**Please check: [vite-vue3-chrome-extension-v3](https://github.com/mubaidr/vite-vue3-chrome-extension-v3) for a more advance template based on Vuejs**

## Features

- HMR for extension pages and content scripts
- Sample `onInstall` & `onUpdate` pages
- vscode recommended settings and extensions for chrome plugin development
- [TypeScript](https://www.typescriptlang.org/) - type safe
- `Eslint` & `Prettier` configured for `javascript`, `TypeScript`
- [CRXJS Vite Plugin](https://crxjs.dev/vite-plugin) Build a Chrome Extension with Vite
- Github build and release actions

_Please create an issue if you feel some feature is missing or could be improved._

## Pre-packed

## Use the Template

### GitHub Template

[Create a repo from this template on GitHub](https://github.com/mubaidr/simple-vite-chrome-extension/generate).

### Clone to local

If you prefer to do it manually with the cleaner git history

> If you don't have pnpm installed, run: npm install -g pnpm

```bash
pnpx degit mubaidr/simple-vite-chrome-extension my-webext
cd my-webext
pnpm i
```

## Usage

### Project Structure

- `src` - main source.
  - `content-script` - scripts and components to be injected as `content_script`
    - `iframe` content script iframe app which will be injected into page
  - `background` - scripts for background.
  - `popup` - popup application root
    - `pages` - popup pages
  - `options` - options application root
    - `pages` - options pages
  - `setup` - Page for Install and Update chrome extension events
    - `pages` - pages for install and update events
  - `offscreen` - Chrome extension offscreen pages, can be used for audio, screen recording
  - `pages` - application pages, common to all views (About, Contact, Authentication etc)
  - `assets` - assets
- `dist` - built files, also serve stub entry for Vite on development.

### Extra info

In [src/background/index.ts](./src/background/index.ts) you can find an example of chrome.runtime.onInstalled.addListener.

### Development

```bash
pnpm dev
```

Then **load extension in browser with the `dist/` folder**.

### Build

To build the extension, run

```bash
pnpm build
```

And then pack files under `dist`, you can upload `dist.crx` or `dist.xpi` to appropriate extension store.

## Contributors

<!-- readme: collaborators,contributors -start -->
<table>
<tr>
    <td align="center">
        <a href="https://github.com/mubaidr">
            <img src="https://avatars.githubusercontent.com/u/2222702?v=4" width="100;" alt="mubaidr"/>
            <br />
            <sub><b>Muhammad Ubaid Raza</b></sub>
        </a>
    </td></tr>
</table>
<!-- readme: collaborators,contributors -end -->
