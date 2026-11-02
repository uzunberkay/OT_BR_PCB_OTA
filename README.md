# OT_BR_PCB_OTA

[OT_BR_PCB](https://github.com/uzunberkay/OT_BR_PCB) (ESP32-C3 + ESP32-H2 RCP
border router) firmware'i icin OTA dagitim reposu. Dosyalar GitHub Pages ile
yayinlanir.

| Dosya | Adres |
| --- | --- |
| Metadata | `https://uzunberkay.github.io/OT_BR_PCB_OTA/ota/esp32c3/prod/metadata.json` |
| Firmware | `https://uzunberkay.github.io/OT_BR_PCB_OTA/ota/esp32c3/prod/firmware.bin` |

`ota/esp32c3/prod/` icerigi elle duzenlenmez. OT_BR_PCB reposunun `master`
dalina yapilan push'ta CI (`ota-publish` job'u) `scripts/release.py` ile
`firmware.bin` ve `metadata.json` dosyalarini gunceller.

Metadata formati:

```json
{
  "version": "X.Y.Z",
  "url": "https://uzunberkay.github.io/OT_BR_PCB_OTA/ota/esp32c3/prod/firmware.bin",
  "sha256": "<esptool image-info Validation hash>"
}
```

Cihazlar yalnizca `version` mevcut surumden buyukse guncellenir.
