# based-pos-and-inv-system
A simple POS & inventory frontend that stores data in Firestore for persistence. The app can be deployed as a static site (e.g. GitHub Pages) and will read/write to a remote database.

## Deployment
1. Create a Firebase project (https://console.firebase.google.com).
2. Enable Firestore in test mode (or configure rules appropriately).
3. In `index.html`, replace the `firebaseConfig` placeholder with your project's configuration object.
4. Ensure the following SDK scripts are included (already in `index.html`):
   - `firebase-app-compat.js`
   - `firebase-firestore-compat.js`
5. Push the repository to GitHub and enable GitHub Pages on the `main` branch. The front-end will read/write to Firestore directly, so multiple users will see the same data.

Once configured, any change made through the UI (inventory updates, checkouts) will be persisted to Firestore. If you share the GitHub Pages URL, other users can modify the data as long as they have access under your Firestore rules.

## Existing link
https://erosgbcs.github.io/based-pos-and-inv-system/
