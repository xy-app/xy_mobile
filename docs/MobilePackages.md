# 获取已安装应用清单 (List Installed Packages) (MobilePackages)

获取手机或模拟器上已安装的所有软件应用包名列表

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识。常用预设：`auto`。
* **仅列出第三方应用 (`third_party_only`)**
  * 类型: `boolean`
  * 默认值: `true`
  * 描述: 若为 true 则只列出用户安装的应用（pm list packages -3），若为 false 则包含所有系统内置应用。常用预设：`true`, `false`。
* **输出变量名 (`output_alias`)**
  * 类型: `string`
  * 默认值: `"installed_packages"`
  * 描述: 存储包名 JSON 数组的上下文变量名。常用预设：`installed_packages`。

## 输出

* 类型: `string`
* 描述: 设备已安装应用程序包名列表 JSON 字符串。

## 使用示例

```json
{
    "tag":  "MobilePackages",
    "device":  "auto",
    "third_party_only":  true,
    "output_alias":  "installed_packages"
}
```
