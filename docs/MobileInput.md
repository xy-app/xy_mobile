# 文本输入 (Mobile Input Text) (MobileInput)

向手机或模拟器当前选中的输入框输入一段文字

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识，auto 为首选设备。常用预设：`auto`。
* **输入文本 (`text`)**
  * 类型: `string`
  * 默认值: `""`
  * 描述: 需要输入的文本内容。常用预设：`Hello`, `123456`, `test@example.com`。
* **输入前清空内容 (`clear_before`)**
  * 类型: `boolean`
  * 默认值: `false`
  * 描述: 若为 true，则在输入新文本前自动模拟退格删除已有内容。常用预设：`true`, `false`。

## 输出

* 类型: `string`
* 描述: 文本输入操作结果。

## 使用示例

```json
{
    "tag":  "MobileInput",
    "device":  "auto",
    "text":  "",
    "clear_before":  false
}
```
