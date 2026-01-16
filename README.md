# TripleU MDM

Welcome to the public release repo for TripleU MDM.

Install with the website installer:
https://mdm.tripleu.org

Access your MDM dashboard (console):
https://mdm.tripleu.org

Comments and feedback:
https://forums.jtechforums.org/t/regarding-upcoming-tripleumdm-v4-0/5535?u=tripleu

Questions for the Israeli community:
https://mitmachim.top/topic/87888

Technical support:
https://tripleu.org

Donations:
https://tripleu.org

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
