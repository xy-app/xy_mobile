# 相册注入媒体 (iOS Add Media) (SimctlAddMedia)

将电脑上的照片或视频直接导入到 iOS 模拟器的系统相册中

## 运行参数

* **目标模拟器 UDID (`device`)**
  * 类型: `string`
  * 默认值: `"booted"`
  * 描述: 目标 iOS 模拟器标识。常用预设：`booted`。
* **本地媒体文件路径 (`media_path`)**
  * 类型: `FilePicker`
  * 默认值: `""`
  * 描述: 准备注入到相册的照片或视频文件本地路径。常用预设：`test.png`, `sample.mp4`。

## 输出

* 类型: `string`
* 描述: 媒体资源导入生效结果回执。

## 使用示例

```json
{
    "tag":  "SimctlAddMedia",
    "device":  "booted",
    "media_path":  ""
}
```
