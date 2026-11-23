# QR — portfolio

One static page. No build step, no dependencies.

    index.html     the whole site
    assets/        the section photos, pulled out of the page
    netlify.toml   publish settings and cache headers

The homepage eye and the six tile photos stay embedded inside index.html on
purpose: the page paints them into a <canvas> to build the split-flap tiles,
and a browser refuses to read a canvas drawn from a separate file when the
page is opened straight off disk. Keeping them inline means index.html also
previews correctly by double-clicking it.

## Put it online

Drag this folder onto https://app.netlify.com/drop, or in Netlify pick
"Add new site" > "Deploy manually" and drop the folder. Any static host works
the same way (GitHub Pages, Vercel, Cloudflare Pages): upload the folder and
serve index.html at the root.

## Change a photo

Section photos live in assets/ and are referenced by name in index.html.
Replace a file, keep its name, redeploy. The homepage also has an
"Edit photos" control for swapping tile photos, but those swaps live only in
the browser session that made them.

## Fonts

Bebas Neue, Inter and Italianno load from Google Fonts at runtime, so the page
needs a connection to look right.
