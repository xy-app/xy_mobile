# 📱 移动端与模拟器自动化套件 (Mobile & Emulator Suite)

[![Plugin Version](https://img.shields.io/badge/version-0.50.5-blue.svg)](manifest.json)
[![Group](https://img.shields.io/badge/group-Mobile-green.svg)](#)
[![Platforms](https://img.shields.io/badge/platform-Android%20%7C%20iOS-brightgreen.svg)](#)
[![License](https://img.shields.io/badge/license-Freeware-brightgreen.svg)](#)

官方高性能原生移动端与多引擎模拟器自动化套件。专为 Android 物理真机、主流安卓模拟器（网易 MuMu、雷电、夜神、逍遥、Google AVD）以及 Apple iOS 模拟器设计。开箱即用，提供设备自愈排障、极速截图、手势仿真、应用生命周期管理、端口映射与隐私权限自动授予等全套自动化能力。

---

## 📖 简介 (Overview)

`xy_mobile` 提供移动端原生跨平台控制能力：
- **多引擎全景兼容**：开箱即用支持 Android 真实设备、Google 官方 AVD 模拟器，并自动适配主流桌面模拟器常用端口（MuMu 16384/7555、雷电 5555/5557、夜神 62001、逍遥 21503 等）。
- **iOS 模拟器原生支持**：支持唤醒/休眠模拟器（`SimctlBoot`/`SimctlShutdown`）、URL Scheme 深层调起（`SimctlOpenUrl`）、相册资源注入（`SimctlAddMedia`）及自动化授予系统相机/相册/定位隐私权限（`SimctlPermission`）。
- **全链路触控与手势**：像素级点击与连击（`MobileTap`）、带时长平滑滚动手势与拖拽（`MobileSwipe`）、字符转义文本键入（`MobileInput`）与系统物理按键广播（`AdbKey`）。
- **极速画面捕获**：提供高帧率截屏（`MobileScreenCap`），支持输出 Base64 变量或直接落盘，无缝串联下游机器视觉与 OCR 算子。
- **设备调试与自愈防护**：支持设备终端指令执行（`AdbShell`）、双向文件传输（`AdbPush`/`AdbPull`）、本地与设备 TCP 端口映射（`AdbForward`），以及重置服务连接与脱机自愈（`AdbRestartServer`）。

---

## ✨ 核心特性 (Features)

- **高性能原生直连**：开箱即用，执行效率高，响应迅速。
- **智能模拟器自愈探测**：内置已知模拟器端口健康巡检机制，连接异常或设备脱机时支持一键守护自愈。
- **统一双端跨平台抽象**：点击、滑动、输入、截屏与 App 管理在 Android 与 iOS 模拟器间保持一致的字段定义。
- **全生命周期 App 管理**：支持安装包部署与卸载、冷启动强制杀后台（`stop_first`）及第三方应用过滤清单提取。
- **iOS 自动化权限辅助**：免手动确认系统授权弹框，直接静默下发授予相机、相册、地理位置与通知等隐私权限。

---

## 🛠️ 动作指令全景速查 (Action Catalog)

| 动作标识 (Tag) | 功能名称 | 平台 | 描述 | 输出类型 |
| :--- | :--- | :--- | :--- | :--- |
| `MobileDevices` | 获取移动设备与模拟器列表 | Android / iOS | 自动扫描并列出真机、桌面模拟器端口及 iOS 模拟器 | `string` |
| `MobileTap` | 屏幕点击 | Android / iOS | 绝对坐标单次/多次点击触控 | `string` |
| `MobileSwipe` | 滑动与拖拽 | Android / iOS | 坐标手势滑动与长按拖拽，支持上下翻页与左右滑动 | `string` |
| `MobileInput` | 文本输入 | Android / iOS | 向聚焦输入框键入文本，支持特殊字符转义与清空旧文本 | `string` |
| `MobileScreenCap` | 屏幕截图 | Android / iOS | 极速捕获当前设备屏幕画面，输出 Base64 变量或直接写盘 | `string` |
| `MobileStartApp` | 启动应用 | Android / iOS | 根据 Package Name 或 Bundle ID 启动应用，支持先杀后台 | `string` |
| `MobileStopApp` | 停止应用 | Android / iOS | 强制终止正在运行的移动应用程序进程 | `string` |
| `MobileInstall` | 安装应用 | Android / iOS | 向设备安装本地 APK 或 iOS .app 应用包 | `string` |
| `MobileUninstall` | 卸载应用 | Android / iOS | 彻底移除指定包名对应的应用及数据 | `string` |
| `MobilePackages` | 获取已安装应用清单 | Android | 查询已安装应用包名列表，支持仅保留第三方应用过滤 | `string` |
| `AdbShell` | 执行 Shell 指令 | Android | 在设备中执行命令并捕获回显输出 | `string` |
| `AdbKey` | 发送系统按键 | Android | 发送物理/虚拟按键（返回、桌面主屏、多任务列表、电源等） | `string` |
| `AdbPush` | 推送文件到设备 | Android | 将本地文件/文件夹上传至设备存储目录 | `string` |
| `AdbPull` | 从设备拉取文件 | Android | 从设备内部存储将指定文件/日志拉取下载到本地 | `string` |
| `AdbForward` | 端口映射转发 | Android | 在宿主机端口与设备/模拟器端口间建立 TCP 数据传输管道 | `string` |
| `AdbConnect` | 网络调试连接 | Android | 通过 IP:Port 建立 TCP/IP 调试连接（支持各大模拟器多开） | `string` |
| `AdbRestartServer` | 重启服务与自愈 | Android | 重启本地连接服务，解决端口冲突与设备脱机问题 | `string` |
| `SimctlBoot` | 唤醒 iOS 模拟器 | iOS | 启动并唤醒指定的 Apple iOS 模拟器实例 | `string` |
| `SimctlShutdown` | 关闭 iOS 模拟器 | iOS | 关闭并休眠运行中的 iOS 模拟器 | `string` |
| `SimctlOpenUrl` | 调起 URL Scheme / 网页 | iOS | 在 iOS 模拟器中通过 Safari 打开网址或调起应用深度链接 | `string` |
| `SimctlPermission` | 自动授予隐私权限 | iOS | 自动授予或撤销目标 App 相机/相册/定位等隐私权限 | `string` |
| `SimctlAddMedia` | 相册注入媒体 | iOS | 将本地图片/视频直接注入到 iOS 模拟器系统相册中 | `string` |

---

## 📚 详细参数说明与使用参考 (Detailed Reference)

### 1. 设备发现与环境自愈 (Device Discovery & Health)

#### `MobileDevices` - 获取设备列表
- **输入参数：**
  | 参数名 (Field) | 显示名称 | 类型 | 默认值 | 预设推荐值 | 说明 |
  | :--- | :--- | :--- | :--- | :--- | :--- |
  | `auto_connect` | 自动扫描并连接模拟器端口 | `boolean` | `true` | `true`, `false` | 自动探测 MuMu (16384)、雷电 (5555)、夜神 (62001) 等端口 |
  | `output_alias` | 输出变量名 | `string` | `mobile_devices` | `mobile_devices` | 存储设备信息 JSON 数组的变量名 |
- **输出类型：** `string`（设备 JSON 数组）

#### `AdbRestartServer` - 重启服务与自愈
- **输入参数：**
  | 参数名 (Field) | 显示名称 | 类型 | 默认值 | 预设推荐值 | 说明 |
  | :--- | :--- | :--- | :--- | :--- | :--- |
  | `diagnose_device` | 重启后诊断设备 | `string` | `auto` | `auto`, `127.0.0.1:16384` | 重启完成后自动验证其连接状态与授权情况 |
- **输出类型：** `string`

#### `AdbConnect` - 网络调试连接
- **输入参数：**
  | 参数名 (Field) | 显示名称 | 类型 | 默认值 | 预设推荐值 | 说明 |
  | :--- | :--- | :--- | :--- | :--- | :--- |
  | `address` | 网络地址与端口 | `string` | `127.0.0.1:16384` | `127.0.0.1:16384` (MuMu 12)<br>`127.0.0.1:5555` (雷电)<br>`127.0.0.1:62001` (夜神)<br>`127.0.0.1:21503` (逍遥) | 目标 `IP:Port` 组合字符串 |
- **输出类型：** `string`

---

### 2. 屏幕手势与交互控制 (Screen Gestures & Interaction)

#### `MobileTap` - 屏幕点击
- **输入参数：**
  | 参数名 (Field) | 显示名称 | 类型 | 默认值 | 预设推荐值 | 说明 |
  | :--- | :--- | :--- | :--- | :--- | :--- |
  | `device` | 目标设备 | `string` | `auto` | `auto`, `127.0.0.1:16384`, `booted` | 设备序列号；`auto` 为首选活跃设备，`booted` 为 iOS 已启动实例 |
  | `xy` | 点击坐标 (X, Y) | `string` | `500, 500` | `500, 500`, `540, 960` | 屏幕像素物理绝对坐标 |
  | `count` | 点击次数 | `number` | `1` | `1` (单击), `2` (双击) | 连续点击次数 |
- **输出类型：** `string`

#### `MobileSwipe` - 滑动与拖拽
- **输入参数：**
  | 参数名 (Field) | 显示名称 | 类型 | 默认值 | 预设推荐值 | 说明 |
  | :--- | :--- | :--- | :--- | :--- | :--- |
  | `device` | 目标设备 | `string` | `auto` | `auto`, `booted` | 目标设备标识 |
  | `from_xy` | 起始坐标 (X1, Y1) | `string` | `500, 800` | `500, 800` (上滑起点), `500, 200` (下滑起点) | 滑动起始像素点 |
  | `to_xy` | 终止坐标 (X2, Y2) | `string` | `500, 200` | `500, 200` (上滑终点), `500, 800` (下滑终点) | 滑动结束像素点 |
  | `duration_ms` | 滑动耗时 (毫秒) | `number` | `300` | `200`, `300`, `500`, `1000` | 耗时越长手势越缓慢平滑 |
- **输出类型：** `string`

#### `MobileInput` - 文本输入
- **输入参数：**
  | 参数名 (Field) | 显示名称 | 类型 | 默认值 | 说明 |
  | :--- | :--- | :--- | :--- | :--- |
  | `device` | 目标设备 | `string` | `auto` | 设备序列号标识 |
  | `text` | 输入文本 | `string` | `""` | 待键入文本内容（支持多语言与符号） |
  | `clear_before` | 输入前清空已有文本 | `boolean` | `false` | 是否在键入前自动退格清空已有文本 |
- **输出类型：** `string`

#### `MobileScreenCap` - 屏幕截图
- **输入参数：**
  | 参数名 (Field) | 显示名称 | 类型 | 默认值 | 说明 |
  | :--- | :--- | :--- | :--- | :--- |
  | `device` | 目标设备 | `string` | `auto` | 设备序列号标识 |
  | `save_path` | 本地保存路径 | `FilePicker` | `""` | 图片本地保存路径（如 `screenshot.png`），留空仅输出变量 |
  | `output_alias` | 输出变量名 | `string` | `screen_image` | 接收 Base64 图片数据的上下文变量名 |
- **输出类型：** `string`

---

### 3. 应用管理与生命周期 (Application Management)

#### `MobileStartApp` 与 `MobileStopApp`
- **`MobileStartApp`**：
  - `device`: 设备序列号标识（默认 `auto`）。
  - `package_name`: Android Package Name（如 `com.tencent.mm`）或 iOS Bundle ID（如 `com.apple.Preferences`）。
  - `activity`: (仅 Android 可选) 页面组件类名（如 `.MainActivity`），留空由默认入口启动。
  - `stop_first`: 启动前是否先强杀后台保证冷启动（默认 `false`）。
- **`MobileStopApp`**：强制结束指定包名进程。参数：`device`、`package_name`。

#### `MobileInstall` 与 `MobileUninstall`
- **`MobileInstall`**：向设备安装应用。参数：`device`、`app_path`（本地 `.apk` 或 iOS 模拟器 `.app` 路径）。
- **`MobileUninstall`**：指定 `package_name` 彻底移除应用。参数：`device`、`package_name`。

#### `MobilePackages` - 查询已安装应用
- **输入参数：**
  - `device`: 目标设备标识（默认 `auto`）。
  - `third_party_only`: 是否过滤系统内置应用，仅展示第三方应用（默认 `true`）。
  - `output_alias`: 结果写入变量名（默认 `installed_packages`）。

---

### 4. 设备调试与传输能力 (Device Bridge & Debugging)

- **`AdbShell`**：执行设备终端命令（如 `getprop ro.build.version.release`、`wm size`、`dumpsys battery`），回显写入指定变量。参数：`device`、`command`、`output_alias`。
- **`AdbKey`**：发送常用系统按键（`BACK`, `HOME`, `APP_SWITCH`, `POWER`, `VOLUME_UP`, `VOLUME_DOWN`, `ENTER`, `DEL`）。参数：`device`、`key_code`。
- **`AdbPush` 与 `AdbPull`**：实现宿主机与设备存储目录（如 `/sdcard/Download/`）之间的双向文件传输。
- **`AdbForward`**：在宿主机与设备间建立端口转发隧道（如 `tcp:8080` -> `tcp:8080`）。参数：`device`、`local_port`、`remote_port`。

---

### 5. iOS 模拟器自动化能力 (iOS Simulator Features)

- **`SimctlBoot` / `SimctlShutdown`**：
  - 支持传入模拟器 UDID 或 `booted`，支持一次性关闭所有模拟器（`device = all`）。
- **`SimctlOpenUrl`**：
  - 支持打开网页（如 `https://www.apple.com`）或 App 深层协议 Scheme（如 `weixin://`、`prefs:root=General`）。
- **`SimctlPermission`**：
  - 操作类型：`grant` (授权), `revoke` (撤销), `reset` (重置)。
  - 隐私权限项：`all`, `camera`, `photos`, `location`, `contacts`, `microphone`。
- **`SimctlAddMedia`**：
  - 传入本地图片/视频路径 `media_path`，直接注入系统相册。

---

## 📦 插件清单描述 (Manifest Definition)

```json
{
  "plugin_id": "xy_mobile",
  "name": "手机与安卓模拟器 (Mobile & Emulator)",
  "version": "0.50.5",
  "group": "Mobile",
  "group_icon": "📱",
  "description": "提供连接雷电/MuMu等模拟器与真机、屏幕点击、滑动翻页、文字输入、极速截屏与 App 安装管理等功能",
  "actions": [...]
}
```

---

## 📄 许可证 (License)

本插件遵循免费专有许可协议 (Freeware)。供 小友+ 用户免费下载与使用，未经官方书面授权，严禁对二进制文件进行逆向工程、反编译或二次打包转售。
