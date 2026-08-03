# thingboot-iot · ThingBoot IoT Ecosystem

[中文](README.md) | **English**

ThingBoot is a complete IoT ecosystem covering the full chain from devices and cloud platform to Web consoles and client apps.
Except for a few core service components, every part of the architecture is fully open source.

This repository is the overview and navigation hub of the ThingBoot ecosystem: learn the overall architecture here and jump quickly to each sub-project repository.

## Overall Architecture

```
┌──────────────────────────────── Upper Layer ─────────────────────────────────┐
│                                                                              │
│   Apps & Management               Devices                                    │
│  ┌──────────────────────────┐                ┌──────────────────────────┐    │
│  │ thingboot-web            │                │ thingboot-device         │    │
│  │ ThingBoot Web            │                │ Device SDKs              │    │
│  │  ├─ thingboot-web-java   │                │  ├─ esp-arduino-sdk      │    │
│  │  └─ thingboot-web-php    │                │  └─ esp-idf-sdk          │    │
│  ├──────────────────────────┤                └────────────┬─────────────┘    │
│  │ thingboot-client         │                             │                  │
│  │ Client Apps              │                             │                  │
│  │  ├─ client-android       │                             │                  │
│  │  ├─ client-ios           │                             │                  │
│  │  └─ client-uniapp        │                             │                  │
│  └────────────┬─────────────┘                             │                  │
└───────────────┼───────────────────────────────────────────┼──────────────────┘
                │               MQTT / HTTPS                │
┌───────────────▼───────────────────────────────────────────▼──────────────────┐
│                        Cloud Layer / ThingBoot Cloud                         │
│                                                                              │
│   thingboot-cloud ThingBoot Cloud Platform                                   │
│   ├─ thingboot-cloud-center Cloud Core (core server)                         │
│   ├─ thingboot-cloud-node   Cloud Service Suite (IoT broker server)          │
│   └─ thingboot-cloud-api    Cloud API (API server)                           │
└──────────────────────────────────────────────────────────────────────────────┘
```

- **Upper layer · Apps & Management**: [thingboot-web](https://github.com/ThingBoot/thingboot-web) (Web console) and [thingboot-client](https://github.com/ThingBoot/thingboot-client) (client apps) for end users and operators.
- **Upper layer · Devices**: [thingboot-device](https://github.com/ThingBoot/thingboot-device), the device SDKs running on ESP-series chips.
- **Cloud layer**: [thingboot-cloud](https://github.com/ThingBoot/thingboot-cloud), the ThingBoot Cloud Platform providing device access, message routing and open APIs for the whole ecosystem.

## Project Navigation

### Navigation repositories (top-level entries)

| Repository | Description |
| --- | --- |
| [thingboot-web](https://github.com/ThingBoot/thingboot-web) | ThingBoot Web: web console and open platform implementations in different languages |
| [thingboot-client](https://github.com/ThingBoot/thingboot-client) | ThingBoot Client: Android / iOS / uni-app client apps |
| [thingboot-device](https://github.com/ThingBoot/thingboot-device) | ThingBoot Device: device SDKs for ESP-series chips |
| [thingboot-cloud](https://github.com/ThingBoot/thingboot-cloud) | ThingBoot Cloud: cloud core, service suite and API services |

### ThingBoot Web

| Repository | Description |
| --- | --- |
| [thingboot-web-java](https://github.com/ThingBoot/thingboot-web-java) | ThingBoot Web (Java stack) |
| [thingboot-web-php](https://github.com/ThingBoot/thingboot-web-php) | ThingBoot Web (PHP stack) |

### ThingBoot Client

| Repository | Description |
| --- | --- |
| [thingboot-client-android](https://github.com/ThingBoot/thingboot-client-android) | Native Android client |
| [thingboot-client-ios](https://github.com/ThingBoot/thingboot-client-ios) | Native iOS client |
| [thingboot-client-uniapp](https://github.com/ThingBoot/thingboot-client-uniapp) | uni-app cross-platform client, one codebase for multiple platforms |

### ThingBoot Cloud

| Repository | Description |
| --- | --- |
| [thingboot-cloud-center](https://github.com/ThingBoot/thingboot-cloud-center) | Cloud core, deployed on the core server |
| [thingboot-cloud-node](https://github.com/ThingBoot/thingboot-cloud-node) | Cloud service suite, deployed on IoT broker servers: an IoT middleware combining device access, message routing, device shadow, OTA, time sync, open platform APIs and a web admin UI |
| [thingboot-cloud-api](https://github.com/ThingBoot/thingboot-cloud-api) | Cloud API services, deployed on API servers |

### ThingBoot Device

| Repository | Description |
| --- | --- |
| [thingboot-device-esp-arduino-sdk](https://github.com/ThingBoot/thingboot-device-esp-arduino-sdk) | Arduino-framework device SDK supporting ESP8266 / ESP32 / ESP32-S3 / ESP32-C6, with built-in WiFi, Ethernet, 4G Cat.1 and WiFi Mesh networking, out-of-the-box cloud connection and OTA |
| [thingboot-device-esp-idf-sdk](https://github.com/ThingBoot/thingboot-device-esp-idf-sdk) | ESP-IDF port of the SDK above, supporting ESP32 / ESP32-S3 / ESP32-C6 / ESP32-C3 |

## Open Source

ThingBoot is open source at its core: except for a few core service components, every part of the architecture is fully open source.
Contributions via Issues and Pull Requests in each sub-project repository are welcome.
