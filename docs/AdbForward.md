# 端口映射转发 (Adb Forward) (AdbForward)

在电脑端口与手机网络端口之间建立通信管道

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识。常用预设：`auto`。
* **本地端口 (Host Socket) (`local_port`)**
  * 类型: `string`
  * 默认值: `"tcp:8080"`
  * 描述: 本地宿主机监听的端口定义，如 'tcp:8080'。常用预设：`tcp:8080`, `tcp:9090`, `tcp:5000`。
* **设备端口 (Remote Socket) (`remote_port`)**
  * 类型: `string`
  * 默认值: `"tcp:8080"`
  * 描述: Android 目标端转发的端口定义，如 'tcp:8080'。常用预设：`tcp:8080`, `tcp:8000`, `tcp:5000`。

## 输出

* 类型: `string`
* 描述: 端口映射建立结果回执。

## 使用示例

```json
{
    "tag":  "AdbForward",
    "device":  "auto",
    "local_port":  "tcp:8080",
    "remote_port":  "tcp:8080"
}
```
