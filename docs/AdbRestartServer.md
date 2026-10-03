# 重启 ADB 服务与自愈 (Restart ADB Server) (AdbRestartServer)

一键重启 ADB 连接服务，快速解决手机掉线或端口冲突问题

## 运行参数

* **重启后诊断设备 (可选) (`diagnose_device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 服务重启完成后自动验证其连接状态与 USB 授权情况的目标设备。常用预设：`auto`, `127.0.0.1:16384`。

## 输出

* 类型: `string`
* 描述: 服务重启与自愈巡检状态回执。

## 使用示例

```json
{
    "tag":  "AdbRestartServer",
    "diagnose_device":  "auto"
}
```
