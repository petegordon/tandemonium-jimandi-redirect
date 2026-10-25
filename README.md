# tandemonium.jimandi.love → tandemonium.housetandem.com

Tandemonium moved to **https://tandemonium.housetandem.com**. This GitHub Pages site now owns the old address, `tandemonium.jimandi.love`. It sends every visit to the same path, query and hash on the new address. `404.html` is a copy of `index.html`, so deep links work too.

Browsers keep each site's saved data (localStorage) separately. So before redirecting, the page packs the player's saved game keys into the link's `#fragment`, which is never sent to a server, and opens `/migrate/` on the new site. That page fills in any keys the browser doesn't have yet and continues to the page that was asked for. Data already saved on the new site always wins, and only the game's own keys (`tandemonium*`, `tndm*`) are carried.

`domain-migrate.js` is a copy of `js/domain-migrate.js` from the Tandemonium repo. Keep the two the same.

DNS: `tandemonium.jimandi.love` is a CNAME to `petegordon.github.io` (unchanged).
