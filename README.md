# Egyptian Streets — Tailwind rebuild

`index.html` is untouched. All styling lives in `css/input.css`,
compiled to `css/output.css`.

## Changelog
- Fixed collision with Tailwind v4's built-in `.container` utility.
- Fixed underline z-index (-10 -> -1) on highlighted spans.
- Added background-color fallback on `.access-banner`.
- Fixed `.recommended-content` / `.arts-tech-content` overlap -> now
  a plain stack with a 5.6rem gap below the image.
- Fixed the blank gap under "Top Viewed": `.top-viewed-grid` now
  uses items-stretch, and the main image grows with flex-1 to fill
  extra height instead of leaving whitespace.
- Added explicit bg-white on `.search-input` so it's always white
  regardless of browser default input styling.

All of the above were rendered and visually verified with a headless
browser before shipping.

Drop your `img/` folder next to `index.html`, then:

```
npm install
npm run build
npm run watch
```

Only edit `css/input.css` — `css/output.css` is generated.
