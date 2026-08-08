# thingboot-iot · 芯步物联网生态

**中文** | [English](README_EN.md)

芯步（ThingBoot）是一个企业级的物联网生态与技术框架，覆盖从设备端、云平台到 Web 端与客户端的全链路。
除个别核心服务组件外，架构中的各部分都会全面开源。

本仓库是芯步生态的总览与导航入口：在这里了解整体架构，并快速跳转到各子项目仓库。

## 整体架构

```
                USER 用户侧
┌───────────────────────────────────────────┐
│ thingboot-web                             │   芯步Web端
│  ├─ thingboot-web-java                    │       Java语言Web端
│  └─ thingboot-web-php                     │       PHP语言Web端
├───────────────────────────────────────────┤
│ thingboot-client                          │   芯步客户端
│  ├─ thingboot-client-android              │       安卓原生客户端
│  ├─ thingboot-client-ios                  │       iOS原生客户端
│  ├─ thingboot-client-uniapp               │       Uniapp框架客户端
│  └─ thingboot-client-flutter              │       Flutter语言客户端
└────────────────────┬──────────────────────┘

                CLOUD 平台侧
┌───────────────────────────────────────────┐
│ thingboot-cloud                           │   芯步云平台
│  ├─ thingboot-cloud-center                │       云平台核心（物联网核心服务）
│  ├─ thingboot-cloud-node                  │       云平台节点（物联网节点服务）
│  ├─ thingboot-cloud-api                   │       云平台接口（内部接口）
│  └─ thingboot-cloud-open                  │       开放平台（开放平台接口）
└─────────────────────┬─────────────────────┘

                DEVICE 设备侧
┌───────────────────────────────────────────┐
│ thingboot-device                          │   芯步设备开发
│  ├─ thingboot-device-esp-arduino-sdk      │       芯步设备ESP-Arduino-SDK
│  ├─ thingboot-device-esp-arduino-driver   │       芯步设备ESP-Arduino-驱动
│  ├─ thingboot-device-esp-idf-sdk          │       芯步设备ESP-IDF-SDK
│  └─ thingboot-device-esp-idf-sdk-driver   │       芯步设备ESP-IDF-驱动
└───────────────────────────────────────────┘
```

- **用户侧 USER**：面向用户与运营者的 [thingboot-web](https://github.com/ThingBoot/thingboot-web)（芯步 Web 端）和 [thingboot-client](https://github.com/ThingBoot/thingboot-client)（芯步客户端）。
- **平台侧 CLOUD**：[thingboot-cloud](https://github.com/ThingBoot/thingboot-cloud)（芯步云平台），为整个生态提供设备接入、消息路由与开放接口。
- **设备侧 DEVICE**：[thingboot-device](https://github.com/ThingBoot/thingboot-device)（芯步设备开发），运行在 ESP 系列芯片上的固件 SDK 与驱动。

## 项目导航

### 导航仓库（生态入口）

| 仓库 | 说明 |
| --- | --- |
| [thingboot-web](https://github.com/ThingBoot/thingboot-web) | 芯步 Web 端：Java 与 PHP 两种语言实现 |
| [thingboot-client](https://github.com/ThingBoot/thingboot-client) | 芯步客户端：安卓 / iOS 原生及 Uniapp / Flutter 框架客户端 |
| [thingboot-device](https://github.com/ThingBoot/thingboot-device) | 芯步设备开发：ESP 系列芯片的固件 SDK 与驱动 |
| [thingboot-cloud](https://github.com/ThingBoot/thingboot-cloud) | 芯步云平台：云平台核心、云平台节点、云平台接口与开放平台 |

### 芯步 Web 端

| 仓库 | 说明 |
| --- | --- |
| [thingboot-web-java](https://github.com/ThingBoot/thingboot-web-java) | Java 语言 Web 端 |
| [thingboot-web-php](https://github.com/ThingBoot/thingboot-web-php) | PHP 语言 Web 端 |

### 芯步客户端

| 仓库 | 说明 |
| --- | --- |
| [thingboot-client-android](https://github.com/ThingBoot/thingboot-client-android) | 安卓原生客户端 |
| [thingboot-client-ios](https://github.com/ThingBoot/thingboot-client-ios) | iOS 原生客户端 |
| [thingboot-client-uniapp](https://github.com/ThingBoot/thingboot-client-uniapp) | Uniapp 框架客户端 |
| [thingboot-client-flutter](https://github.com/ThingBoot/thingboot-client-flutter) | Flutter 语言客户端 |

### 芯步云平台

| 仓库 | 说明 |
| --- | --- |
| [thingboot-cloud-center](https://github.com/ThingBoot/thingboot-cloud-center) | 云平台核心（物联网核心服务） |
| [thingboot-cloud-node](https://github.com/ThingBoot/thingboot-cloud-node) | 云平台节点（物联网节点服务）：设备接入、消息路由、设备影子、OTA、对时、开放平台接口与 Web 管理界面合一的物联网中间件 |
| [thingboot-cloud-api](https://github.com/ThingBoot/thingboot-cloud-api) | 云平台接口（内部接口，供 Web 端和客户端调用） |
| [thingboot-cloud-open](https://github.com/ThingBoot/thingboot-cloud-open) | 开放平台（开放平台接口） |

### 芯步设备开发

| 仓库 | 说明 |
| --- | --- |
| [thingboot-device-esp-arduino-sdk](https://github.com/ThingBoot/thingboot-device-esp-arduino-sdk) | 芯步设备 ESP-Arduino SDK，支持 ESP8266 / ESP32 / ESP32-S3 / ESP32-C6，内置 WiFi、以太网、4G Cat.1 与 WiFi Mesh 组网，开箱即用的平台直连与 OTA |
| [thingboot-device-esp-arduino-drivers](https://github.com/ThingBoot/thingboot-device-esp-arduino-drivers) | 芯步设备 ESP-Arduino 驱动 |
| [thingboot-device-esp-idf-sdk](https://github.com/ThingBoot/thingboot-device-esp-idf-sdk) | 芯步设备 ESP-IDF SDK，Arduino 版 SDK 的 ESP-IDF 移植版，支持 ESP32 / ESP32-S3 / ESP32-C6 / ESP32-C3 |
| [thingboot-device-esp-idf-driver](https://github.com/ThingBoot/thingboot-device-esp-idf-drivers) | 芯步设备 ESP-IDF 驱动 |

## 开源说明

芯步生态以开源为核心：除个别核心服务组件外，架构中的各部分都会全面开源。
欢迎通过各子项目仓库的 Issues 与 Pull Requests 参与共建。
