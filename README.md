# DriveMeNuts 🚗

A zero-dependency, single-file progressive web app for tracking your car's fuel fill-ups, car washes, and service history — with a built-in dashboard and optional Google Sheets sync.

---

## Features

- **⛽ Fuel tracking** — log fill-ups with gallons, price/gal, odometer, and auto-calculated MPG
- **🫧 Car wash log** — track wash type, location, and cost
- **🔧 Service history** — log repairs and maintenance with next-due mileage reminders
- **📊 Dashboard** — MPG trend chart, monthly cost breakdown, and service reminder status
- **🔔 Service reminders** — alerts when you're within 500 miles of a due service
- **📥 Fuelio import** — import your existing history from a Fuelio CSV export
- **☁️ Google Sheets sync** — optional real-time sync to a Google Sheet via Apps Script
- **🚗 Multi-vehicle** — up to 5 vehicles, each with their own history

## No install required

Everything is in a single `index.html` file — no build step, no dependencies, no server. Just open it in a browser.

Data is stored in your browser's `localStorage`.

---

## Usage

### Option A — Open locally

Download `index.html` and open it in any modern browser.

### Option B — Host it yourself

Upload `index.html` to any static host (GitHub Pages, Netlify, Vercel, etc.) and access it from your phone like a native app.

### Option C — Add to Home Screen (iOS / Android)

Open the hosted URL in Safari or Chrome → Share → **Add to Home Screen**. It runs full-screen with no browser chrome.

---

## Google Sheets Sync (optional)

1. Create a new Google Sheet
2. Open **Extensions → Apps Script**
3. Paste the script shown inside the app (Settings → View Apps Script code)
4. Click **Deploy → New Deployment → Web App**
   - Execute as: **Me**
   - Who has access: **Anyone**
5. Copy the Web App URL
6. In DriveMeNuts → Settings → paste the URL → Save

Every new entry is appended to your sheet in real time across three tabs: `Fuel`, `CarWash`, `Service`.

---

## Fuelio Import

If you're migrating from [Fuelio](https://www.fuelio.com/):

1. Fuelio → Menu → **Backup & Restore** → **Export to CSV**
2. In DriveMeNuts → **Import tab** → tap the drop zone → select the exported file

Fuel fill-ups, service costs, and wash costs all import in one shot.

---

## Tech

- Vanilla HTML / CSS / JavaScript — no frameworks, no build tools
- `localStorage` for persistence
- Canvas API for the MPG trend chart
- Fetch API for Google Sheets sync

## Browser Support

Any modern browser (Chrome, Safari, Firefox, Edge). Optimized for mobile.

---

## License

MIT
