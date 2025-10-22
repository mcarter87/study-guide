# H5P on GitHub Pages — Accordion Starter

This repo is a minimal starter to host an **H5P Accordion** (or any H5P content) on **GitHub Pages** using the **H5P Standalone** player.

## Quick start

1. **Export your H5P from WordPress**
   - In your H5P content, click **Reuse → Download** to get a `.h5p` file.

2. **Unzip the `.h5p`**
   - Rename it to `.zip` if needed and extract. You should get:
     ```
     h5p.json
     content/
     libraries/
     ```

3. **Add it to this repo**
   - Copy those extracted items into: `h5p/accordion/` (replace the placeholder `README.txt`).

4. **Commit & push**, then enable **GitHub Pages** in **Settings → Pages** for this repository.

5. **Open your site** and test. The main page (`index.html`) will load the H5P from `./h5p/accordion`.

## Notes

- This starter pins the H5P Standalone CDN to version `3.8.0` for stability.
- Make sure the `.nojekyll` file stays in the repo root so GitHub Pages serves the library folders as-is.
- For multiple H5P items, duplicate the folder (e.g., `h5p/accordion-2/`) and add another container + initializer in `index.html`.
- GitHub Pages is static: viewing works perfectly, but things like xAPI/LRS data storage require a separate service.

## Repo structure

```
(repo root)
├─ .nojekyll
├─ index.html
├─ README.md
└─ h5p/
   └─ accordion/
      └─ README.txt   # replace this entire folder with your unzipped H5P
```
