## Extracted Public Site Assets

This folder contains the browser-delivered files downloaded from `https://vivek-ghodadra.web.app/`.

Included:
- `index.html`
- `assets/index-CiYoD383.js`
- `assets/index-CJGaUyoD.css`
- `assets/logo-CaGKeVn-.png`
- `thumbnail.png`

Important limitation:
- This is a production build of a React app, not the original repository.
- The JavaScript is bundled and minified, so component names and data can be partially inferred, but the original `src/` file structure, TypeScript source, build config, and commit history are not publicly available from page source alone.

Useful clues found in the bundle:
- Resume link: `https://drive.google.com/file/d/1HvMMA8N_FXklZ8xoa8lguF8juD3pLQwd/view?usp=sharing`
- Contact email: `ghodadravivek.work@gmail.com`
- The site uses React 18 and appears to be built with a Vite-style asset pipeline.

Best next step:
- Rebuild the UI as a fresh project using these extracted assets as a visual/content reference, instead of trying to directly maintain the minified bundle.

## Current Customization Notes

- Profile image now lives at `assets/aditya-profile.png`
- Resume button now opens `assets/aditya-resume.pdf`
- Project cards currently use `assets/project-placeholder.svg`

## How To Add Your Real Project Links Later

Open `assets/index-CiYoD383.js` and find the `const oe={...}` object.

Inside `oe.projects`, each project can include:
- `title`
- `description`
- `image`
- `technologies`
- `android`
- `ios`
- `website`
- `inDev`

Example structure:

```js
{
  title: "My Project",
  description: "Short summary here.",
  image: u6,
  technologies: ["HTML", "CSS", "JavaScript"],
  website: "https://github.com/your-project"
}
```

## How To Replace Project Screenshots

1. Add your screenshot file into `assets/`
2. Create or reuse an asset variable near the top of `index-CiYoD383.js`
3. Point the project's `image` field to that asset variable

Example:

```js
newShot = "/assets/my-project.png"
```

Then:

```js
image: newShot
```
