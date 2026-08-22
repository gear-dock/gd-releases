# gd-releases

Firmware-Releases für GearDock: `manifest.json` (stable), `manifest-beta.json`
(beta) und die zugehörigen `.bin`-Dateien, ausgeliefert über GitHub Pages.
Die App liest das Manifest, prüft die Ed25519-Signatur je Target und spielt
die Firmware per `POST /api/ota` auf das Gerät — das Gerät prüft die Signatur
davor selbst noch einmal.

**Hier wird nicht von Hand editiert.** Jeder Inhalt entsteht durch
`tools/make_release.py release` im (privaten) Firmware-Repo `gd-firmware`;
das Konzept steht dort in `entwurf/OTA.md`.

Dieses Repo ist bewusst öffentlich: es enthält ausschließlich signierte
Artefakte und keinen Quellcode. Die Signatur — nicht die Herkunfts-URL — ist
das, was App und Gerät prüfen.
