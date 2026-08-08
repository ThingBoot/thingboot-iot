# thingboot-iot · ThingBoot IoT Ecosystem

[中文](README.md) | **English**

ThingBoot is an enterprise-grade IoT ecosystem and technical framework covering the full chain from devices and cloud platform to Web consoles and client apps.
Except for a few core service components, every part of the architecture is fully open source.

This repository is the overview and navigation hub of the ThingBoot ecosystem: learn the overall architecture here and jump quickly to each sub-project repository.

## Overall Architecture

```
                USER SIDE
┌───────────────────────────────────────────┐
│ thingboot-web                             │   ThingBoot Web
│  ├─ thingboot-web-java                    │       Web (Java)
│  └─ thingboot-web-php                     │       Web (PHP)
├───────────────────────────────────────────┤
│ thingboot-client                          │   ThingBoot Client
│  ├─ thingboot-client-android              │   Native Android client
│  ├─ thingboot-client-ios                  │       Native iOS client
│  ├─ thingboot-client-uniapp               │       uni-app framework client
│  └─ thingboot-client-flutter              │       Flutter client
└────────────────────┬──────────────────────┘

                CLOUD SIDE
┌───────────────────────────────────────────┐
│ thingboot-cloud                           │   ThingBoot Cloud Platform
│  ├─ thingboot-cloud-center                │   Cloud Core (IoT core service)
│  ├─ thingboot-cloud-node                  │   Cloud Node (IoT node service)
│  ├─ thingboot-cloud-api                   │   Cloud API (internal API)
│  └─ thingboot-cloud-open                  │   Open Platform (open platform API)
└─────────────────────┬─────────────────────┘

                DEVICE SIDE
┌───────────────────────────────────────────┐
│ thingboot-device                          │   ThingBoot Device Development
│  ├─ thingboot-device-esp-arduino-sdk      │   ThingBoot Device ESP-Arduino SDK
│  ├─ thingboot-device-esp-arduino-driver   │   ThingBoot Device ESP-Arduino drivers
│  ├─ thingboot-device-esp-idf-sdk          │   ThingBoot Device ESP-IDF SDK
│  └─ thingboot-device-esp-idf-sdk-driver   │   ThingBoot Device ESP-IDF drivers
└───────────────────────────────────────────┘

```

- **USER side**: [thingboot-web](https://github.com/ThingBoot/thingboot-web) (ThingBoot Web) and [thingboot-client](https://github.com/ThingBoot/thingboot-client) (ThingBoot Client) for end users and operators.
- **CLOUD side**: [thingboot-cloud](https://github.com/ThingBoot/thingboot-cloud), the ThingBoot Cloud Platform providing device access, message routing and open APIs for the whole ecosystem.
- **DEVICE SIDE**: [thingboot-device](https://github.com/ThingBoot/thingboot-device) (ThingBoot Device Development), firmware SDKs and drivers running on ESP chips.

## Project Navigation

### Navigation repositories (top-level entries)

| Repository | Description |
| --- | --- |
| [thingboot-web](https://github.com/ThingBoot/thingboot-web) | ThingBoot Web: Java and PHP implementations |
| [thingboot-client](https://github.com/ThingBoot/thingboot-client) | ThingBoot Client: native Android / iOS and uni-app / Flutter clients |
| [thingboot-device](https://github.com/ThingBoot/thingboot-device) | ThingBoot Device Development: firmware SDKs and drivers for ESP chips |
| [thingboot-cloud](https://github.com/ThingBoot/thingboot-cloud) | ThingBoot Cloud: cloud core, cloud node, cloud API and open platform |

### ThingBoot Web

| Repository | Description |
| --- | --- |
| [thingboot-web-java](https://github.com/ThingBoot/thingboot-web-java) | Web (Java) |
| [thingboot-web-php](https://github.com/ThingBoot/thingboot-web-php) | Web (PHP) |

### ThingBoot Client

| Repository | Description |
| --- | --- |
| [thingboot-client-android](https://github.com/ThingBoot/thingboot-client-android) | Native Android client |
| [thingboot-client-ios](https://github.com/ThingBoot/thingboot-client-ios) | Native iOS client |
| [thingboot-client-uniapp](https://github.com/ThingBoot/thingboot-client-uniapp) | uni-app framework client |
| [thingboot-client-flutter](https://github.com/ThingBoot/thingboot-client-flutter) | Flutter client |

### ThingBoot Cloud

| Repository | Description |
| --- | --- |
| [thingboot-cloud-center](https://github.com/ThingBoot/thingboot-cloud-center) | Cloud Core (IoT core service) |
| [thingboot-cloud-node](https://github.com/ThingBoot/thingboot-cloud-node) | Cloud Node (IoT node service): an IoT middleware combining device access, message routing, device shadow, OTA, time sync, open platform APIs and a web admin UI |
| [thingboot-cloud-api](https://github.com/ThingBoot/thingboot-cloud-api) | Cloud API (internal API, called by the web console and client apps) |
| [thingboot-cloud-open](https://github.com/ThingBoot/thingboot-cloud-open) | Open Platform (open platform API) |

### ThingBoot Device Development

| Repository | Description |
| --- | --- |
| [thingboot-device-esp-arduino-sdk](https://github.com/ThingBoot/thingboot-device-esp-arduino-sdk) | ThingBoot Device ESP-Arduino SDK, supporting ESP8266 / ESP32 / ESP32-S3 / ESP32-C6, with built-in WiFi, Ethernet, 4G Cat.1 and WiFi Mesh networking, out-of-the-box cloud connection and OTA |
| [thingboot-device-esp-arduino-drivers](https://github.com/ThingBoot/thingboot-device-esp-arduino-drivers) | ThingBoot Device ESP-Arduino drivers |
| [thingboot-device-esp-idf-sdk](https://github.com/ThingBoot/thingboot-device-esp-idf-sdk) | ThingBoot Device ESP-IDF SDK, a port of the Arduino SDK above, supporting ESP32 / ESP32-S3 / ESP32-C6 / ESP32-C3 |
| [thingboot-device-esp-idf-driver](https://github.com/ThingBoot/thingboot-device-esp-idf-drivers) | ThingBoot Device ESP-IDF drivers |

## Open Source

ThingBoot is open source at its core: except for a few core service components, every part of the architecture is fully open source.
Contributions via Issues and Pull Requests in each sub-project repository are welcome.
