# matthias-matthies.com

Jekyll-powered resume site, published via GitHub Pages.

## Running locally with Docker

Build the image:

```
docker build -t matthias-cv .
```

Run it with the source mounted as a volume, so edits on your machine trigger a hot reload in the browser:

```
docker run --rm -p 4000:4000 -p 35729:35729 -v "$PWD":/site matthias-cv
```

Then open `http://localhost:4000`. Edit any file and the page will rebuild and refresh automatically.

If you just want to view the site without hot reload, drop the volume mount:

```
docker run --rm -p 4000:4000 matthias-cv
```
