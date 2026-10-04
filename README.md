# My Collection

A guided tour of a large image, published on GitHub Pages. Made with
[PosterForker](https://github.com/micahchoo/posterforker): no install, no server.

## Publish it (once)

The first **Publish** run, made when you copied the template, fails: GitHub Pages is
off in a new repository. That is expected.

1. **Settings → Pages → Build and deployment → Source: GitHub Actions.**
2. **Actions → Publish → Run workflow**, and wait for it to turn green, about a minute.
3. Your Collection is at `https://<your-name>.github.io/<this-repository>/`.

See this template's own Collection: https://micahchoo.github.io/posterforker-template/

## Make it yours

| To | Do |
|---|---|
| Add an Image up to 25 MB | **Add file → Upload files** into a new folder `tours/<name>/`, then copy `tours/great-wave/tour.yml` beside it |
| Add a bigger Image (up to 2 GB) | **Releases → Draft a new release**, attach the file, publish; in `tour.yml` write `image: { release: <file name> }` |
| Add a Scene | Open `/edit/` on your Collection, draw a box, write, press **Commit this Scene on GitHub** |
| Change the look or the layout | `/edit/` → **Theme** or **Layout**, then paste into the file it opens |
| Remove the example | Delete the folder `tours/great-wave/` and its name in `collection.yml` |

Each commit publishes again. If something is wrong, the **Publish** run fails and
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
