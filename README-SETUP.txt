WOWSHOPPING — CLEAN SINGLE-STOREFRONT BUILD

Architecture
- One storefront: index.html
- One admin panel: admin.html
- Firestore siteConfig/storefront is the authoritative storefront data source.
- Browser localStorage is NOT used as the source for products, categories, banners, branding, theme, menu or other storefront content.
- No service worker/PWA cache is included.
- PC, tablet and phone use the same HTML/data; responsive CSS changes layout only.
- vercel.json disables browser/CDN caching for the HTML entry points.

Firebase setup
1. Firebase Console -> Authentication -> Sign-in method -> enable Google.
2. Authentication -> Settings -> Authorized domains -> add your Vercel production domain.
3. Firestore Database -> create database.
4. The admin account must have the custom claim: admin=true.
5. Deploy this folder to Vercel.
6. Open admin.html, sign in with the authorized admin account, and save the storefront settings.

Important
The Firebase web config is intentionally included in the frontend. Firebase API keys identify the project; Firestore/Authentication Security Rules and custom claims must enforce access.
