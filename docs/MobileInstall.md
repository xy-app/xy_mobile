# 安装应用 (Install App / APK / IPA) (MobileInstall)

向手机或模拟器中安装指定的 APK 或应用安装包

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识。常用预设：`auto`。
* **安装包文件路径 (`app_path`)**
  * 类型: `FilePicker`
  * 默认值: `""`
  * 描述: 待安装的应用包在本地计算机上的绝对或相对路径。常用预设：`app-debug.apk`, `build/MyApp.app`。

## 输出

* 类型: `string`
* 描述: 安装包部署执行结果回执。

## 使用示例

```json
{
    "tag":  "MobileInstall",
    "device":  "auto",
    "app_path":  ""
}
```
