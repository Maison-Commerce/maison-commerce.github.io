AZIN — DUTCH HTML PROTOTYPE
Setup and sharing guide (English)

START HERE

This folder contains the Dutch storefront prototype.
Open index.html in your browser. Keep the assets folder beside index.html.
The site is already built: you do not need a terminal, Node.js, npm, or a build step.
Extract the ZIP first; do not open the HTML from inside the ZIP viewer.
An internet connection is needed for fonts and some additional gallery photos.

CONTENTS

index.html   — the Dutch interactive storefront
assets/      — local product photos, customer photos and supporting graphics
README.txt   — this English guide
.nojekyll    — a small GitHub Pages support file (may be hidden)

PUBLISH WITH GITHUB PAGES — NO TERMINAL

1. Extract this ZIP.
2. Open your GitHub repository and choose Add file > Upload files.
3. Upload the CONTENTS of this folder: index.html, assets and the other files.
   Do not upload the ZIP itself. Do not add an extra enclosing folder.
   index.html should appear directly at the top of your repository.
4. Save with Commit changes.
5. Open Settings > Pages. Under Build and deployment:
   Source: Deploy from a branch
   Branch: main (or the branch where you uploaded the files)
   Folder: / (root)
   Click Save.
6. Wait for publication, then open the website link shown in Settings > Pages.
   Share that website link, not the github.com page showing the HTML source.

For a straightforward public demo, use a public repository with GitHub Pages
available. You need permission to configure Pages in that repository.
The package contains fewer than 100 files and can be uploaded in one batch.

EXAMPLE LINKS

https://username.github.io/repository/#/
https://username.github.io/repository/#/collections/bestsellers
https://username.github.io/repository/#/products/faux-bloesem-oudroze-3-stengels

The part after # is the page route. Direct links and page refreshes therefore
work on GitHub Pages without server configuration. Product route names are
kept the same across languages; the interface itself is Dutch.

KEEPING THE ENGLISH AND DUTCH VERSIONS

The English and Dutch downloads are separate packages. Both use index.html
as their entry file so either package works immediately with GitHub Pages.
Keep them in separate local folders; do not overwrite one with the other.

To publish both, either:
- Use a separate repository for each language; or
- Put the English package contents at the root of one repository, then put
  the entire Dutch package contents in a new nl folder in that repository.
  Upload each package in a separate batch. Keep each assets folder alongside
  its corresponding index.html. Use these links:
  English: https://username.github.io/repository/
  Dutch:   https://username.github.io/repository/nl/

WHAT IS INCLUDED

Homepage, collections, search, product pages, optional vase selection,
one/two-bouquet choices, cart drawer, image enlargement, customer-photo sliders,
styling inspiration, review cards and the checkout preview handoff.

This is a design prototype. No real orders, payments or email signups are sent.
Cart and product selections are stored in the browser. The two languages use
separate demo carts when published on the same website. The catalogue, stock,
preorder dates, promotions and shipping costs are sample prototype values,
not a live connection to Shopify. Prices and dates must be checked before launch.
The Dutch version uses Dutch wording, euro formatting and review dates.
Brand/product identifiers, coupon code WELCOME10 and route names are preserved.
Some source images may contain text embedded by the original store.

IF THE PAGE DOES NOT LOOK RIGHT

- Check that the ZIP has been extracted and index.html is beside assets/.
- Enable JavaScript and connect to the internet for fonts/extended galleries.
- For GitHub Pages, check that you uploaded the extracted files and selected
  the correct branch and root folder. Give the deployment time to complete.
- If a local browser restricts file access, use the GitHub Pages website link.
- If you are updating an existing site, refresh the page after deployment.

Official GitHub instructions:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
