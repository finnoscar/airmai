# 安装 Airmai

## TestFlight

1. 在 App Store 安装 Apple 的 TestFlight。
2. 在 iPhone 或 iPad 打开 Airmai 邀请链接。
3. 在 TestFlight 中接受邀请并安装 Airmai。

[打开 Airmai TestFlight](https://testflight.apple.com/join/GEN6DdpC)

可安装的版本和测试名额以 TestFlight 页面显示为准。支持的 Apple Watch 组件通过已配对 iPhone 的 TestFlight 应用管理。[Apple 安装说明](https://testflight.apple.com/join/GEN6DdpC)

## IPA

GitHub Releases 提供从当前应用工作区构建的 Release 安装包。文件名中的版本与构建号对应包内信息。

1. 打开发布页，下载 `.ipa` 和 `SHA256SUMS.txt`。
2. 使用自己的 Apple 签名与兼容的安装工具签名、安装。
3. 按签名工具及系统提示完成信任、开发者模式等步骤。

[下载 IPA](https://github.com/finnoscar/airmai/releases/latest)

IPA 采用未签名分发，需要自行签名才能安装。签名工具需要同时处理应用、扩展，以及包内的 Watch 组件。小组件、健康数据和成绩同步扩展等能力取决于签名后的权限与配置。

在 macOS 上可以核对下载文件的校验值。

```sh
shasum -a 256 -c SHA256SUMS.txt
```

首次安装前请保留现有数据。相同 Bundle ID 的不同安装方式可能覆盖原有应用，具体行为由签名与安装工具决定。

## 系统要求

| 设备 | 系统 |
| --- | --- |
| iPhone、iPhone Duo | iOS 16.0 或更新版本 |
| iPad | iPadOS 16.0 或更新版本 |
| Apple Watch | watchOS 10.0 或更新版本，配合已配对的 iPhone |

需要社区数据服务的功能，请先连接相应账号。心率记录需要 Apple Watch 和健康数据授权。
