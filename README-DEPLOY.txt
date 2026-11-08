MONEYVERSE — PERSONAL FINANCE WEB APP
======================================

FILES
- index.html : app interface
- style.css  : complete styling and responsive layout
- app.js     : app logic and local data storage
- firebase.json : Firebase Hosting config

FEATURES
- Distinct editorial / money-envelope design
- Total balance across pockets
- Money in, money out, and transfers between pockets
- Multiple named money pockets with individual balances
- Dream funds / savings goals with deposits
- Daily allowance auto-credit (catch-up on next app open)
- Recurring income/expense schedules (daily, weekly, every 30 days)
- Upcoming bill reminders
- Activity search, type and month filters
- Cashflow chart for 7/30/90 days
- Financial health indicator and spending insights
- Sound effects, dark mode, profile name
- CSV export, JSON backup and restore

IMPORTANT DATA NOTE
This build uses browser LocalStorage. Data stays in this browser on this device and is not synced to another device. It is a personal tracker prototype, not a bank connection. Recurring schedules and daily allowance are processed when the app is opened; browsers do not run this static website in the background while it is closed.

DEPLOY TO FIREBASE HOSTING
1. Install Node.js: https://nodejs.org/
2. Open terminal in this folder.
3. Run: npm install -g firebase-tools
4. Run: firebase login
5. Run: firebase use --add   (choose a Firebase project)
6. Run: firebase deploy --only hosting
7. Firebase prints your live URL, usually https://PROJECT_ID.web.app

This package is configured for Firebase Hosting but is not deployed to an account yet.
To sync data across devices with secure user accounts, add Firebase Authentication + Firestore and owner-only Security Rules in a later version.
