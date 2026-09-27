# waahlstrand.github.io

A minimal Jekyll homepage. There is no theme and there are no plugins.

| What | Where |
|---|---|
| Name, role, links, publication categories | `_config.yml` |
| Bio paragraphs | `index.html` (the `.about` section) |
| Publication cards | `_data/publications.yml` |
| Styles (light and dark) | `assets/css/style.css` |
| Portrait | `assets/img/portrait.jpg` |

**Adding a paper:** add an entry at the top of `_data/publications.yml`. Set `category` to `imaging` or `humanities`, and give it a few generic `tags`. Reuse existing tags where you can, since clicking a tag shows every paper that has it. The first link becomes the link on the card title.

**Adding an image to a card:** put the figure in `assets/img/papers/`. Then add `image: /assets/img/papers/<file>` to the paper's entry, and optionally `image_alt:` with a short description. The image fills the card's left edge on desktop and its top edge on phones. It is cropped to fit, so pick a figure whose important part is near the centre; roughly square or portrait figures work best. Keep files under about 200 KB; around 600 px wide is plenty.

**Building locally:**

```sh
bundle install
bundle exec jekyll serve
```

**Deploying:** a push to `master` runs `.github/workflows/deploy.yml`. It builds the site and publishes it to the `gh-pages` branch.
