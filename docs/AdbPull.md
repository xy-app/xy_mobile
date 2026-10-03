# 从设备拉取文件 (Adb Pull) (AdbPull)

将手机中的照片、文档或文件夹下载保存到电脑上

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备标识。常用预设：`auto`。
* **设备端源文件路径 (`remote_path`)**
  * 类型: `string`
  * 默认值: `"/sdcard/Download/test.txt"`
  * 描述: Android 存储上的文件绝对路径。常用预设：`/sdcard/Download/test.txt`, `/sdcard/log.txt`。
* **本地保存路径 (`local_path`)**
  * 类型: `FilePicker`
  * 默认值: `"./downloaded.txt"`
  * 描述: 保存到本地计算机的路径。常用预设：`./downloaded.txt`, `C:/temp/export.log`。

## 输出

* 类型: `string`
* 描述: 从设备拉取文件至本地的结果回执。

## 使用示例

```json
{
    "tag":  "AdbPull",
    "device":  "auto",
    "remote_path":  "/sdcard/Download/test.txt",
    "local_path":  "./downloaded.txt"
}
```
