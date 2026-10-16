# GitHub Pages product site

This folder contains the standalone static product site, its own copies of the product images, and a small set of practical Windows guides. It has no build step, external JavaScript, analytics, or tracking pixels.

## Hosting without exposing the app repository

The app repository is private. GitHub Pages is free for public repositories, but making the app repository public would expose its source code and history. The product page is therefore published separately in the public repository `nikatsam/WhatWasIWorkingOn-Website`; only this folder's site files belong there.

The public site URL is:
`https://nikatsam.github.io/WhatWasIWorkingOn-Website/`

The `.github/workflows/deploy-pages.yml` workflow in this folder deploys the site from the root of that public repository. It republishes on pushes to `main` or when run manually.

To update the public site, copy the contents of this folder (including the hidden `.github` directory) into the root of the public website repository and push to `main`. On first setup, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions** and allow the Pages workflow if prompted.

## Microsoft Store link

The call-to-action buttons link to the app's Microsoft Store listing (`https://apps.microsoft.com/detail/9P963MWV3JR5`, Store ID 9P963MWV3JR5). The same URL is used in the structured data (`downloadUrl`, `installUrl`) and in `pad.xml`. If the listing ever changes, update those places.

## Search indexing

The site includes canonical URLs, descriptive page and social metadata, crawlable headings and text, image alt text, `robots.txt`, an XML sitemap covering the home page and guides, and SoftwareApplication, Article, CollectionPage, BreadcrumbList, and FAQPage JSON-LD. The PAD 3.11 software description is available at `pad.xml`; its Microsoft Store URL points to the direct listing (Store ID 9P963MWV3JR5). Search engines and directories decide whether to use metadata; it cannot guarantee placement or rich results.

The root-level `5236cce0528840139d690bb4f23fbbee.txt` file is the public IndexNow verification key. IndexNow submits changed page URLs, not sitemap files; the sitemap provides the URL list to notify.

This is a project site, not the account-level `nikatsam.github.io` site. Its URL includes the repository name.
