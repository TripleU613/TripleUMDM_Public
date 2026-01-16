# TripleU MDM v3.8 – User Guide

This guide is formatted for **guide.md** on GitHub with all screenshots hidden under expandable “Image” sections for a cleaner layout.

---

## Step 1 – Welcome

Welcome to **TripleU MDM**! When you open the app for the first time, you’ll be asked to agree to the *Terms of Use*.

Please read and agree to continue — basically, it means you’re agreeing to use the app responsibly (**and don’t sue us 😉 just kidding**).

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803482593-step-one.png" width="400"/></p>
</details>

---

## Step 2 – Sign In or Reset PIN

On this screen you can **sign in to your existing account** or **reset your PIN** if you’ve forgotten it.

If you already have an account, enter your email and PIN, then press **Sign In**.

If you forgot your PIN – tap **Reset PIN**, enter your email, and you’ll receive a **recovery link**.

<details>
<summary>📷 Images</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803530990-screenshot_20251110_001735.png" width="400"/></p>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803540773-screenshot_20251110_001758.png" width="400"/></p>
</details>

---

## Step 3 – Create an Account

Here you can **create a new account**. Fill in your *email*, *password*, and *PIN code*.

The PIN is your **main access code** — you’ll need it every time you log in. Make sure to remember it!

After filling in all fields, press **Register** to complete setup.

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803561319-screenshot_20251110_001751.png" width="400"/></p>
</details>

After registration, you’ll get a **verification email**. It might land in your **Spam** folder — check there if you don’t see it.

Inside the email is a **verification link** you must click. Once verified, go back to the app and tap **“I verified”** to continue.

⚠️ Note: *Firebase* announced that this verification service might be discontinued in the future, so occasional errors may occur — for now, it works fine.

---

## Step 4 – Grant Permissions

You’ll need to grant the app the required permissions. Usually, only **ADB commands** are needed:

```bash
adb shell dpm set-device-owner "com.tripleu.mdm/.a"
adb shell pm grant com.tripleu.mdm android.permission.WRITE_SECURE_SETTINGS
```

You can also use the online installer: [installer.jtechforums.org](https://installer.jtechforums.org)

If you get an error, you may need to **temporarily disable apps that hold accounts** (like *com.google.android.gms*), run the command, then re-enable them.

On Android 14+, a **device restart** may be required. If you see a warning about Google services after reboot — don’t worry, everything’s fine.

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803601172-screenshot_20251110_001929.png" width="400"/></p>
</details>

---

## Step 5 – Enter the App

After granting permissions, tap **Enter**. You may see the PIN screen again — enter your **PIN code** (not your account password).

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803630243-screenshot_20251110_002307.png" width="400"/></p>
</details>

Once logged in, you’ll reach the dashboard — it’s mainly visual, showing **daily facts**, **tips**, and **notices**, but no user action is required.

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803639576-screenshot_20251110_002136.png" width="400"/></p>
</details>

---

## Step 6 – Sidebar

### 🛠️ System

* Block adding new users
* Disable factory reset (FRP)
* Block developer options
* Prevent access to app settings
* Block phone calls and SMS

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803675090-screenshot_20251110_002121.png" width="400"/></p>
</details>

### 📦 Installation

* **Disable APK Install** – blocks new app installs.
* **Block New Apps** – allows updates but prevents new installs.
* **Allow User Updates** – gives shortcut to update screen from lockscreen.
* **Block Play Store** – quickly disables Google Play.

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803695241-screenshot_20251110_002115.png" width="400"/></p>
</details>

### ♿ Accessibility

* **Android Auto Quirk** – prevents Maps or QuickSearchBox launch but keeps them functional.
* **Block WhatsApp Tabs** – hides Channels, Status, and Updates tabs.
* **Block In-App AI** – disables Gemini, Meta AI, and other built-in AIs.
* **Block In-App Browsers** – detects and prevents embedded browsers.

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803716929-screenshot_20251110_002107.png" width="400"/></p>
</details>

### 🌐 Network

* **Block Hotspot** – prevents hotspot/tethering.
* **Block All Traffic** – cuts all internet access (no updates possible!).
* **Enable Private DNS** – default: `all.dns.mullvad.net` (blocks social media).
* **Enable Firewall VPN** – manage offline/online app access.
* **Whitelist Domains** – allow access only to approved sites.

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803737884-screenshot_20251110_002057.png" width="400"/></p>
</details>

---

## Step 7 – Updates

The update screen lets you update apps directly. If an update fails, it’s usually due to signature mismatch (e.g., *APKPure* versions). You can **mute** an app and later unmute it from settings.

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803919711-screenshot_20251110_002049.png" width="400"/></p>
</details>

---

## Step 8 – Apps Tab

Here you can **select multiple apps**, **apply policies**, **block WebView**, or **set apps offline** via the VPN feature.

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762803955844-screenshot_20251110_002004.png" width="400"/></p>
</details>

---

## Step 9 – Settings Tab

* **Switch to Hebrew** – switch interface language
* **Import Whitelist** – import a text file of allowed domains
* **Privacy / Support** – access privacy policy and support
* **Muted Apps** – manage muted apps
* **Reset PIN / Uninstall** – reset MDM PIN or uninstall app

<details>
<summary>📷 Image</summary>
<p align="center"><img src="https://mitmachim.top/assets/uploads/files/1762804003309-screenshot_20251110_001954.png" width="400"/></p>
</details>

---

## Notes & Support

Report bugs on [jtechforums.org](https://jtechforums.org) or get direct help at [tripleu.org](https://tripleu.org).

If you want to translate or improve this guide, post your version in the forum thread and tag me.

**Enjoy and good luck!**
