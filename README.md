# schreibtischhelden.github.io

Source of <https://schreibtischhelden.github.io>.

The site is built with [markdown-pages.js](https://github.com/schreibtischhelden/markdown-pages.js) – no build step.

- **Home page:** `profile/README.md` from [schreibtischhelden/.github](https://github.com/schreibtischhelden/.github), included as the git submodule `org-profile/`. It is the same file that is shown on [github.com/schreibtischhelden](https://github.com/schreibtischhelden). To change the home page, edit it there.
- **Renderer:** markdown-pages.js is not part of this repository. `index.html` loads it from [`/markdown-pages.js/`](https://schreibtischhelden.github.io/markdown-pages.js/), the GitHub Pages site of that repository on the same origin, so it is always the version deployed from its `main` branch.

## Updates

- Dependabot checks the `org-profile` submodule daily and opens a pull request when the `.github` repository has new commits.
- The `Dependabot auto-merge` workflow merges these pull requests and triggers the `Pages` workflow, which deploys the site.

## Local preview

```sh
git clone --recurse-submodules https://github.com/schreibtischhelden/schreibtischhelden.github.io.git
cd schreibtischhelden.github.io
# local copy of the renderer, ignored by git
git clone --depth 1 https://github.com/schreibtischhelden/markdown-pages.js.git
python -m http.server 8000
```
