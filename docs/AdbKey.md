# 发送系统按键 (Android Key Event) (AdbKey)

模拟按下手机的系统按键，如返回键、Home键、任务列表或电源键

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识。常用预设：`auto`。
* **按键名称 / KeyCode (`key_code`)**
  * 类型: `string`
  * 默认值: `"BACK"`
  * 描述: 系统按键枚举代码（如 BACK=返回, HOME=主页, APP_SWITCH=多任务列表）或整数键值。常用预设：`BACK`, `HOME`, `APP_SWITCH`, `POWER`, `VOLUME_UP`, `VOLUME_DOWN`, `ENTER`, `DEL`。

## 输出

* 类型: `string`
* 描述: 物理按键广播发送状态结果。

## 使用示例

```json
{
    "tag":  "AdbKey",
    "device":  "auto",
    "key_code":  "BACK"
}
```
