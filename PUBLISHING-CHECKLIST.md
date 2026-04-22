# 🚢 New Dispatch Publishing Checklist

Every time a new dispatch page is created, run through this entire list.

## 1. HTML Page
- [ ] Create `dispatch-name.html` in `~/rosesdispatch/`
- [ ] Add `<link rel="canonical" href="https://rosesdispatch.com/dispatch-name.html">` in `<head>`
- [ ] Add `<meta name="description" content="...">` in `<head>` (70-150 chars, hook + destination)
- [ ] Add Dispatch # tag (e.g., `Dispatch #008`) visible on the page

## 2. Sitemap Update
- [ ] Add new URL to `sitemap.xml` with:
  - `<loc>https://rosesdispatch.com/dispatch-name.html</loc>`
  - `<lastmod>YYYY-MM-DD</lastmod>` (today's date)
  - `<changefreq>monthly</changefreq>`
  - `<priority>0.8</priority>` (or `0.9` for featured/latest)

## 3. Homepage Update
- [ ] Add the dispatch link to the "Latest Dispatches" section on `index.html`
- [ ] If a dispatch moves out of "Coming Soon", remove it from that section

## 4. Git Commit & Push
```bash
cd ~/rosesdispatch
git add -A
git commit -m "publish: Dispatch #NNN — Destination Name"
git push
```

## 5. Post-Publish (within 48h)
- [ ] Verify page loads at `https://rosesdispatch.com/dispatch-name.html`
- [ ] Verify `https://rosesdispatch.com/sitemap.xml` includes the new URL
- [ ] Request indexing in Google Search Console (URL Inspection → Request Indexing)
- [ ] Announce in Discord / social if applicable
