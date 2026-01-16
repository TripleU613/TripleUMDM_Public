# TripleU MDM 4.0 - User Guide

This guide covers installation, enrollment, and daily use. Screenshots are collapsed under Image sections to keep the page clean. The UI may vary slightly by version.

---

## Before You Start

- Prepare a computer for the installer or ADB.
- Enable Developer Options and USB Debugging on the device.
- Have access to the email address you will use for login.

---

## Step 1 - Welcome

Open the app and accept the Terms of Use.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803482593-step-one.png" width="400"/></p>
</details>

---

## Step 2 - Sign In or Reset PIN

- Sign in with your existing account, or
- Reset your PIN if you forgot it.

<details>
<summary>Images</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803530990-screenshot_20251110_001735.png" width="400"/></p>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803540773-screenshot_20251110_001758.png" width="400"/></p>
</details>

---

## Step 3 - Create an Account

If you are new, create an account with your email, password, and PIN. The PIN is your primary access code.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803561319-screenshot_20251110_001751.png" width="400"/></p>
</details>

After registration, verify your email and return to the app to continue. Check Spam folders if the message does not appear.

---

## Step 4 - Grant Permissions

Use the online installer or manual ADB commands.

### Option A: Online installer

https://installer.jtechforums.org

Follow the on-screen steps to connect the device and complete enrollment.

### Option B: Manual ADB setup

```bash
adb shell dpm set-device-owner "com.tripleu.mdm/.a"
adb shell pm grant com.tripleu.mdm android.permission.WRITE_SECURE_SETTINGS
```

If the device owner command fails, temporarily disable apps that hold accounts (for example, Google Play Services), run the command, then re-enable them. On Android 14+, a reboot may be required.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803601172-screenshot_20251110_001929.png" width="400"/></p>
</details>

---

## Step 5 - Enter the App

Use your PIN (not your password) to enter the dashboard.

<details>
<summary>Images</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803630243-screenshot_20251110_002307.png" width="400"/></p>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803639576-screenshot_20251110_002136.png" width="400"/></p>
</details>

---

## Core Sections

### System

- Block adding new users.
- Disable factory reset and safe boot.
- Block developer options and app settings control.
- Block calls and SMS/MMS.
- Enable lockout mode for strict focus windows.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803675090-screenshot_20251110_002121.png" width="400"/></p>
</details>

### Installation

- Block APK installs.
- Block new apps while allowing updates.
- Block the Play Store.
- Allow user updates from the lock screen.
- Approve or reject apps in the detection console.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803695241-screenshot_20251110_002115.png" width="400"/></p>
</details>

### Accessibility

- Block WhatsApp Status, Channels, and Updates tabs.
- Block in-app AI chats.
- Block in-app browsers with exceptions.
- Block Gboard GIF and media search.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803716929-screenshot_20251110_002107.png" width="400"/></p>
</details>

### Network

- Enable Private DNS filtering.
- Use the firewall VPN to control apps and domains.
- Whitelist-only browsing when needed.
- Block Wi-Fi, hotspot, or all traffic.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803737884-screenshot_20251110_002057.png" width="400"/></p>
</details>

---

## Updates

The Updates screen lets you update apps directly. If an update fails due to signature mismatch, you can mute it and unmute it later in Settings.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803919711-screenshot_20251110_002049.png" width="400"/></p>
</details>

---

## Apps Tab

Select one or multiple apps and apply policies such as offline mode, in-app browser blocking, or uninstall protection.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803955844-screenshot_20251110_002004.png" width="400"/></p>
</details>

---

## Settings Tab

- Switch languages and adjust UI density.
- Import or export profiles.
- Import a whitelist file.
- Manage muted updates.
- Reset PIN, uninstall, or delete account.

<details>
<summary>Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762804003309-screenshot_20251110_001954.png" width="400"/></p>
</details>

---

## Remote Access (Optional)

Remote support sessions can be started from the portal. The user must accept the request before any screen access starts.

---

## Troubleshooting

- If device owner enrollment fails, disable apps that hold accounts, run the command, then re-enable them.
- If you do not receive the verification email, check Spam or Promotions folders.
- If an update fails, try muting the app or reinstalling from the official source.

---

## Support

- Community support: https://jtechforums.org
- Main website: https://tripleu.org
