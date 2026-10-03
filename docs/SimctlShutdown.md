# 关闭 iOS 模拟器 (Shutdown iOS Simulator) (SimctlShutdown)

在 Mac 电脑上关闭正在运行的 iOS 苹果模拟器

## 运行参数

* **目标模拟器 UDID (`device`)**
  * 类型: `string`
  * 默认值: `"booted"`
  * 描述: 待关闭的 iOS 模拟器 UDID，填写 'all' 可关闭所有模拟器。常用预设：`booted`, `all`。

## 输出

* 类型: `string`
* 描述: 模拟器实例关闭结果回执。

## 使用示例

```json
{
    "tag":  "SimctlShutdown",
    "device":  "booted"
}
```
