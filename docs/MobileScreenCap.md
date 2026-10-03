# 屏幕截图 (Mobile Screen Capture) (MobileScreenCap)

极速截取手机或模拟器的当前屏幕画面并保存为图片

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标设备序列号或模拟器标识。常用预设：`auto`, `127.0.0.1:16384`, `booted`。
* **保存本地路径 (可选) (`save_path`)**
  * 类型: `FilePicker`
  * 默认值: `""`
  * 描述: 可选截图图片落盘文件完整路径（.png/.jpg）。若为空则仅注入变量。常用预设：`screenshot.png`, `C:/temp/screen.png`。
* **输出 Base64 变量名 (`output_alias`)**
  * 类型: `string`
  * 默认值: `"screen_image"`
  * 描述: 接收 Base64 编码图片数据的上下文变量名。常用预设：`screen_image`。

## 输出

* 类型: `string`
* 描述: 屏幕捕获结果（保存文件路径或 Base64 图像数据）。

## 使用示例

```json
{
    "tag":  "MobileScreenCap",
    "device":  "auto",
    "save_path":  "",
    "output_alias":  "screen_image"
}
```
