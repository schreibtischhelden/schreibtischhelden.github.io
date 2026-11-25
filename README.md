# schreibtischhelden.github.io

Source of <https://schreibtischhelden.github.io>.

The site is built with [markdown-pages.js](https://github.com/schreibtischhelden/markdown-pages.js) – no build step. Its content comes from two git submodules:

| Submodule | Repository | Used for |
|---|---|---|
| `org-profile/` | [schreibtischhelden/.github](https://github.com/schreibtischhelden/.github) | Home page: `profile/README.md`, the same file that is shown on [github.com/schreibtischhelden](https://github.com/schreibtischhelden) |
| `markdown-pages.js/` | [schreibtischhelden/markdown-pages.js](https://github.com/schreibtischhelden/markdown-pages.js) | Renderer, styles and vendored libraries |

To change the home page, edit `profile/README.md` in the `.github` repository.

## Updates

- Dependabot checks both submodules daily and opens a pull request when they have new commits.
- The `Dependabot auto-merge` workflow merges these pull requests and triggers the `Pages` workflow, which deploys the site.

## Local preview

```sh
git clone --recurse-submodules https://github.com/schreibtischhelden/schreibtischhelden.github.io.git
cd schreibtischhelden.github.io
python -m http.server 8000
```
