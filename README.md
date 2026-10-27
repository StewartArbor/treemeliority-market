# Treemeliority Market

Static Jekyll affiliate marketplace for https://market.treemeliority.org/

## Adding a product

Products live in `_data/products.yml`. Add one YAML record per product:

```yaml
- id: prism-reading-glasses
  active: true
  shelf: curiosities
  category: optics
  title: "90° Prism Reading Glasses"
  note: "Read while lying flat without converting your cervical spine into punctuation."
  image: "/assets/products/prism-reading-glasses.webp"
  price: "About $7"
  merchant: "AliExpress"
  affiliate_url: "https://your-affiliate-link.example"
  badge: "Optical oddity"
```

Rules:

- `shelf` must be `essentials` or `curiosities`.
- Only `active: true` items render.
- `affiliate_url` should be the checked merchant/deeplink destination.
- `image`, `price`, `merchant`, and `badge` are optional.
- Set `active: false` to retire an item without deleting its record.
- Do not invent prices, ratings, stock, discounts, or reviews.

Historical Rialto files remain in repository history; the live site is Treemeliority Market.
