# thingboot-iot · 芯步物联网生态

**中文** | [English](README_EN.md)

芯步（ThingBoot）是一个完整的物联网生态，覆盖从设备端、云平台到 Web 端与客户端的全链路。
除个别核心服务组件外，架构中的各部分都会全面开源。

本仓库是芯步生态的总览与导航入口：在这里了解整体架构，并快速跳转到各子项目仓库。

## 整体架构

```
UPPER LAYER	上层
══════════════════════════════════════════════════════════════════════════════
  APPS & MANAGEMENT                                DEVICES                    	管理与应用侧 / 设备侧
  ┌──────────────────────────┐                ┌──────────────────────────┐
  │ thingboot-web            │                │ thingboot-device         │  	芯步 Web 端（左）/ 芯步设备端（右）
  │  ├─ thingboot-web-java   │                │  ├─ esp-arduino-sdk      │
  │  └─ thingboot-web-php    │                │  └─ esp-idf-sdk          │
  ├──────────────────────────┤                └────────────┬─────────────┘
  │ thingboot-client         │                             │               	芯步客户端
  │  ├─ client-android       │                             │
  │  ├─ client-ios           │                             │
  │  ├─ client-uniapp        │                             │
  │  └─ client-flutter       │                             │
  └────────────┬─────────────┘                             │
               └────────────── MQTT / HTTPS ───────────────┘
CLOUD LAYER	底层
══════════════════════════════════════════════════════════════════════════════
                                                           ▼
  ┌──────────────────────────────────────────────────────────────────────────┐
  │ thingboot-cloud                                                          │	芯步云平台
  │  ├─ thingboot-cloud-center                                               │	云服务器核心（核心服务器）
  │  ├─ thingboot-cloud-node                                                 │	云服务器服务套件（物联网 Broker 服务器）
  │  └─ thingboot-cloud-api                                                  │	云服务器接口（接口服务器）
  └──────────────────────────────────────────────────────────────────────────┘
```

- **上层 · 管理与应用侧**：面向用户与运营者的 [thingboot-web](https://github.com/ThingBoot/thingboot-web)（芯步 Web 端）和 [thingboot-client](https://github.com/ThingBoot/thingboot-client)（芯步客户端）。
- **上层 · 设备侧**：运行在 ESP 系列芯片上的 [thingboot-device](https://github.com/ThingBoot/thingboot-device)（芯步设备端 SDK）。
- **底层 · 芯步云平台**：[thingboot-cloud](https://github.com/ThingBoot/thingboot-cloud)，为整个生态提供设备接入、消息路由与开放接口。

## 项目导航

### 导航仓库（上层入口）

| 仓库 | 说明 |
| --- | --- |
| [thingboot-web](https://github.com/ThingBoot/thingboot-web) | 芯步 Web 端：Web 管理控制台与开放平台的各语言实现 |
| [thingboot-client](https://github.com/ThingBoot/thingboot-client) | 芯步客户端：Android / iOS / uni-app 客户端 |
| [thingboot-device](https://github.com/ThingBoot/thingboot-device) | 芯步设备端：ESP 系列芯片的设备 SDK |
| [thingboot-cloud](https://github.com/ThingBoot/thingboot-cloud) | 芯步云平台：云服务器核心、服务套件与接口 |

### 芯步 Web 端

| 仓库 | 说明 |
| --- | --- |
| [thingboot-web-java](https://github.com/ThingBoot/thingboot-web-java) | 芯步 Web 端（Java 技术栈） |
| [thingboot-web-php](https://github.com/ThingBoot/thingboot-web-php) | 芯步 Web 端（PHP 技术栈） |

### 芯步客户端

| 仓库 | 说明 |
| --- | --- |
| [thingboot-client-android](https://github.com/ThingBoot/thingboot-client-android) | Android 原生客户端 |
| [thingboot-client-ios](https://github.com/ThingBoot/thingboot-client-ios) | iOS 原生客户端 |
| [thingboot-client-uniapp](https://github.com/ThingBoot/thingboot-client-uniapp) | uni-app 跨平台客户端，一套代码多端运行 |
| [thingboot-client-flutter](https://github.com/ThingBoot/thingboot-client-flutter) | Flutter 跨平台客户端 |

### 芯步云平台

| 仓库 | 说明 |
| --- | --- |
| [thingboot-cloud-center](https://github.com/ThingBoot/thingboot-cloud-center) | 云服务器核心，部署于核心服务器 |
| [thingboot-cloud-node](https://github.com/ThingBoot/thingboot-cloud-node) | 云服务器服务套件，部署于物联网 Broker 服务器：设备接入、消息路由、设备影子、OTA、对时、开放平台接口与 Web 管理界面合一的物联网中间件 |
| [thingboot-cloud-api](https://github.com/ThingBoot/thingboot-cloud-api) | 云服务器接口，部署于接口服务器 |

### 芯步设备端

| 仓库 | 说明 |
| --- | --- |
| [thingboot-device-esp-arduino-sdk](https://github.com/ThingBoot/thingboot-device-esp-arduino-sdk) | Arduino 框架设备 SDK，支持 ESP8266 / ESP32 / ESP32-S3 / ESP32-C6，内置 WiFi、以太网、4G Cat.1 与 WiFi Mesh 组网，开箱即用的平台直连与 OTA |
| [thingboot-device-esp-idf-sdk](https://github.com/ThingBoot/thingboot-device-esp-idf-sdk) | 上述 SDK 的 ESP-IDF 移植版，支持 ESP32 / ESP32-S3 / ESP32-C6 / ESP32-C3 |

## 开源说明

芯步生态以开源为核心：除个别核心服务组件外，架构中的各部分都会全面开源。
欢迎通过各子项目仓库的 Issues 与 Pull Requests 参与共建。
