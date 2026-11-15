# LibreWolf custom CSS

A dark theme with bright blue (`#00ACFF`) accents and square corners.

- `userChrome.css` hides the horizontal tab bar and sidebar panel header, removes the sidebar's starting padding, and squares browser UI corners.
- `userContent.css` styles internal `about:` pages with dark backgrounds, blue accents, and square corners.

The horizontal tab bar is hidden, so use vertical/sidebar tabs or remove the `#TabsToolbar` rule from `userChrome.css` to show it again.

## Setup

1. In LibreWolf, open `about:support` and find **Profile Directory** (or **Profile Folder**). Click **Open Directory** / **Open Folder** to open your active profile.
2. Create a folder named `chrome` inside that profile if it does not exist.
3. Back up any existing `userChrome.css` and `userContent.css`, then copy these two files into `chrome`. Keep their exact filenames; they should not end in `.txt`.
4. Open `about:config`, search for `toolkit.legacyUserProfileCustomizations.stylesheets`, and set it to `true`.
5. Fully quit and reopen LibreWolf to load the styles.

The files should be arranged like this:

```text
<your active profile>/
└── chrome/
    ├── userChrome.css
    └── userContent.css
```

## Customize or remove

To change the accent, replace `#00ACFF` in `userContent.css`. Keep the trailing `55` on transparent variants such as `#00ACFF55`. Restart LibreWolf after editing.

To remove this theme, delete these CSS files or restore your backups, then restart. To disable all profile CSS, set `toolkit.legacyUserProfileCustomizations.stylesheets` to `false` instead.

Reference: [Mozilla's guide to custom CSS](https://support.mozilla.org/en-US/kb/contributors-guide-firefox-advanced-customization).
