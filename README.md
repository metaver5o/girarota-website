# GiraRota website

Static site for https://girarota.com: route optimization for delivery drivers,
running in the browser (2-opt TSP, Leaflet maps, Waze / Google Maps links).

## No secrets in this repo

Everything here is served to every visitor, so nothing secret may live in it:
no API tokens, client secrets, passwords or private keys, and no build step
that injects them. Checkout opens a Mercado Pago payment link (a public URL).
Anything that needs a credential, like creating Pix charges or confirming
payments, belongs in a server-side component holding the token as its own
secret, never in this repo or in GitHub Pages.

Before every push: `gitleaks git .` must report no leaks.
