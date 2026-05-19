# OnOff-Remote (Updated Fork)



A simple webOS application to toggle the `piccap` service on your LG TV by hijacking dedicated remote buttons (e.g., Netflix, Amazon).

## Setup Instructions

### 1. Uninstall the Original App
**Crucial:** Before installing this, you must **uninstall** the official application you intend to remap (e.g., uninstall the real Netflix app) from your TV. If the official app remains installed, the TV will prioritize it and launch the official app instead of this one.

### 2. Configure the Button
To change which button triggers the service, open `app/appinfo.json` and update the `"id"` field:

- **For Netflix:** `"id": "netflix"`
- **For Amazon Prime:** `"id": "amazon"`

*Note: The ID must match the internal system ID of the app you are hijacking.*

### 3. Build & Install

Ensure you have `ares-tools` installed:
```bash
npm install -g @webosose/ares-cli
```

Build the package:
```bash
ares-package app/
```

Install the generated `.ipk` file to your TV:
```bash
ares-install <path-to-generated-ipk-file>
```

---
*Based on the original project: https://github.com/Bahoue/OnOff-Remote*
