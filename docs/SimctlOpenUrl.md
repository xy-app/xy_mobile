# 调起 URL Scheme / 网页 (iOS Open URL) (SimctlOpenUrl)

在 iOS 模拟器中自动打开指定网址或调起 App

## 运行参数

* **目标模拟器 UDID (`device`)**
  * 类型: `string`
  * 默认值: `"booted"`
  * 描述: 目标 iOS 模拟器标识。常用预设：`booted`。
* **目标 URL / Scheme (`url`)**
  * 类型: `string`
  * 默认值: `"https://www.apple.com"`
  * 描述: 待打开的标准网页地址或应用自定义协议（如 weixin://）。常用预设：`https://www.apple.com`, `weixin://`, `prefs:root=General`。

## 输出

* 类型: `string`
* 描述: 深度链接调起结果回执。

## 使用示例

```json
{
    "tag":  "SimctlOpenUrl",
    "device":  "booted",
    "url":  "https://www.apple.com"
}
```
