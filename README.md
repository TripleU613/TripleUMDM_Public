# TripleU MDM 4.0

[Install Online](https://installer.jtechforums.org) | [User Guide](./Guide.md) | [Website](https://tripleu.org) | [Privacy](./Privacy.md) | [Support](https://jtechforums.org)

TripleU MDM is a community-built Android management platform for focused, secure devices. It combines device policies, app controls, network filtering, and remote management in one place.

This repository is the public release hub for the Android app and its documentation.

---

## At a Glance

- Full Android device management with strict policy enforcement.
- App approvals and per-app controls including offline mode and uninstall protection.
- Network filtering with Private DNS, firewall VPN, and domain allowlists.
- Accessibility protections for WhatsApp, AI chat, in-app browsers, and more.
- Built-in updater with update-all, mute updates, and background checks.
- Optional web portal with remote management and screen support.

---

## 4.0 Highlights

- Expanded policy coverage across system, installation, network, accessibility, and apps.
- Fine-grained app control: hide, suspend, disable, offline, and block in-app browsers.
- Premium VPN option with category filtering, image filtering, and word detection.
- Remote access with explicit user approval to protect privacy.
- Profile export/import and whitelist import for fast setup.
- English and Hebrew interface with adjustable UI density.

---

## Who It Is For

- Families and communities who want consistent, safe devices.
- Schools and organizations that need centralized control.
- Individuals who want a distraction-free phone that stays locked down.

---

## Feature Map

### Device and System Controls

- Block adding new users.
- Disable factory reset and safe-boot routes.
- Block developer options.
- Block access to app settings controls.
- Block phone calls and SMS/MMS.
- Lockout mode for strict focus windows.

### Installation and App Approvals

- Block APK installs.
- Block new app installs while allowing updates.
- Block the Play Store with one switch.
- App detection console for pending installs and approvals.
- Allow user updates from the lock screen when needed.

### App Controls

- Hide, suspend, or disable apps.
- Block uninstall for managed apps.
- Make apps offline using the firewall VPN.
- Block in-app browsers per app or across the device.
- Add WebView exceptions for trusted apps.
- Block video in supported apps.

### Network and Web Filtering

- Private DNS toggle for system-wide filtering.
- Firewall VPN for per-app network control.
- Domain whitelist mode for strict, approved-only browsing.
- Domain blacklist mode for targeted blocking.
- Block all traffic mode for full offline lockdown.
- Block Wi-Fi and hotspot/tethering.

### Accessibility Protections

- Block WhatsApp Status, Channels, and Updates tabs.
- Block in-app AI chats (Gemini, Meta AI, and similar).
- Block in-app browsers globally with an exception list.
- Block Gboard GIF and media search features.
- Prevent quick-launch routes in Google Search and Maps from bypassing rules.

### Updates and Maintenance

- Built-in app updater with update-all support.
- Mute specific apps so they never appear in the updater list.
- Background update checks and update notifications.
- Critical fixes can be delivered remotely when needed.

### Settings and Recovery

- Switch interface language between English and Hebrew.
- Import or export a full profile to reuse policies.
- Import a domain whitelist from a file.
- Account info, privacy policy, and support links inside the app.
- App density control for compact or comfortable layouts.
- PIN reset and account deletion tools.

### Remote Management and Support

- Remote commands: sync, lock, wipe, or uninstall.
- Remote support with screen sharing and remote input.
- Device status, last seen, and policy summaries in the portal.
- Device notes for quick context.

---

## VPN and Filtering Options

TripleU offers three filtering paths depending on your needs:

| Option | Summary |
| --- | --- |
| Per-app offline (free) | Take selected apps offline without impacting the rest of the device. |
| Local whitelist (free) | Allow only approved sites when the firewall VPN is active. |
| Premium VPN (paid) | Category filtering, ad and tracker blocking, image filtering, and word detection. |

Premium VPN is optional and requires a subscription.

---

## Supported Apps for Advanced Filtering

TripleU continuously expands coverage. Current supported apps include:

- Moovit
- Waze
- WhatsApp
- Gmail
- Gboard
- Spotify
- Google Maps
- Chrome (full filtering)

---

## Pricing at a Glance

- First device is free.
- Add a second device for a one-time $10 fee.
- Premium VPN is $15 per 3 months.

---

## Admin Portal (Optional)

The web portal provides centralized control across devices:

- Manage multiple devices from one dashboard.
- Approve apps and apply policies remotely.
- Start and stop remote support sessions.
- View device health and policy summaries.

---

## Installation

### Option 1: Online Installer

Use the browser-based installer:

https://installer.jtechforums.org

### Option 2: Manual ADB Setup

Install the APK, then run:

```bash
adb shell dpm set-device-owner "com.tripleu.mdm/.a"
adb shell pm grant com.tripleu.mdm android.permission.WRITE_SECURE_SETTINGS
```

If the device owner command fails, temporarily disable apps that hold accounts (for example, Google Play Services), run the command, then re-enable them.

---

## First-Time Setup

1. Open the app and accept the Terms of Use.
2. Sign in or create an account.
3. Verify your email and return to the app.
4. Grant device owner permissions.
5. Enter the app using your PIN.

---

## Daily Use Guide

### Home

- Overview of active policies.
- Device status, last seen, and quick summaries.
- Daily tips and notices.

### System

- Core restrictions like factory reset, developer options, calls, and SMS.
- Lockout mode for strict focus times.

### Installation

- Control how new apps are installed.
- Approve or reject pending apps.
- Keep updates available without allowing installs.

### Network

- Private DNS and firewall VPN controls.
- Whitelist-only browsing modes.
- Block Wi-Fi, hotspot, or all traffic.

### Accessibility

- Block unwanted UI paths inside apps.
- WhatsApp and AI restrictions.
- In-app browser controls.

### Apps

- Apply app policies in bulk.
- Mark apps as offline or block uninstall.
- Block video or in-app browsers where needed.

### Updates

- Update apps in one place.
- Mute problematic updates.
- Keep the device stable and predictable.

### Settings

- Switch languages, import/export profiles, and manage muted updates.
- Reset PIN, uninstall, or delete account.

---

## Updates

TripleU MDM checks for updates in the background and can prompt you when a new build is available. Managed devices can also be updated silently when possible.

---

## Privacy and Data

- We do not sell data.
- Minimal technical data is used only for support and device management.
- The app is for private, community use. Do not redistribute or repackage it.

See the full policy here: [Privacy](./Privacy.md)

---

## Support

- Community support: https://jtechforums.org
- Main website: https://tripleu.org

---

## Disclaimer

Use at your own risk. Device owner tools are powerful, and misconfiguration can lock you out or block connectivity. Make sure you understand each restriction before enabling it.
