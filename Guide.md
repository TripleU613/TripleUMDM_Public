Hi everyone!
Since I feel that **TripleUMDM**, even though it’s built with a nice UI and UX, is still pretty hard for newcomers to use, I decided to write a guide on how to get started. Hope you all enjoy!

---

## Step 1: Welcome

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_114849" src="https://github.com/user-attachments/assets/8871bf6f-249a-410e-bd1e-5a4d09290546" />

</details>

Since this app is an **MDM**, and I have no time for lawsuits, there’s a welcome page for a **privacy agreement**.
Note: clicking on *“I agree to the privacy policy”* will take you directly to the agreement and the repository.

---

## Step 2a: Create Account

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115002" src="https://github.com/user-attachments/assets/9fb82235-a5d6-4695-871d-f9806cf7faeb" />

</details>

Because the app can be remotely managed, and we don’t want to risk losing control of the MDM, there’s a **sign-in page**.
This will eventually be used with a **customer login portal**, where an admin will control a child or supervised device remotely.

Fill out:

* **Name** (doesn’t have to be real)
* **Phone number** (use your real one in case we need to contact you)
* **Password** (for your account)
* **PIN** (for logging into the app)

Why both password and PIN?
Because if you manage multiple users, each can have their own PIN — which you can share without exposing your main password.

After creating an account, you’ll receive an **email confirmation link**.
Check your spam folder if it doesn’t arrive.

---

## Step 2b: Sign In

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_114936" src="https://github.com/user-attachments/assets/82a82baf-5604-44d2-962a-418a53be3efa" />

</details>

If you already have an account, simply sign in.
The **PIN** can differ, but the **password** must match your account.

---

## Step 3: Permissions

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115058" src="https://github.com/user-attachments/assets/49ae3002-7ca0-4ba5-9e66-5a889193dd44" />

</details>

The first permissions required are **DPM** and **WRITE\_SECURE\_SETTINGS**.
You can:

* Grant them via PC,
* Use the online installer, or
* Do it with root using:

```bash
adb shell dpm set-device-owner "com.tripleu.mdm/.a"
adb shell pm grant com.tripleu.mdm android.permission.WRITE_SECURE_SETTINGS
```

On **OnePlus devices**, enable **“Disable permission monitoring”** in Developer Options.

Once granted, continue with the rest. If any permission fails, close the app and reopen — the prompt should disappear.

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115218" src="https://github.com/user-attachments/assets/84e5dc62-3479-431a-8296-6aebdf8d924a" />

</details>

After all permissions are set: **enter the app.**

---

## Step 4: Knowing the Options

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115324" src="https://github.com/user-attachments/assets/3f0c924a-329b-4bfe-a74d-05a7b5770b92" />

</details>

There are 4 categories:

1. **Network**
2. **Accessibility**
3. **Apps and Install**
4. **System**

---

### Network

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115342" src="https://github.com/user-attachments/assets/bae06d88-188b-455a-8ebf-90fc668805df" />
<img width="480" height="854" alt="Screenshot_20250912_115444" src="https://github.com/user-attachments/assets/5c24805c-f2e4-4ce3-a778-a8693946e312" />
<img width="480" height="854" alt="Screenshot_20250912_115842" src="https://github.com/user-attachments/assets/30aa1a05-1f30-40d2-9e96-dcd320413bff" />
<img width="480" height="854" alt="Screenshot_20250912_115819" src="https://github.com/user-attachments/assets/c0eb21e1-8e62-468b-a364-fd5a7ef446e6" />
<img width="480" height="854" alt="Screenshot_20250912_115825" src="https://github.com/user-attachments/assets/bed52683-5689-401c-a4c1-ff882211906d" />

</details>

* Disable hotspot and tethering.
* Disable all network access (**warning**: we won’t be able to connect remotely; if you lose your password, you’re locked out).
* Enable Private DNS (if you click **Save** without typing anything, it defaults to `all.dns.mullvad.net`).
* VPN/Firewall: enables making apps offline in **App Management**.
* Whitelist domains: lets you import a whitelist file. (**Note**: this disables DNS filter as they conflict.)

**Example:** Amazon works, but YouTube (not whitelisted) shows *DNS bad config* — meaning blocked.
**Note:** Apps using direct IP connections or raw sockets may still partially work, but DNS-reliant ones will fail.

---

### Accessibility

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115403" src="https://github.com/user-attachments/assets/0a0271ea-1cd4-4bf0-a2a5-f59decd96737" />
<img width="480" height="854" alt="Screenshot_20250912_115521" src="https://github.com/user-attachments/assets/039574ba-e7b7-4c87-bfbc-8113b1896f7c" />
<img width="480" height="854" alt="Screenshot_20250912_115540" src="https://github.com/user-attachments/assets/508d9b3c-bd10-4fdc-a7c5-14e1b208891e" />

</details>

* Android Auto fix: Google QuickSearchBox and Google Maps won’t function directly but Android Auto works fine.
* Block WhatsApp updates (includes channels).
* Block in-app AI (Meta in WhatsApp, Gemini in Google Messages).
* Block Gboard GIF search (only search; scrolling still works).
* Block all in-app browsers (unless WebView exceptions are set in **App Management**).

---

### Apps and Install

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115417" src="https://github.com/user-attachments/assets/7db8a7d9-26d9-4dbc-b26f-fc0499508d14" />

</details>

* Disable APK installation (blocks all install sources).
* Block new apps detection (new apps are blocked until unblocked in **App Management**).
* Block Play Store (hides it entirely).

---

### System

* Disallow adding users.
* Disable factory reset (forces FRP, may brick if reset from recovery — good or bad depending on use).
* Block Developer Options.
* Disable App Settings (prevents editing in Settings → Apps).
* Disable SMS and MMS.

---

### Settings Page

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115510" src="https://github.com/user-attachments/assets/42231e7a-0ac3-4236-a3dd-5cb27be50463" />

</details>

Includes:

* Reset MDM PIN (not account password)
* Import whitelist
* Privacy policy
* Account info (shows your email)
* Support us (donation link)
* Uninstall (removes the MDM)

---

### App Management

<details>
<summary>Tap to expand</summary>

<img width="480" height="854" alt="Screenshot_20250912_115620" src="https://github.com/user-attachments/assets/c3410a9c-4bb9-414f-b01c-73cf24a5afc3" />
<img width="480" height="854" alt="Screenshot_20250912_115540" src="https://github.com/user-attachments/assets/137c356f-49c8-4af2-8258-430775b33a17" />
<img width="480" height="854" alt="Screenshot_20250912_115620" src="https://github.com/user-attachments/assets/3be21712-4087-4444-af96-78128dfd3206" />

</details>

Tap an app for options, or long-press to select multiple. After selecting, press **Done**.

Options available (depending on settings):

* Hide
* Suspend
* Disable (hide+suspend)
* Block network (make offline)
* WebView block/exception
* Block uninstall (persistent)

Applied settings appear in the **Managed tab**, with color coding.

---

## That’s the Guide for Now

* We can remotely uninstall the app for you (minimal fee + ownership verification).
* Accounts used commercially may be suspended.
* Everything here was made by **TripleU**. My purpose is to **expand kedusha** in the community. Staying safe from the internet shouldn’t cost money — so please respect this and **do not charge** for installation.

---

## Contact

For custom versions, cooperation, or anything similar, visit [tripleu.org](https://tripleu.org).

Love y’all,
**TripleU aka, Usher Weiss**
