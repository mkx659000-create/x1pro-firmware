# X1PRO firmware

Public distribution of signed firmware binaries for X1PRO. This repository contains release metadata and firmware assets; the application source is maintained separately.

## Compatibility

The current pilot channel targets X1PRO board_v4 with ESP32-S3, 8 MB flash and the ota-ble-control profile. Use only on compatible machines already configured for this signed OTA profile.

## Updates

The X1PRO Chrome extension reads [channel.json](./channel.json), downloads and verifies the signed firmware, then transfers it to the machine through its existing local Wi-Fi update interface. The computer needs internet to download the image. During installation it must reach the machine on the same local network or through the X1PRO hotspot. The machine itself does not need internet access.

End the scan and stop X1PRO before updating. Keep the machine powered through upload and restart. The extension reports success only after checking the running version, partition, image digest and machine health. If the result is unconfirmed, reconnect and check the result before attempting another update.

The signed application image can also be installed from the machine's firmware-update page. Release binaries are OTA application images, not full-flash serial images. SHA-256 values are published with each release.

## Pilot channel

The initial channel is a prerelease used to verify the browser-assisted update flow. See the release notes for acceptance status and changes.
