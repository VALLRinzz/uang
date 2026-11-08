MONEYVERSE — FIREBASE CLOUD EDITION
==================================

FILES
- index.html, style.css, app.js: website
- firebase-config.js: paste your Firebase Web App config here
- firestore.rules: private per-user database rules
- firebase.json: Hosting + Firestore rules deployment config

STEP 1 — CREATE / SELECT A FIREBASE PROJECT
1. Open https://console.firebase.google.com/ and create a project (or choose one dedicated to Moneyverse).
2. In Project settings → General → Your apps, add a Web app (</>) if you have not already.
3. Copy the Firebase config object values into firebase-config.js. Do not paste the config into chat.

STEP 2 — ENABLE EMAIL LOGIN
1. Firebase Console → Authentication → Get started.
2. Open Sign-in method / Sign-in providers.
3. Enable Email/Password and save.

STEP 3 — ENABLE CLOUD DATABASE
1. Firebase Console → Firestore Database → Create database.
2. Choose production mode. Select a location close to your users; the database location cannot easily be changed later.
3. In the project folder terminal, run: npm install -g firebase-tools
4. Run: firebase login
5. Run: firebase use --add (select the same Firebase project).
6. Run: firebase deploy --only firestore:rules,hosting

STEP 4 — USE IT
1. Open the Hosting URL printed by Firebase.
2. Open Settings & data → Sync your money universe.
3. Create an account using email + password.
4. Existing browser data is copied to the cloud if the account has no cloud record yet.
5. Log in using the same account on another device to see synced data.

IMPORTANT
- This project is not deployed automatically. You must complete the Firebase Console setup and run the deploy command.
- Do not use Firestore test mode or public read/write rules. Deploy firestore.rules included here.
- Firebase Web config is intended to be present in browser code; database access is protected by Authentication and the owner-only rules. Never put service-account private keys in this website.
- If a cloud record already exists, it becomes the source of truth when you sign in. Export a JSON backup before changing accounts or resetting data.
- The app keeps a local browser copy for offline resilience; cloud sync runs while signed in and online.
- Daily allowance / recurring schedules are processed when the app is opened, not while it is closed.
