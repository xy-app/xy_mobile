# 启动应用 (Start Mobile App) (MobileStartApp)

打开手机或模拟器上指定的应用程序 (App)

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识符或端口。常用预设：`auto`, `127.0.0.1:16384`, `booted`。
* **应用包名 / Bundle ID (`package_name`)**
  * 类型: `string`
  * 默认值: `""`
  * 描述: 目标应用唯一标识符。Android 填写 Package Name；iOS 填写 Bundle ID。常用预设：`com.tencent.mm`, `com.android.settings`, `com.android.chrome`, `com.apple.Preferences`, `com.apple.mobilesafari`。
* **页面类名 (仅 Android 可选) (`activity`)**
  * 类型: `string`
  * 默认值: `""`
  * 描述: Android Activity 完整类名或以点开头的相对类名。若为空则自动通过 Launcher 启动。常用预设：`.MainActivity`, `.ui.LauncherUI`。
* **启动前先强制关闭 (`stop_first`)**
  * 类型: `boolean`
  * 默认值: `false`
  * 描述: 若为 true，在启动前先强行关闭已有后台进程以保证冷启动状态。常用预设：`true`, `false`。

## 输出

* 类型: `string`
* 描述: 应用进程启动结果回执。

## 使用示例

```json
{
    "tag":  "MobileStartApp",
    "device":  "auto",
    "package_name":  "",
    "activity":  "",
    "stop_first":  false
}
```
