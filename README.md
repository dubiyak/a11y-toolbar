# Accessibility toolbar

One shared build of the accessibility toolbar, served from a permanent address
so every site loads the same file:

    https://dubiyak.github.io/a11y-toolbar/v1/accessibility-toolbar.js

## Install

```html
<script defer src="https://dubiyak.github.io/a11y-toolbar/v1/accessibility-toolbar.js"
        data-lang="he"
        data-position="bottom-left"
        data-color="#002495"
        data-storage-key="SITE-NAME-a11y"
        data-statement-url="/access"></script>
```

| attribute | meaning |
|---|---|
| `data-lang` | `he` or `en` — the toolbar's own language |
| `data-position` | `bottom-left` or `bottom-right` |
| `data-color` | the button colour, any CSS colour |
| `data-storage-key` | **unique per site** — where the reader's choices are remembered |
| `data-statement-url` | link to that site's accessibility statement; empty hides the link |

## Versions

- A fix that does not change how a site installs the toolbar is pushed into
  `v1/` and reaches every site within about ten minutes.
- ⛔ A change that would break an existing install goes into `v2/`, never into
  `v1/`. Sites move to it one at a time.
- ⚠️ Because every site loads this one file, a broken push to `v1/` breaks the
  toolbar everywhere at once. Test on one site before pushing.

⚠️ A toolbar is not conformance. Each site still needs its own accessibility
statement and audit.

Source: the build copied into the Wix Headless sites (hadisco, hapoel-haemek,
aguda-maccabi, golf-israel) and basket.co.il — all identical as of 2026-09-26.
