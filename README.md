# FUEL UP OUTDOORS

Trail-ready jerky & meat sticks by **Johanthan Blake Olson**.

**Tagline:** Fuel the Wild.

**Live site:** https://aadlakha1.github.io/mankit/
**Admin dashboard:** append `?admin` to the site URL

---

## Tech Stack

- Single self-contained `index.html` (no build tools, no dependencies)
- Dark, earthy, premium outdoor design with campfire amber accent
- Firebase Firestore for real-time order + waitlist storage
- Firebase Auth (email/password) for admin access
- Hosted on GitHub Pages

---

## Project Structure

```
/
├── index.html          # Entire app (HTML + CSS + JS)
├── firestore.rules     # Firestore security rules (deploy manually)
└── README.md
```

---

## Products & Pricing

### Jerky Bags (2.5 oz each)
| Flavor | Price | ID |
|---|---|---|
| Basecamp Original | $14 | `jerky-original` |
| Smokestack Pepper | $14 | `jerky-peppered` |
| Summit Teriyaki | $15 | `jerky-teriyaki` |
| Trailfire Habanero | $16 | `jerky-habanero` |

### Meat Sticks (Pack of 8)
| Flavor | Price | ID |
|---|---|---|
| Ridgeline Original | $18 | `stick-original` |
| Pinecrest Turkey | $18 | `stick-turkey` |
| Timberline Buffalo | $20 | `stick-buffalo` |
| Elk Run Venison | $22 | `stick-venison` |
| Fireside Jalapeno | $20 | `stick-jalapeno` |

---

## Firebase Setup (Required)

The `firebaseConfig` block in `index.html` has placeholder values. Replace with your project's config.

1. Create Firebase project at [console.firebase.google.com](https://console.firebase.google.com)
2. Enable Firestore (production mode)
3. Deploy security rules from `firestore.rules`
4. Enable Email/Password authentication
5. Add admin user
6. Paste your `firebaseConfig` into `index.html`

---

## Admin Dashboard

Access: append `?admin` to the site URL.

- Real-time orders via Firestore `onSnapshot`
- Stats: total orders, revenue, items, avg order value
- Search & filter by status
- Status cycling: pending → confirmed → shipped → cancelled
- Delete orders, export CSV

---

## Customer Order Flow

1. Click **Order Now**
2. Select products and quantities
3. Fill in shipping details
4. Place order → saved to Firestore
5. Confirmation with order ID (e.g. `MK-M4X8K2AB`)
6. Social share buttons

---

## Design

- **Palette:** Campfire amber `#c17f3e`, forest green `#5a7a52`, on deep woodland `#1a1710`
- **Always dark** — no light mode
- **Jerky bags:** Earthy gradient pouches with sealed tops
- **Meat sticks:** Slim rounded cylinders in natural tones
- **Animations:** Scroll reveal, number counters, mouse-follow parallax
- **Responsive:** Fully mobile-friendly
