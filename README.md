
<p align="center">
  <img src="https://github.com/user-attachments/assets/c4311169-c8f1-4bdc-ab3f-80db811c064b" width="450" alt="TripleU MDM banner" />
</p>

# TripleU MDM

This repository contains the **public release** of TripleU MDM, including installation info and links to support and community discussions.

## Links

- **Installer (web):** https://mdm.tripleu.org  
- **Dashboard / console:** https://mdm.tripleu.org/login  
- **Feedback thread (JTech Forums):** https://forums.jtechforums.org/t/regarding-upcoming-tripleumdm-v4-0/5535?u=tripleu  
- **Israeli community Q&A (Mitmachim):** https://mitmachim.top/topic/87888  
- **Support / contact:** https://tripleu.org  
- **Donations:** https://tripleu.org  

## Contributing / feedback

Documentation improvements and guides are welcome — feel free to open a PR.

For bugs and feature requests, use GitHub Issues:  
https://github.com/TripleU613/TripleUMDM_Public/issues  
(You can also post in either community thread above.)

## Manual install (ADB)

If the web installer doesn’t work, you can set the device owner manually:

```bash
adb shell dpm set-device-owner "com.tripleu.mdm/.a"
adb shell pm grant com.tripleu.mdm android.permission.WRITE_SECURE_SETTINGS
````

## Usage

TripleU MDM is intended for **private use**.
Commercial use is available by request — contact us at [https://tripleu.org](https://tripleu.org) for pricing and discounts.


