# 卸载应用 (Uninstall App) (MobileUninstall)

从手机或模拟器中彻底卸载删除指定的应用程序

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识。常用预设：`auto`。
* **应用包名 / Bundle ID (`package_name`)**
  * 类型: `string`
  * 默认值: `""`
  * 描述: 待卸载的应用 Package Name 或 Bundle Identifier。常用预设：`com.example.app`。

## 输出

* 类型: `string`
* 描述: 应用卸载执行结果回执。

## 使用示例

```json
{
    "tag":  "MobileUninstall",
    "device":  "auto",
    "package_name":  ""
}
```
