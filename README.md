# Kirinuki — releases

This repository only hosts the **Kirinuki** Windows installer and its signed update files. There is no source code here.

## Install
1. Open the **latest release** and download `Kirinuki_<version>_x64-setup.exe`.
2. Check the file's fingerprint against the one you were sent **through a different app** (for example a text message). In PowerShell:
   ```powershell
   Get-FileHash .\Kirinuki_<version>_x64-setup.exe -Algorithm SHA256
   ```
   If the two values differ, do not run it.
3. Run the installer. It installs just for you and needs no admin rights. The app isn't code-signed yet, so Windows may say "Windows protected your PC"; click **More info → Run anyway**.
4. The first-run setup wizard installs everything else Kirinuki needs.

## Updates
Kirinuki checks this repository for new versions and installs them for you after you confirm. Every update is signed, and the app refuses anything not signed with the Kirinuki update key (key ID `BE0D2A41BBB3D592`). Published releases in this repository are locked and cannot be modified.

## Licenses
Kirinuki runs FFmpeg (GPL) as a separate program. Each release that includes FFmpeg links the matching FFmpeg source. Other third-party notices ship inside the app (About → Licenses).

## Safety
Only install Kirinuki from this page. Never disable your antivirus or SmartScreen to install it, and never share your API keys with anyone, including the app's authors.
