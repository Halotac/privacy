# Privacy Policy — HALOTAC

**Effective date:** May 6, 2026
**App name:** HALOTAC
**Bundle ID:** com.halotac.app
**Developer:** HALOTAC
**Contact:** halotac@icloud.com

---

## 1. Overview

HALOTAC is an offline-first, Bluetooth mesh tactical communication app designed for use with Heltec V4 LoRa radios. It does not require an account, does not connect to any cloud service, and does not transmit any data to the developer or any third party. All data you create in HALOTAC stays on your device.

---

## 2. Data We Do NOT Collect

We do not collect, store, transmit, or share any of the following:

- Personal identifiers (name, email address, phone number, user ID)
- Location data
- Bluetooth device identifiers or scan results
- Messages or communications
- Contacts or callsigns
- Medical card or supply inventory data
- Biometric data
- Usage analytics or crash reports
- Device identifiers (IDFA, IDFV, serial number)
- IP addresses or network information

There are no servers, no accounts, no analytics SDKs, and no advertising networks integrated into HALOTAC.

---

## 3. Data Stored Locally On Your Device

HALOTAC stores the following data **exclusively on your device**:

| Data | Purpose | Storage |
|---|---|---|
| Your callsign / display name | Shown in the app and broadcast over LoRa mesh | Encrypted local storage |
| Contact list (node names, callsigns, roles) | Identify other mesh nodes | Encrypted local storage |
| Chat messages | Conversation history with mesh nodes | Encrypted local storage |
| Check-in history | Operational status log | Encrypted local storage |
| Waypoints | Saved GPS coordinates | Encrypted local storage |
| Supply inventory | Personal gear tracking | Encrypted local storage |
| Medical card | Emergency reference | Encrypted local storage |
| Settings & preferences | App configuration | Encrypted local storage |
| Survival checklist state | Gear loadout tracking | Encrypted local storage |
| Last connected BLE device ID | Reconnection convenience | Plain local storage |

### Encryption

All sensitive data listed above (except the last BLE device ID) is encrypted at rest using **AES-256-GCM**. A unique 256-bit Data Encryption Key (DEK) is generated per install and stored in the iOS Keychain / Android Keystore using `AFTER_FIRST_UNLOCK_THIS_DEVICE_ONLY` access control. This key is never transmitted off the device.

---

## 4. Bluetooth (BLE)

HALOTAC uses Bluetooth Low Energy (BLE) to communicate with your Heltec V4 LoRa hardware device. The app:

- Scans for and connects to your own paired Heltec V4 device only
- Does **not** build profiles of nearby Bluetooth devices
- Does **not** share scan results with anyone
- Requires the **Bluetooth** permission solely to exchange messages with your hardware

Messages sent over the LoRa radio mesh are transmitted over radio frequency to other mesh nodes operated by people you choose to communicate with. HALOTAC does not intercept or store these radio transmissions on any server.

---

## 5. Location (GPS)

HALOTAC requests **foreground location** permission for the following features, **only when you explicitly trigger them**:

- **SOS Beacon** — attaches your GPS coordinates to an emergency alert you manually activate (hold-to-send, 1.5 s)
- **Check-in** — optionally attaches your GPS coordinates to an "I'm OK" broadcast you manually send
- **Waypoints** — records your current location when you create a waypoint
- **Position Map** — displays your position alongside mesh node positions on a local map

Location data is:
- Never sent to the developer or any server
- Only transmitted over the LoRa radio mesh to other nodes **when you choose to send it**
- Stored locally on your device only

The app does **not** track your location in the background.

---

## 6. Biometrics (Face ID / Touch ID)

If you enable the **Biometric Lock** feature in Settings, HALOTAC uses Face ID or Touch ID to authenticate you when opening the app. Biometric data is handled entirely by the iOS / Android operating system. HALOTAC never sees, stores, or transmits your biometric data.

---

## 7. Camera and Microphone

HALOTAC may request microphone access to record voice notes sent over the mesh. Voice note audio is:

- Processed locally on your device
- Transmitted as encoded audio over the LoRa radio mesh to other nodes only when you choose to send it
- Not stored on any server

HALOTAC does not use the camera.

---

## 8. Children's Privacy

HALOTAC is not directed at children under 13 (or under 16 in the European Economic Area). We do not knowingly collect any data from children.

---

## 9. Third-Party Services

HALOTAC does not integrate any third-party analytics, advertising, crash reporting, or social login services. The app is distributed via Apple TestFlight and the Apple App Store. Apple's own privacy practices apply to the distribution platform; see [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).

---

## 10. Data Retention and Deletion

All app data is stored locally on your device. You can delete it at any time:

- **Individual data:** Use the in-app "Reset" or "Clear" controls within each feature
- **All app data:** Go to **Profile → Settings → Reset All App Data**. This wipes all local data and destroys the encryption key, making any residual encrypted blobs permanently unrecoverable
- **Complete removal:** Uninstalling HALOTAC removes all app data from your device

We have no copies of your data and cannot assist with data recovery after deletion.

---

## 11. Security

- All sensitive local data is encrypted with AES-256-GCM before being written to storage
- The encryption key lives in the OS-managed secure enclave (iOS Keychain / Android Keystore)
- Network passphrases are stored in the Keychain/Keystore, not in plain storage
- The app fails closed on encryption errors — if encryption is unavailable on a native device, the write is dropped rather than stored in plaintext

---

## 12. Changes to This Policy

If we update this policy, we will revise the **Effective date** at the top and (where required) notify users through the app or App Store release notes. Continued use of the app after changes constitutes acceptance of the updated policy.

---

## 13. Contact

If you have questions or concerns about this privacy policy, please contact us at:

*(add your contact email or GitHub Issues link here)*

---

*This privacy policy was last updated on May 6, 2026.*
