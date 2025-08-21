
# 📱 TripleU MDM

**Simple, strict, and offline Android MDM** – no accounts, no setup, no nonsense.

> 🔄 *This app is updated frequently. Until an official release, the APK link may be refreshed daily.*

---

## ✅ Features

This MDM app is focused on simplicity and control. Here's what it can do:

* Block Play Store
* Block Developer Options
* Block APK installations
* Block internet access
* Block app uninstalls
* Disable MMS and SMS
* Block Bluetooth
* Block access to App Settings
* Set and lock custom DNS
* VPN integration
* Block root access
* Prevent adding users
* Block factory reset
* Suspend, disable, or hide apps
* Block network access on a per-app basis
* Self update
* Hosts filtering
* Block webviews
---

## 🔧 Installation (via ADB)

Run the following commands to set up the app as a Device Owner (**note the new command**):

```bash
adb shell dpm set-device-owner com.aurora.store/.AdminReceiver
```

Grant secure settings permissions:

```bash
adb shell pm grant com.aurora.store android.permission.WRITE_SECURE_SETTINGS
```

---

Enjoy!
Simple. Strict. Local.

