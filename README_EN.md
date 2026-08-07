# thingboot-iot · ThingBoot IoT Ecosystem

[中文](README.md) | **English**

ThingBoot is an enterprise-grade IoT ecosystem and technical framework covering the full chain from devices and cloud platform to Web consoles and client apps.
Except for a few core service components, every part of the architecture is fully open source.

This repository is the overview and navigation hub of the ThingBoot ecosystem: learn the overall architecture here and jump quickly to each sub-project repository.

## Overall Architecture

```
            USER SIDE
┌─────────────────────────────┐
│ thingboot-web               │  ThingBoot Web
│  ├─ thingboot-web-java      │      Web (Java)
│  └─ thingboot-web-php       │      Web (PHP)
├─────────────────────────────┤
│ thingboot-client            │  ThingBoot Client
│  ├─ client-android          │      Native Android client
│  ├─ client-ios              │      Native iOS client
│  ├─ client-uniapp           │      uni-app framework client
│  └─ client-flutter          │      Flutter client
└─────────────┬───────────────┘

            CLOUD SIDE
┌─────────────────────────────┐
│ thingboot-cloud             │  ThingBoot Cloud Platform
│  ├─ thingboot-cloud-center  │  Cloud Core (core server)
│  ├─ thingboot-cloud-node    │  Cloud Service Suite (IoT broker server)
│  ├─ thingboot-cloud-api     │  Cloud API (for web & client)
│  └─ thingboot-cloud-open    │  Open Platform API (API server)
└─────────────┬───────────────┘

           DEVICE SIDE
┌─────────────────────────────┐
│ thingboot-device            │  ThingBoot Device Development
│  ├─ esp-arduino-sdk         │  ESP Arduino firmware SDK
│  ├─ esp-arduino-driver      │  ESP Arduino drivers
│  ├─ esp-idf-sdk             │  ESP-IDF firmware SDK
│  └─ esp-idf-sdk-driver      │  ESP-IDF drivers
└─────────────────────────────┘

```

- **USER side**: [thingboot-web](/ThingBoot/thingboot-web) (ThingBoot Web) and [thingboot-client](/ThingBoot/thingboot-client) (ThingBoot Client) for end users and operators.
- **CLOUD side**: [thingboot-cloud](/ThingBoot/thingboot-cloud), the ThingBoot Cloud Platform providing device access, message routing and open APIs for the whole ecosystem.
- **DEVICE side**: [thingboot-device](/ThingBoot/thingboot-device), firmware SDKs and drivers running on ESP (Espressif) chips.

## Project Navigation

### Navigation repositories (top-level entries)

| Repository | Description |
| --- | --- |
| [thingboot-web](/ThingBoot/thingboot-web) | ThingBoot Web: web console and open platform implementations in different languages |
| [thingboot-client](/ThingBoot/thingboot-client) | ThingBoot Client: Android / iOS / uni-app client apps |
| [thingboot-device](/ThingBoot/thingboot-device) | ThingBoot Device: firmware SDKs and drivers for ESP (Espressif) chips |
| [thingboot-cloud](/ThingBoot/thingboot-cloud) | ThingBoot Cloud: cloud core, service suite and API services |

### ThingBoot Web

| Repository | Description |
| --- | --- |
| [thingboot-web-java](/ThingBoot/thingboot-web-java) | ThingBoot Web (Java stack) |
| [thingboot-web-php](/ThingBoot/thingboot-web-php) | ThingBoot Web (PHP stack) |

### ThingBoot Client

| Repository | Description |
| --- | --- |
| [thingboot-client-android](/ThingBoot/thingboot-client-android) | Native Android client |
| [thingboot-client-ios](/ThingBoot/thingboot-client-ios) | Native iOS client |
| [thingboot-client-uniapp](/ThingBoot/thingboot-client-uniapp) | uni-app cross-platform client, one codebase for multiple platforms |
| [thingboot-client-flutter](/ThingBoot/thingboot-client-flutter) | Flutter cross-platform client |

### ThingBoot Cloud

| Repository | Description |
| --- | --- |
| [thingboot-cloud-center](/ThingBoot/thingboot-cloud-center) | Cloud core, deployed on the core server |
| [thingboot-cloud-node](/ThingBoot/thingboot-cloud-node) | Cloud service suite, deployed on IoT broker servers: an IoT middleware combining device access, message routing, device shadow, OTA, time sync, open platform APIs and a web admin UI |
| [thingboot-cloud-api](/ThingBoot/thingboot-cloud-api) | Cloud API, called by the web console and client apps |
| [thingboot-cloud-open](/ThingBoot/thingboot-cloud-open) | Open platform API, deployed on API servers |

### ThingBoot Device

| Repository | Description |
| --- | --- |
| [thingboot-device-esp-arduino-sdk](/ThingBoot/thingboot-device-esp-arduino-sdk) | ESP Arduino firmware SDK supporting ESP8266 / ESP32 / ESP32-S3 / ESP32-C6, with built-in WiFi, Ethernet, 4G Cat.1 and WiFi Mesh networking, out-of-the-box cloud connection and OTA |
| [thingboot-device-esp-arduino-drivers](/ThingBoot/thingboot-device-esp-arduino-drivers) | ESP Arduino drivers |
| [thingboot-device-esp-idf-sdk](/ThingBoot/thingboot-device-esp-idf-sdk) | ESP-IDF firmware SDK, a port of the Arduino SDK above, supporting ESP32 / ESP32-S3 / ESP32-C6 / ESP32-C3 |
| [thingboot-device-esp-idf-sdk-driver](/ThingBoot/thingboot-device-esp-idf-sdk-driver) | ESP-IDF drivers |

## Open Source

ThingBoot is open source at its core: except for a few core service components, every part of the architecture is fully open source.
Contributions via Issues and Pull Requests in each sub-project repository are welcome.
