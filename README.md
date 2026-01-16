<img width="900" height="512" alt="Untitled design" src="https://github.com/user-attachments/assets/c4311169-c8f1-4bdc-ab3f-80db811c064b" />


# TripleU MDM

Welcome to the public release repo for TripleU MDM.

Install with the website installer:
https://mdm.tripleu.org

Access your MDM dashboard (console):
https://mdm.tripleu.org/login

Comments and feedback:
https://forums.jtechforums.org/t/regarding-upcoming-tripleumdm-v4-0/5535?u=tripleu

Questions for the Israeli community:
https://mitmachim.top/topic/87888

Technical support:
https://tripleu.org (contact)

Donations:
https://tripleu.org (multiple payment methods)

Want to write a guide or improve the docs? Open a PR to this repo.
Issues: https://github.com/TripleU613/TripleUMDM_Public/issues (or mention them on either forum).

## Manual install (ADB)

If the website installer does not work, run:

```bash
adb shell dpm set-device-owner "com.tripleu.mdm/.a"
adb shell pm grant com.tripleu.mdm android.permission.WRITE_SECURE_SETTINGS
```

## Usage

This MDM is for private use only. Commercial use can receive discounts by contacting us at https://tripleu.org.
