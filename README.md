# Check-In

A simple, Apple-style customer check-in app for iPhone and iPad.

- Tap **+ Check In** to add a customer: name, what they're wearing, location (A, B, C, GB + 1–6), product, trade-in, and how they'll pay.
- **Up Next** shows each customer's location, wait time, and tags like **Ready to pay**.
- Follows the device's light/dark mode.

## Sync and privacy

Up Next is shared by every device through Supabase — just open the app, no passcode.

- The Supabase tables (`ci_checkins`, `ci_store`) are locked; the app can only use the `ci_*` functions.
- There is no passcode, so anyone who has the app's link can see and change Up Next.
- Each customer is deleted automatically **1 hour after check-in**, by a scheduled job in Supabase, even if no device is open. **Helped**, **Remove** and **Clear All** delete right away.
- Customer info is no longer kept on the device itself.

## Install on iPhone or iPad

1. Open the GitHub Pages link in **Safari**.
2. Tap **Share → Add to Home Screen → Add**.

## Products

Only **iPhone**, **Multiple** (two iPhones) and **Trade-in** are shown right now. iPad, Mac, Apple Watch, Apple Home and Accessories are still saved in `index.html` with all their steps — to bring any back, add its name to the `ACTIVE` list near the top of the script.

iPhone models: DUO, 18 Pro, 18 Pro Max, Air, 17, 17e, 16 (edit the `MODELS` list to change them).
