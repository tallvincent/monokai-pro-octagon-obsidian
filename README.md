<div align="center">

# Monokai Pro Octagon for Obsidian

An Obsidian dark theme based on the Monokai Pro Octagon palette used by Ghostty.

</div>

The theme brings Octagon's deep blue-gray background and vivid syntax colors to Obsidian. Its modular Sass source and embedded [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) options make selected accents and interface details configurable.

## Palette

The palette is based on the [Monokai Pro Octagon Ghostty theme](https://github.com/Kirlovon/monokai-ghostty/blob/main/Monokai%20Pro%20Octagon), which identifies its colors as based on the Monokai Pro color scheme. The Obsidian theme maps the terminal colors to app surfaces, text, accents, links, and syntax highlighting; a few intermediate surface shades are derived from the base background.

| Role | Color |
| --- | --- |
| Background | `#282a3a` |
| Foreground | `#eaf2f1` |
| Red | `#ff657a` |
| Green | `#bad761` |
| Yellow | `#ffd76d` |
| Orange | `#ff9b5e` |
| Purple | `#c39ac9` |
| Teal | `#9cd1bb` |
| Selection | `#535763` |
| Cursor | `#b2b9bd` |

## Install and configure

Install the theme from **Settings → Appearance → Themes**, or copy `theme.css` and `manifest.json` into `.obsidian/themes/Monokai Pro Octagon/` in your vault. Select **Monokai Pro Octagon** as the active theme.

For customization, install and enable the Style Settings community plugin. Open **Settings → Style Settings → Monokai Pro Octagon** to choose an accent color, toggle colored headings, or enable rounded corners.

## Development

The Sass source is split by responsibility under `scss/`; `scss/main.scss` compiles to the root-level `theme.css` used by Obsidian and releases.

The repository includes a Nix flake that provides Node.js and npm. With Nix installed and flakes enabled:

```sh
nix develop .
npm ci
npm run build
npm run lint
```

Use `npm run watch` to rebuild `theme.css` while editing. Reload the theme in Obsidian to preview changes. Linting also runs in GitHub Actions.

## Screenshots

### Dashboard

![Monokai Pro Octagon displaying a dashboard with the file explorer and calendar](screenshots/main.png)

### Task statuses

![Monokai Pro Octagon task checkbox and status marker styles](screenshots/task-statuses.png)

## Releasing

Update `manifest.json` and `versions.json` for a release, then push a tag matching the manifest version. The existing GitHub Actions workflow creates a draft release with `manifest.json` and `theme.css` attached. See the [Obsidian theme release guide](https://docs.obsidian.md/Themes/App+themes/Release+your+theme+with+GitHub+Actions).

## License and attribution

The palette reference and attribution are documented above. The repository's existing `LICENSE` applies to the theme source; check the upstream Monokai Pro and Ghostty palette terms before redistributing the palette independently.
