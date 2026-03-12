# MANKIT

Intense workout protein & electrolyte drinks by **Ryan Hutzley**.

**Tagline:** Built Different.

**Live site:** https://aadlakha1.github.io/mankit/
**Admin dashboard:** append `?admin` to the site URL

---

## Tech Stack

- Single self-contained `index.html` (no build tools, no dependencies)
- Dark, matte, premium design with burnt copper accent
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

### Powder Sticks (Box of 12)
| Flavor | Price | ID |
|---|---|---|
| Iron Forge (Blood Orange) | $24 | `stick-blood-orange` |
| Black Ops (Unflavored) | $22 | `stick-unflavored` |
| Granite (Vanilla Smoke) | $24 | `stick-vanilla` |
| War Paint (Tropical) | $26 | `stick-tropical` |

### RTD Cans (Pack of 6)
| Flavor | Price | ID |
|---|---|---|
| Ironside (Blood Orange) | $30 | `can-blood-orange` |
| Blackout (Unflavored) | $28 | `can-unflavored` |
| Concrete (Vanilla) | $30 | `can-vanilla` |
| Warzone (Mango Ginger) | $32 | `can-mango` |
| Titan (Chocolate) | $32 | `can-chocolate` |

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

## Customer Pre-Order Flow

1. Click **Pre-Order Now**
2. Select products and quantities
3. Fill in shipping details
4. Place order → saved to Firestore
5. Confirmation with order ID (e.g. `MK-M4X8K2AB`)
6. Social share buttons

---

## Design

- **Palette:** Burnt copper `#c47a3a`, warm stone `#8a7e72`, on near-black `#0c0c0c`
- **Always dark** — no light mode
- **Cans:** Matte dark charcoal bodies with copper color bands
- **Animations:** Scroll reveal, number counters, mouse-follow parallax, countdown timer
- **Responsive:** Fully mobile-friendly
