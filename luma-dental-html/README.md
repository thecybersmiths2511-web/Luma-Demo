# Luma Dental Studio — Plain HTML, CSS & JavaScript

This is a static, framework-free conversion of the supplied Design Arena project. The original image files from `public/images/` have been copied unchanged into `images/`. The public visual direction is retained: warm cream/paper backgrounds, deep navy, restrained teal, Fraunces/Figtree typography, editorial spacing, rounded image frames, treatment cards, team profiles, hours, and map illustration.

## Run locally (Windows 10)

1. Extract the ZIP.
2. Open the extracted folder in VS Code.
3. In the VS Code terminal, run:

   ```bat
   py -m http.server 8000
   ```

   If `py` is unavailable, try `python -m http.server 8000`.

4. Open `http://localhost:8000` in your browser.
5. Public pages use hash-based navigation (`#/about`, `#/treatments`, etc.), so they also work when hosted on static GitHub Pages under a repository subpath.

No npm install, build step, React, Vite, or TypeScript is required.

## Hidden demo admin panel

The admin panel is embedded into the original public site and has no visible link or separate admin HTML page. To open it, use either hidden entry method:

- Press **Ctrl + Shift + L** while on the public website.
- Or click the footer copyright line 7 times within about 3.5 seconds.

Login: username `admin`, password `admin12345`. The admin interface replaces the public page only after the hidden trigger is used. Use **Return to site** to go back to the public website.

The supplied React/Vite project did **not** contain an admin panel or admin route. This conversion adds a demo admin panel. It supports overview counts, searching and managing demo enquiries, managing services and illustrative prices, managing offers, editing selected homepage copy, and resetting demo data.

### Important limitations

This is a **frontend-only portfolio demonstration**, not secure clinic software. The hidden keyboard/click trigger is only a way to keep the panel out of ordinary navigation, not real access control; a static GitHub Pages site cannot keep its admin code or client-side password secret. Do not use it for a real clinic or real patient data.


- The demo password is visible in client-side JavaScript and is not real security.
- Demo appointment requests, services, offers, and editable homepage copy are stored in the current browser's `localStorage`.
- Data does not synchronize across devices, browsers, or separate visitors.
- The public enquiry form stores a sample request locally so it appears in the admin panel. It does not send email, contact a clinic, or book an appointment.
- Never enter real patient details or sensitive medical information.
- All service prices are illustrative USD demo prices, not actual clinical fees.
- To restore the demo defaults, use **Demo settings → Reset all demo data**.

For a real clinic, replace the demo authentication and browser storage with a secure backend, server-side authorization/validation, a shared database, and appropriate privacy/security controls.

## Files

- `index.html` — public site entry point
- `styles.css` — design system and responsive styling
- `app.js` — public pages, routing, forms, and shared demo data rendering
- `admin.js` — hidden demo authentication, dashboard, and management actions
- `images/` — original image assets copied from the supplied project
- `favicon.svg` — original favicon

## Verification notes

- JavaScript syntax checked with `node --check` for `app.js` and `admin.js`.
- The ZIP is designed to run as static files; no dependency installation is required.
- Browser-based visual QA was not run in this environment. Please test the public site and admin workflows in your browser before presenting it to prospects.
