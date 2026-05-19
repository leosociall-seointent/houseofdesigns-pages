# House of Designs — Location Pages

Hyperlocal landing pages for House of Designs (Bangalore), served via GitHub Pages and embedded into the live Wix site via iframe.

## Pages

| Locality | File | Final URL on Wix |
|----------|------|------------------|
| Sarjapur Road | `interior-designers-in-sarjapur-road.html` | https://www.houseofdesigns.co.in/locations/interior-designers-in-sarjapur-road |
| Bellandur | `interior-designers-in-bellandur.html` | https://www.houseofdesigns.co.in/locations/interior-designers-in-bellandur |
| Marathahalli | `interior-designers-in-marathahalli.html` | https://www.houseofdesigns.co.in/locations/interior-designers-in-marathahalli |
| Whitefield | `interior-designers-in-whitefield.html` | https://www.houseofdesigns.co.in/locations/interior-designers-in-whitefield |
| ITPL Main Road | `interior-designers-in-itpl-main-road.html` | https://www.houseofdesigns.co.in/locations/interior-designers-in-itpl-main-road |

## How it works

1. These HTML files are served by GitHub Pages at `https://leosociall-seointent.github.io/houseofdesigns-pages/<file>.html`
2. The Wix dynamic page at `/locations/interior-designers-in-{slug}` contains an HTML iframe
3. A Velo snippet reads the slug from the URL and sets the iframe `src` to the matching GitHub Pages URL
4. Each HTML file has its own `<link rel="canonical">` pointing to the Wix URL, so Google credits the right domain

## Design system

Matches `1-modular-kitchen.html` from the source repo:

- **Fonts:** Cormorant Garamond (headings) + Jost (body)
- **Palette:** gold `#d4af37`, cream `#faf9f6`, dark `#2b2926`
- **Sections:** Nav → Hero slider → Intro → Wide-image → 6 service cards → Communities (dark) → Pricing → Features → Quote → Stats → Process → FAQ → Maps → CTA → Footer + Sticky CTA bar

## Schema markup

Every page includes 6 JSON-LD blocks:

1. Organization
2. LocalBusiness (locality-specific, with geo, hours, rating, hasMap)
3. Service (with AggregateOffer + price range)
4. BreadcrumbList
5. FAQPage (matching visible FAQ)
6. WebPage

Plus Open Graph, Twitter Card, and geo meta tags.
