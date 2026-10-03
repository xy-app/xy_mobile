# 停止应用 (Stop Mobile App) (MobileStopApp)

强制关闭手机或模拟器上正在运行的应用程序

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识。常用预设：`auto`。
* **应用包名 / Bundle ID (`package_name`)**
  * 类型: `string`
  * 默认值: `""`
  * 描述: 需要停止的目标应用 Package Name 或 iOS Bundle ID。常用预设：`com.tencent.mm`, `com.android.settings`, `com.apple.Preferences`。

## 输出

* 类型: `string`
* 描述: 应用进程终止状态回执。

## 使用示例

```json
{
    "tag":  "MobileStopApp",
    "device":  "auto",
    "package_name":  ""
}
```
