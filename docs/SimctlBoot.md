# 唤醒 iOS 模拟器 (Boot iOS Simulator) (SimctlBoot)

在 Mac 电脑上启动指定的 iOS 苹果模拟器

## 运行参数

* **目标模拟器 UDID (`device`)**
  * 类型: `string`
  * 默认值: `"booted"`
  * 描述: 目标 iOS 模拟器的唯一 UDID 字符串，或填写 'booted' 操作当前已运行项。常用预设：`booted`。

## 输出

* 类型: `string`
* 描述: 模拟器实例唤醒结果回执。

## 使用示例

```json
{
    "tag":  "SimctlBoot",
    "device":  "booted"
}
```
