# AA Phone Dongle

[Tiếng Việt](README_vi.md)

Turn a spare Android phone into a wireless Android Auto dongle for a car head unit that supports wired Android Auto.

The app is experimental; compatibility and automatic reconnection depend on your phones and head unit.

## How it works

```text
Main Android phone          Spare Android phone             Car head unit
Android Auto         <-->   AA Phone Dongle          <-->   Wired Android Auto
                   Bluetooth + Wi-Fi                  USB
```

The spare phone stays connected to the car's USB data port. Your main phone connects to it wirelessly and runs Android Auto, including navigation, music, and supported apps.

Bluetooth sets up the wireless connection and exchanges hotspot credentials. Wi-Fi carries Android Auto traffic, and the dongle forwards it over USB to the head unit.

Install AA Phone Dongle only on the **spare phone**. It does not add Android Auto to an unsupported head unit and does not support Apple CarPlay.

## Features

- Wireless Android Auto bridge using a spare Android phone.
- Bluetooth pairing and automatic exchange of Wi-Fi credentials.
- Connection status showing the connected phone's name when available and recent data transfer activity.
- Display of the current hotspot SSID, without a password or QR code.
- Optional startup when USB is connected.
- A **Stop dongle** button to end the session.
- English and Vietnamese interface, with the app version shown in the main title.

## Requirements

| Component | Requirement |
| --- | --- |
| Dongle phone | Android 11 or newer, Bluetooth, local Wi-Fi hotspot support, and USB accessory support |
| Main phone | Wireless Android Auto support, with Android Auto already configured |
| Car head unit | Working wired Android Auto and its USB data port |
| USB cable | A cable that supports data transfer |

Android 11 is the app's minimum installation version, not a guarantee of compatibility. Testing so far has included a Xiaomi sapphire dongle phone and a Pixel 8a main phone; this is not a broad compatibility certification.

## First-time setup

### 1. Prepare the phones

1. Install the AA Phone Dongle APK on the **spare phone**.
2. On the **main phone**, complete Android Auto setup and enable wireless Android Auto if that option is available.
3. Turn on Bluetooth and Wi-Fi on both phones.
4. Keep mobile data available on the main phone for online navigation and music. The dongle creates a local hotspot; it does not provide internet access.

**Disable Android Auto (Gearhead) on the dongle phone if your system allows it**, to avoid conflicts. Look under Android Settings → Apps → Android Auto → **Disable**. Menu names and availability vary by device. Closing the app's screen does not disable it.

**Keep Android Auto enabled on the main phone.** That phone runs the Android Auto session.

### 2. Grant permissions

1. Open AA Phone Dongle and its **Setup guide**.
2. Tap **Grant permissions** and allow the requested permissions. Depending on your Android version, these include nearby devices, Bluetooth, Wi-Fi/location, and notifications.
3. Allow background operation if your phone's battery settings restrict the app.

### 3. Connect the two phones over Bluetooth first — required

**The main phone must be paired and connected to the dongle phone over Bluetooth before continuing. Turning Bluetooth on is not enough, and pairing only with the car does not replace this step.**

1. Turn on Bluetooth on both phones. On the dongle phone, use **Pair Bluetooth** on the app's main screen and accept the visibility prompt.
2. On the **main phone**, open Android Bluetooth settings, search for devices, and select the **dongle phone's Bluetooth name**.
3. Confirm the pairing code on both phones. If they are already paired, select the dongle phone in the main phone's saved Bluetooth devices to connect again.
4. Complete the Bluetooth connection between the two phones before proceeding to the car connection below.
5. Return to the setup guide, choose whether to enable **Start automatically when USB is connected**, and tap **Finish and enable dongle**.

### 4. Connect to the car

1. Connect the dongle phone to the head unit's **wired Android Auto USB port** using a data cable.
2. If Android asks which app to open or requests USB accessory access, select AA Phone Dongle and allow access.
3. If the dongle is stopped, tap **Enable dongle**.
4. Accept any Android Auto setup prompts on the main phone or head unit.
5. Wait for Android Auto to appear on the head unit. The app shows **Connecting to [phone name]** when the name is available, and **Transferring data** while traffic is flowing.

You normally do not need to join the hotspot manually: its credentials are exchanged over Bluetooth. Android chooses the hotspot SSID, password, and band; the SSID may change between sessions.

## Everyday use

- With USB auto-start enabled, connect the dongle to the car and keep Bluetooth/Wi-Fi enabled on the main phone. Permissions and background execution must still be available.
- Tap **Stop dongle** to end the session, then **Enable dongle** to start again.
- If the head unit does not reconnect or the app asks you to reconnect USB, unplug and reconnect the cable. The app cannot force a physical USB reset.
- **Transferring data** indicates recent relay traffic; it does not by itself confirm that the head unit is displaying the session correctly.

## Current limitations

- **USB reconnection can be intermittent**, particularly after Stop/Start, unplugging/replugging the cable, or a slow initial handshake. Some head units may restart USB while the phones are still connecting.
- **USB recovery is limited:** the app can try to reopen a protocol session, but cannot force the head unit to detect a fresh physical USB connection. Manual cable reconnection may be necessary.
- **Hotspot settings are system-managed.** A fixed SSID or a specific Wi-Fi band cannot be guaranteed. Some ROMs restrict access to hotspot network information, which can prevent connection.
- **Abrupt disconnection can leave audio stuck or buzzing on some head units.** Shutdown handling has improved observed cases, but it is not verified across all head units or Android Auto force-stop scenarios.
- Only one active projection session is supported; seamless switching between multiple phones is not provided.
- Background restrictions, power supply, heat, and wireless conditions can affect stability. Long sessions and broad device compatibility still need testing.

## Troubleshooting

| Symptom | What to try |
| --- | --- |
| Head unit does not detect the dongle | Check that wired Android Auto works on that USB port, try another data cable, and approve USB accessory access. |
| Bluetooth is paired but projection does not start | Check Android Auto on the main phone, keep Bluetooth/Wi-Fi on, and confirm all dongle permissions are granted. If the issue persists, forget/unpair the two phones in Bluetooth settings on both devices, then pair and connect them again before retrying. |
| The phones connect but the head unit remains blank | Stop the dongle, unplug/reconnect USB, and enable it again. Report the issue if this repeats. |
| The head unit repeatedly reconnects during startup | Record the sequence and connection status. Startup/reconnection compatibility remains a known limitation. |
| Audio freezes or buzzes after disconnection | Tap **Stop dongle**. If the head unit stays stuck, unplug USB before starting a new session. |
| Auto-start does not work | Open the app, check the USB auto-start setting, permissions, and background restrictions, then reconnect USB. |

When reporting an issue, include both phone models and Android versions, the head unit model, app version/build type, and the exact steps that caused the problem. Mention whether Android Auto was force-stopped or USB was unplugged. Remove personal information and Wi-Fi credentials from any shared logs.

---

Made by @thucngv in Hanoi
