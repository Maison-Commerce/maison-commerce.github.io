# CRO Wireframe Template

This folder contains Maison Commerce's reusable, single-file CRO roadmap and
mobile wireframe template. Use it to turn a client research brief into a clear,
clickable overview of no more than four A/B tests.

## What is included

- `index.html` contains all markup, styling, example content, navigation and
  interactions. It has no build step.
- `AGENTS.md` is this operating guide.
- `cro-wireframes-template.zip` is the public download package. Rebuild it after
  changing either file or any packaged asset.

The downloadable ZIP also contains the required `fonts/` files and the Maison
Commerce logo under `images/`. Keep that relative folder structure intact:
`index.html` expects those assets one level above its own folder.

## How the template works

The document behaves like a small website while remaining one HTML file. Its
six views are selected by the URL hash:

1. `#overview` — title, introduction and the master test table.
2. `#b1` through `#b4` — four individual test briefs with before/after mobile
   wireframes.
3. `#plan` — recommended sequencing and measurement guidance.

The router near the bottom of `index.html` uses the `ORDER` array. Elements with
`data-go="..."` open the matching `<section id="page-...">`. The arrow buttons,
keyboard arrows and browser history use the same order.

Interactive wireframe elements use these attributes:

- `data-opens` and `data-close` control modal sheets.
- `data-add` provides the temporary added-to-cart response.
- `.acc .q` controls FAQ accordions.
- `.hotspot` and `data-card` control shoppable-banner cards.

## Create a client version

1. Duplicate the template folder or create a working branch.
2. Replace `{client-name}` in the overview title.
3. Replace the four example tests with evidence-backed client tests. Keep the
   template to a maximum of four tests and retain the labels `T1`–`T4`.
4. Update each test everywhere it appears: top navigation, overview table,
   individual page, previous/next buttons and planning section.
5. On each test page, update the title, summary, KPIs, targeting, segment, tool,
   evidence and A/B test ID. The A/B test ID must remain the final row of the
   metadata list, after Tool and Evidence.
6. Replace the problem, solution and hypothesis with client-specific content.
7. Adapt both phone wireframes to show the actual control and proposed variant.
8. Keep the writing globally applicable: do not add a previous client's name,
   products, internal tools or untranslated copy unless that client is the
   intended recipient.
9. Update the Planning view so dependencies, sequence and measurement match the
   four selected tests.

## Editing rules

- Follow the design tokens in `:root` and the presentation layer already in the
  file. Headings stay italic at weight 400.
- Preserve the Maison Commerce logo, near-black/green palette and existing font
  stack unless the brief explicitly calls for a rebrand.
- Keep buttons slightly rounded (`4px`) where the existing component uses that
  shape; do not turn navigation buttons into pills.
- Keep all examples store-agnostic until real client data has been supplied.
- Use semantic labels and preserve keyboard access for interactive elements.
- Do not add a framework or build tooling. This template is deliberately
  portable and should still open directly as a local HTML file.
- The public download banner is hidden by default. JavaScript reveals it only
  when the hostname is `www.maisoncommerce.co` and the path starts with
  `/cro-wireframes-template`.

## Validate before delivery

- Confirm Overview, T1–T4 and Planning all open from the top navigation.
- Confirm previous/next buttons, keyboard arrows and browser back/forward work.
- Test every modal, accordion, add button and hotspot in both wireframe columns.
- Check desktop, tablet and mobile widths for clipping and horizontal overflow.
- Verify the overview table contains exactly four tests and no status column.
- Search for `{client-name}`, previous-client references, stale test names,
  stale test IDs and draft copy before delivering a client version.
- Open the page from the intended hosted URL and verify assets load there; a
  local-file check alone does not prove the deployed route works.

## Rebuild the public ZIP

From the repository root, create `cro-wireframes-template/cro-wireframes-template.zip`
with these paths and no macOS metadata:

```sh
zip -X -r cro-wireframes-template/cro-wireframes-template.zip \
  cro-wireframes-template/index.html \
  cro-wireframes-template/AGENTS.md \
  fonts/GTSectra-Book.woff2 \
  fonts/GTSectra-Medium.woff2 \
  fonts/GTSectra-Bold.woff2 \
  fonts/GTSectra-BookItalic.woff2 \
  images/logo-maison-commerce.png
```

List the archive contents after rebuilding it and confirm both `index.html` and
`AGENTS.md` are present before publishing.
