# GitHub Pages product site

This folder contains the standalone static product site and its own copies of the product images. It has no build step, external JavaScript, analytics, or tracking pixels.

## Hosting without exposing the app repository

The app repository is private. GitHub Pages is free for public repositories, but making the app repository public would expose its source code and history. The product page is therefore published separately in the public repository `nikatsam/WhatWasIWorkingOn-Website`; only this folder's site files belong there.

The public site URL is:
`https://nikatsam.github.io/WhatWasIWorkingOn-Website/`

The `.github/workflows/deploy-pages.yml` workflow in this folder deploys the site from the root of that public repository. It republishes on pushes to `main` or when run manually.

To update the public site, copy the contents of this folder (including the hidden `.github` directory) into the root of the public website repository and push to `main`. On first setup, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions** and allow the Pages workflow if prompted.

## Microsoft Store link

The call-to-action buttons link to Microsoft Store search for the exact product name. If you have the app's direct Store URL or Store product ID, replace the `https://apps.microsoft.com/search?query=What%20Was%20I%20Working%20On` links in `index.html` and the `downloadUrl` in the structured data with the direct listing URL.

## Search indexing

The page includes a canonical URL, descriptive page and social metadata, crawlable headings and text, image alt text, `robots.txt`, an XML sitemap, and SoftwareApplication, BreadcrumbList, and FAQPage JSON-LD. Once the site is public, submit the sitemap to Google Search Console and Bing Webmaster Tools and add their verification tags or files if you want those consoles to report indexing status. Search engines decide when and how pages appear; metadata cannot guarantee placement or rich results.

This is a project site, not the account-level `nikatsam.github.io` site. Its URL includes the repository name.
