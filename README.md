# My Collection

A guided tour of a large image, published on GitHub Pages. Made with
[PosterForker](https://github.com/micahchoo/posterforker): no install, no server.

## Publish it (once)

The first **Publish** run, made when you copied the template, fails: GitHub Pages is
off in a new repository. That is expected.

1. **Settings → Pages → Build and deployment → Source: GitHub Actions.**
2. **Actions → Publish → Run workflow**, and wait for it to turn green, about a minute.
3. Your Collection is at `https://<your-name>.github.io/<this-repository>/`, and its
   editor is at the same address plus `edit/`:
   `https://<your-name>.github.io/<this-repository>/edit/`. Every Publish run lists
   both on its summary page.

   Add `edit/` to the address itself, not after a `#`: anything after `#` stays in
   the viewer.

See this template's own Collection: https://micahchoo.github.io/posterforker-template/

## Make it yours

| To | Do |
|---|---|
| Add an Image up to 25 MB | **Add file → Upload files** into a new folder `tours/<name>/`, then copy `tours/great-wave/tour.yml` beside it |
| Add a bigger Image (up to 2 GB) | **Releases → Draft a new release**, attach the file, publish; in `tour.yml` write `image: { release: <file name> }` |
| Add or change a Scene | Open your Collection's `edit/` address, press **Add a Scene** or pick one, drag its box, write |
| Change the look or the layout | `edit/` → **Look** or **Layout** |
| Remove the example | Delete the folder `tours/great-wave/` and its name in `collection.yml` |

When you are done, press **Save**. It lists each change with a button
that opens the right page on GitHub; commit each one there. Every commit publishes again,
in about a minute. Your unsaved edits wait in the browser until then, even across a reload. If something is wrong, the **Publish** run fails and
GitHub marks the line on the file, for example
`tours/river/scenes/04.md line 3: region.w is required`.

## Scene files

```markdown
---
title: The river mouth
region: { x: 1200, y: 3400, w: 2400, h: 1600 }   # pixels of the full Image
---
What a Reader should notice here. Markdown works.
```

Scenes play in file-name order: `01.md`, `02.md`, …
