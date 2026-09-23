# Orchestra Platform Preview, shareable build

A plain static site. No account, no build step, no server code: three files and an image.

    index.html    the presentation, nineteen screens in two themes and three navigation styles
    canvas.html   the same screens on one pan-and-zoom board, heavier to load
    og.png        the image shown when the link is pasted into Slack, Teams or email
    vercel.json   asks hosts not to index the pages

## Put it online with Vercel

From inside this folder:

    npx vercel deploy --prod

The first run asks you to sign in and to confirm the project name, then prints the link.
Anyone with that link can open it, no Claude account needed.

Vercel's dashboard also takes the folder by drag and drop, which needs no command line.

## Or any other static host

Netlify, Cloudflare Pages, GitHub Pages, an S3 bucket, or a folder on your own web server.
Upload the files as they are; `index.html` is the entry point.

## Keeping it in step with the design

The site is generated. After changing a screen, rebuild in this order from the folder above:

    python3 build_deck.py
    python3 build_site.py

## Note on the sample data

Every figure, name, invoice and document in these screens is illustrative sample data,
shaped to look like a real year at the fund. Nothing is a real record.
# OFIS-next-design
