# DigiBloom website — Android-friendly setup (Tanglish)

## Website-la enna irukku?
- Cream background, black buttons, stylish product cards
- Search bar + category filters
- Product detail popup
- Shopping bag/cart + checkout form
- Razorpay order creation and payment signature verification starter
- Sample downloadable files

## Mukkiyam — launch panna munnaadi
Indha ZIP oru working starter project. Product files ippodhu **sample placeholder text files**. Un original PDF/poster files-a `public/downloads/` folder-la replace pannanum. Demo mode-la real payment nadakkaadhu. Live payment-ku Razorpay account, keys, backend hosting, HTTPS, and secure download-token/database work thevai.

## Android-la easiest preview
1. ZIP file download pannitu Android Files app-la extract pannu.
2. Mobile browser-la local HTML open pannina design preview aagalam; server/payment functions work aagaadhu.
3. Full website run panna Node.js support irukkura hosting service use pannanum. Hosting provider-la project files upload panni Node app deploy pannu. Static-only hosting (simple HTML hosting) `server.js` payment endpoints-a run pannaadhu.
4. Project root-la terminal irundhaal:
   - `npm install`
   - `.env.example`-ai `.env` nu copy pannu
   - Razorpay Dashboard-la irundhu TEST Key ID + TEST Key Secret add pannu
   - `npm start`
5. Browser-la hosting URL open pannu.

## Razorpay test keys
- Razorpay Dashboard-la account create/verify pannitu Test Mode keys eduthu `.env`-la mattum add pannu.
- Secret key-a `public/` folder-la podaadha; yaarukkum share pannaadha.
- Test payment success aagura flow-ai test pannitu, account approval mudinja piragu live keys use pannu.
- UPI methods and availability Razorpay account setup/eligibility-ku depend aagum.

## Security before real customers
Starter code-la download route demonstration purpose-ku simple-a irukku; direct URL therinja file access aagalaam. **Live launch-ku munnaadi** database-la order store panni, verified payment-kku piragu short-lived, single-use download token generate pannura system add pannanum. Email delivery, order history, refunds, privacy policy, terms, GST/tax applicability and customer support details-um set pannu. Never mark an order paid based only on browser redirect; verify server-side and preferably confirm via Razorpay webhooks.

## Sample products
- The Self-Care Planner — ₹99
- The Creator Poster Pack — ₹149
- The Mini E-book Bundle — ₹199

`public/app.js`-la product title, price, description change pannalaam. `server.js`-la product IDs and amounts match aaganum. Prices in server are paise: ₹99 = 9900.

## Important
This project is a starter, not a fully audited commerce platform. Don't accept live payments until protected downloads, order database, webhook verification, and hosting secrets are configured and tested.
