# 推送文件到设备 (Adb Push) (AdbPush)

将电脑上的文件或文件夹复制上传到手机的存储目录中

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识。常用预设：`auto`。
* **本地源文件路径 (`local_path`)**
  * 类型: `FilePicker`
  * 默认值: `""`
  * 描述: 计算机上的本地文件或文件夹路径。常用预设：`data.json`, `C:/photos/pic.jpg`。
* **设备目标路径 (`remote_path`)**
  * 类型: `string`
  * 默认值: `"/sdcard/Download/"`
  * 描述: Android 存储卡或设备中的存放绝对路径。常用预设：`/sdcard/Download/`, `/sdcard/Pictures/`, `/data/local/tmp/`。

## 输出

* 类型: `string`
* 描述: 本地文件推送至设备的结果回执。

## 使用示例

```json
{
    "tag":  "AdbPush",
    "device":  "auto",
    "local_path":  "",
    "remote_path":  "/sdcard/Download/"
}
```
