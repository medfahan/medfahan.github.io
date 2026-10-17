# fukukitaru.me

Personal site. Hand-written HTML and CSS — no framework, no build step, no
JavaScript. What's in the repo is exactly what the browser gets.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole page |
| `style.css` | All styling; every colour and size is a variable at the top |
| `404.html` | Not-found page |
| `favicon.svg` | Tab icon |
| `CNAME` | Points the custom domain at this repo — **don't delete or move it** |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is |

## Editing it

Open `index.html` in an editor, change the text, save, reload. That's the
whole workflow.

To preview with correct absolute paths (`/style.css` etc.), serve the folder
rather than opening the file directly:

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

### Before sharing the link

Three things are still placeholders, each marked `TODO` on the page:

1. **Projects** — replace both cards with real work, or delete the whole
   `<section>`. There's a copy-paste template in an HTML comment just above
   them. Coursework counts.
2. **Education** — fill in school, programme and relevant modules.
3. **Email** — the footer says `you@example.com`. Swap in whichever address
   you actually want public.

Once a block says something true, delete its `class="todo"` and its
`<span class="badge">TODO</span>` so it stops looking unfinished.

### Changing a skill level

Each skill meter is three segments. Add or remove `class="on"` to change it:

```html
<span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i></i></span>
```

One of three = learning, two = working knowledge, three = comfortable. The word
to the right of the meter is what screen readers and search engines actually
read, so keep it matched to the segments.

## Deploying

GitHub Pages serves this from the `main` branch, so `fukukitaru.me` updates a
minute or so after anything is merged there. Pushing to any other branch
changes nothing on the live site.
