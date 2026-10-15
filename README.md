# ESP Dashboard

A production-ready React and Firebase SPA for managing ESP32/ESP8266 devices with live telemetry, relay control, output management, and history visualization.

## Quick Start

```bash
npm install
npm run dev
```

## What this app does
- Authenticates users via Firebase Email/Password.
- Registers and links ESP devices to user accounts.
- Shows device status, sensor telemetry, relay state, and output controls.
- Sends real-time commands to ESP devices through Firebase Realtime Database.
- Displays historical sensor data using Recharts.

## Key folders
- `src/pages/` — route-level screens.
- `src/components/` — reusable UI components.
- `src/firebase/` — Firebase Auth and Realtime Database access.
- `src/hooks/` — subscription and auth hooks.
- `src/utils/` — helper functions and demo data.

## Deployment
The `main` branch is configured to deploy to GitHub Pages through `.github/workflows/deploy.yml`.

1. In the GitHub repository, open **Settings → Pages** and set the build source to **GitHub Actions**.
2. Push this branch to GitHub, or run the **Deploy to GitHub Pages** workflow manually from the Actions tab.
3. Once the workflow succeeds, the app will be available at <https://ra564-5.github.io/iotProject/>.

Before using real accounts or devices, add `ra564-5.github.io` to the authorized domains in Firebase Authentication and verify that Realtime Database rules restrict access to authenticated users and their permitted devices.

To build the static bundle locally:

```bash
npm run build
```

## Documentation
For developer, deployment, and maintenance details, see `TECHNICAL_DOCUMENTATION.md`.
