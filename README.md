# Through the Frame

A night museum you walk through by scrolling. It holds a rendered 4½-minute film with an original score, six painting rooms that a camera explores as you scroll, and a closing salon. The six paintings run from Botticelli to Munch, 1484 to 1893.

It's a static site with no build step, so GitHub Pages serves it as is.

## Publish on GitHub Pages

1. Create a new **public** repository, for example `through-the-frame`.
2. Upload everything in this folder to the root of the repository, including the hidden `.nojekyll` file. You can drag the files onto the repository page on github.com or push with git.
3. In the repository, open **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, then choose **main** and **/ (root)**. Click **Save**.
4. After about a minute the site is live at `https://<your-username>.github.io/through-the-frame/`.

To push with git from this folder instead of uploading by hand:

```bash
git init -b main
git add .
git commit -m "Publish Through the Frame"
git remote add origin https://github.com/<your-username>/through-the-frame.git
git push -u origin main
```

## What's inside

| Path | What it is |
| --- | --- |
| `index.html` | The whole page: styles, scroll engine and film player |
| `film/00-intro.mp4` … `film/07-outro.mp4` | The film's eight chapters, 1280×720 H.264, no sound |
| `score.mp3` | The continuous original score. It drives playback and keeps the chapters in sync |
| `art/` | The six paintings, plus small copies for the salon wall |
| `poster.jpg` | The poster frame and the social preview image |
| `downloads/through-the-frame.mp4` | The whole film in one file (HEVC and AAC) |

## Credits

The paintings are in the public domain: Sandro Botticelli, *The Birth of Venus*; Leonardo da Vinci, *Mona Lisa*; Johannes Vermeer, *Girl with a Pearl Earring*; Katsushika Hokusai, *The Great Wave off Kanagawa*; Vincent van Gogh, *The Starry Night*; Edvard Munch, *The Scream*. Titles, dates and collections come from Wikipedia and Wikidata. The animation and score were made for this project.
