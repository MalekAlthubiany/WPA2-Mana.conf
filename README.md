# Hostapd-MANA Configuration for Rogue Access Point Attacks

This repository contains a customized configuration file for `hostapd-mana`, designed to facilitate rogue access point (AP) attacks. By using this configuration, you can set up a fake Wi-Fi access point to capture client credentials and perform advanced man-in-the-middle (MitM) attacks. 

## Features
- Mimics the target SSID for phishing or credential harvesting.
- Supports WPA/WPA2 Enterprise attacks.
- Includes MANA Wireless Pwnage Edition (WPE) features for EAP credential capture.
- Supports logging of captured credentials and MitM operations.
- Configurable authentication settings, including CCMP and TKIP encryption.

## Usage
1. **Edit the SSID**:
   Modify the `ssid` parameter in the configuration file to match your target's SSID.
   ```plaintext
   ssid=YourTargetSSID
   ```

2. **Start the Rogue AP**:
   Use `hostapd-mana` with the configuration file:
   ```bash
   sudo hostapd /etc/hostapd-mana/hostapd-mana.conf
   ```

3. **Capture Credentials**:
   Monitor the output or check the configured logs for captured credentials.

## Requirements
- A Linux system with `hostapd-mana` installed.
- A compatible wireless interface card (supports AP mode).
- Certificates for WPA Enterprise (configured in the file).

## Disclaimer
This repository is intended for educational purposes and security research only. Unauthorized use of this configuration in real-world scenarios is prohibited and may be illegal. Always obtain proper authorization before testing any system.

---
