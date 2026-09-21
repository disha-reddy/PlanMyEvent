# PlanMyEvent
 
A Tampa-based, two-sided event vendor marketplace prototype. PlanMyEvent matches hosts planning any kind of event — weddings, birthdays, corporate events, graduations, galas, and more — with verified local vendors across catering, photography, florals, DJ/audio, and venues.
 
This repo is a **front-end prototype**: a single self-contained HTML file with no backend, no build step, and no real database. It's built to demo the full product flow end to end.
 
## What it does
 
### Host side
- Browse vendors ranked by an algorithmic matching engine (budget fit, location, style, capacity, and quality/trust score)
- Set a total event budget, which is split across categories to drive matching
- Manage up to 3 active events at once, each with its own vendor matches, budget, and guest list
- View and edit event details after creation
- Book a vendor with a deposit held today and the balance due later, followed by a booking confirmation screen
- Invite guests via a shareable RSVP link and track attendance
- Message vendors directly before booking (optional, never required)
### Vendor side
- Publish a listing with category-specific credential requirements (e.g. a Florida catering license, venue occupancy/fire-safety docs, or business registration + insurance + portfolio minimum)
- Edit an existing listing at any time — including after renewing an expired credential
- Manage blocked/unavailable dates independently of publishing, no republish required
- Track open leads, quotes sent, and bookings won from a vendor dashboard
- Listings are automatically suspended if a required credential expires, and automatically restored once fixed
### Matching engine
Vendors are ranked per category using weighted scoring across budget fit, location, style alignment, capacity, and quality/trust, with hard filters on service category and date availability.
 
## Tech stack
 
- Vanilla HTML, CSS, and JavaScript — no framework, no build tooling
- Google Fonts (Fraunces + Inter)
- State is held in memory and persisted to the browser's `sessionStorage`, so a reload keeps your progress but closing the tab resets to the seed data
## Running it
 
No install or server required — just open the file in a browser:
 
```bash
open planmyevent.html   # macOS
# or double-click the file / drag it into a browser tab
```
 
To serve it locally instead:
 
```bash
python3 -m http.server 8000
# then visit http://localhost:8000/planmyevent.html
```
 
## Demo accounts
 
Authentication is mocked for demo purposes — any name/email you enter works, no password required. Signing in as a vendor always resolves to the same demo vendor account, which already has one live catering listing seeded so you can try the edit/availability flows immediately without publishing from scratch.
 
## Known limitations
 
- No real backend, database, authentication, or payment processing — everything is client-side mock data
- State does not persist across browser sessions by design (see Tech stack)
- Not production-ready; built as a clickable prototype to validate product flow and UX
