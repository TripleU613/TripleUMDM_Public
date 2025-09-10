

# TripleU MDM v3.7

**TripleU MDM** is a simple, powerful, all-in-one Mobile Device Management (MDM) solution designed to give our community safe, secure, and responsible technology.

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
   adb shell pm grant com.tripleu android.permission.WRITE_SECURE_SETTINGS
   ```
3. Or use our [automatic installer](https://installer.jtechforums.org) directly from your computer browser.

---

## 📌 Notes

* Versions prior to **3.7** are archived and no longer supported.
* Future plans include:

  * Online MDM management.
  * Full content-filtering VPN.

---

## 🙏 Contributing & Support

* We thank the few contributors and donors who have supported us so far.
* If you’d like to help grow this project, please consider donating or partnering with us.
* Contact: [tripleu.org](https://tripleu.org)
