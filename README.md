# TripleU MDM v3.7 → v3.8

[**▶ Install Online**](https://installer.jtechforums.org) • [**Latest Guide**](#-user-guide-v38) • [**Issues**](https://jtechforums.org) • [**Website**](https://tripleu.org)

> **TL;DR**: v3.8 is faster, stricter, fully translated (Hebrew toggle), with Safe Mode protection, refined WhatsApp controls, and a Compose UI overhaul.

**TripleU MDM** is a simple, powerful, all-in-one Mobile Device Management (MDM) solution designed to give our community safe, secure, and responsible technology.

---

## 🚀 What’s New in v3.8

<details>
<summary><b>Changelog (tap to expand)</b></summary>

* Added Safe Mode protection
* Added root self-grant support
* Removed unnecessary permission prompts
* Fully translated app (includes Hebrew switch)
* Added call blocking and video blocking
* Fixed crashes after enabling restrictions
* Fixed Google sign-in blocked by WebView filter
* Fixed and refined WhatsApp Channels/Status blocking
* Added version codename in Settings
* Allowed longer PINs (no 8-digit limit)
* Added whitelist domains GUI
* Added daily “Fact of the Day”
* Updated Google APIs for locked-out users
* Rebuilt UI using Jetpack Compose
* Many performance and stability fixes

</details>

*Stable, cleaner, and more powerful than ever.*

---

## ✨ Features

* **App Control**

  * Make specific apps *offline* or *online*.
  * Block in-app browsers.
  * Disable, hide, suspend, or block app uninstallation.

* **Network & Ads**

  * Block all ads and social media sites via **Private DNS**.
  * Upload a **URL whitelist** so that only approved sites are accessible.
  * Option to take the *entire device offline*.

* **System Restrictions**

  * Block app installation, hotspot & tethering.
  * Disable developer options, factory reset with FRP, user additions.
  * Block SMS/MMS.

* **Accessibility Controls**

  * Block in-app AI chats.
  * Restrict WhatsApp status and channels.
  * Block GIFs and media search in Gboard.
  * Disable launching Google Maps and the Google app.

* **Recovery & Support**

  * Forgotten PIN? Receive an email recovery link.
  * For those who no longer need filtering, remote uninstallation is available (small fee applies).
  * Remote updates: bug fixes and improvements are pushed directly, no manual work required.

* **Free for the Community**

  * 100% free to install and use.
  * Donations welcome to help support ongoing development.

---

## 🛡️ Privacy & Security

* We **do not collect personal data**.
* Minimal technical info (device model, Android version, serial number) is collected *only* for troubleshooting.
* This app is strictly for **private use**. Do not reverse-engineer, redistribute, or use it commercially.

Abuse prevention: if our systems detect suspicious activity (too many duplicate emails, numbers, PINs, or similar patterns), remote uninstall and ban may be triggered automatically.

---

## ⚠️ Disclaimer

* We are **not responsible** for bricked devices, factory resets during FRP, or situations where you enabled "all network block" and then tried to remote-uninstall.
* Please use responsibly and at your own risk.

---

## 🚀 Installation

1. Install the app on your device.
2. Run the following ADB commands:

   ```bash
   adb shell dpm set-device-owner "com.tripleu.mdm/.a"
   adb shell pm grant com.tripleu.mdm android.permission.WRITE_SECURE_SETTINGS
   ```
3. Or use our [automatic installer](https://installer.jtechforums.org) directly from your computer browser.

---

## 📘 User Guide (v3.8)

Everything you need to set up and manage TripleU MDM:

<details>
<summary><b>Open the step‑by‑step guide</b></summary>

### Step 1 – Welcome

When opening **TripleU MDM** for the first time, agree to the *Terms of Use*.

<details><summary>📷 Image</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803482593-step-one.png" width="400"/></p></details>

### Step 2 – Sign In or Reset PIN

Sign in with your existing account or reset your PIN if forgotten.

<details><summary>📷 Images</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803530990-screenshot_20251110_001735.png" width="400"/></p><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803540773-screenshot_20251110_001758.png" width="400"/></p></details>

### Step 3 – Create an Account

Fill in your *email*, *password*, and *PIN code* (used for login). Check your email for a verification link.

<details><summary>📷 Image</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803561319-screenshot_20251110_001751.png" width="400"/></p></details>

### Step 4 – Grant Permissions

Grant permissions with **ADB** or use the online installer.

```bash
adb shell dpm set-device-owner "com.tripleu.mdm/.a"
adb shell pm grant com.tripleu.mdm android.permission.WRITE_SECURE_SETTINGS
```

<details><summary>📷 Image</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803601172-screenshot_20251110_001929.png" width="400"/></p></details>

### Step 5 – Enter the App

Enter your **PIN** (not password) and access the dashboard with daily facts and tips.

<details><summary>📷 Image</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803639576-screenshot_20251110_002136.png" width="400"/></p></details>

### Step 6 – Sidebar Overview

Control system, installation, accessibility, and network features.

<details><summary>📷 Image</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803675090-screenshot_20251110_002121.png" width="400"/></p></details>

### Step 7 – Updates

Manage app updates directly; mute problematic apps if needed.

<details><summary>📷 Image</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803919711-screenshot_20251110_002049.png" width="400"/></p></details>

### Step 8 – Apps Tab

Select multiple apps, apply policies, block WebView, or set apps offline.

<details><summary>📷 Image</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803955844-screenshot_20251110_002004.png" width="400"/></p></details>

### Step 9 – Settings Tab

Switch language, import whitelists, manage muted apps, reset PIN, or uninstall.

<details><summary>📷 Image</summary><p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762804003309-screenshot_20251110_001954.png" width="400"/></p></details>

</details>

---

## Notes & Support

Report bugs on [jtechforums.org](https://jtechforums.org) or get direct help at [tripleu.org](https://tripleu.org).

If you want to translate or improve this guide, post your version in the forum thread and tag me.

**Enjoy and good luck!**
