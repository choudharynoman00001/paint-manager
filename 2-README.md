# Paint Manager

Offline POS (point of sale) for paint shops - Windows desktop app.

**Features**
- **Bill** - counter billing with cash / udhaar, discount, printable 80 mm receipt
- **Maal (stock)** - paint brands, types, colours/shades with swatches, sizes (Quarter, 1 Litre, Gallon, Drum, putty kg), stock-in ("Maal aaya"), low-stock warnings
- **Udhaar (khata)** - customer credit ledger, wasooli (payments), WhatsApp reminder link (opens WhatsApp; message sends only when the shopkeeper taps send)
- **Report** - daily / 7-day / all sales, cash vs udhaar totals, CSV export, JSON backup + restore
- All data stays on the shop's own computer (offline, no internet needed)

## Install (Windows)
1. Open **Actions** → latest successful run → download **Paint-Manager-Setup**, or use the latest **Release**.
2. Run `Paint-Manager-Setup-x.x.x.exe`. Windows may show "Unknown publisher" (no paid code-signing certificate) - click **More info → Run anyway**.
3. First run loads demo stock (Brighto, Master, Nippon, Berger, Diamond, Gobis). Set the shop name in **Settings** and edit/delete demo items in **Maal**.

## Data safety
- All data (stock, bills, udhaar) is stored only on the shop's own computer, in the app's data folder (`%APPDATA%/paint-manager`). No internet account is needed.
- Installing a newer version keeps the data. Uninstalling does **not** delete the data folder.
- Even so, use **Report - Backup Download (JSON)** regularly (e.g. weekly) and keep the file somewhere safe (USB / Google Drive). Restore it any time from **Report - Backup Restore**.
- First run loads practice (demo) stock. For a real shop use **Settings - Khali start** to begin empty, or **Settings - Demo data reset** to get practice data back.

## Build from source
Requires Node.js 20+.
```
npm install
npm start        # run the app
npm run dist     # build dist/Paint-Manager-Setup-*.exe (Windows)
```

The `Build Windows installer` GitHub Action builds the installer whenever a `v*` tag (release) is pushed, and can also be run manually from the **Actions** tab.

DEVELOPER BY CHAUDHRY NOMAN · POWERED BY ALPHA BLUE DIGITAL · ALL RIGHTS RESERVED 2026
