# 执行底层 Shell 指令 (Android Shell) (AdbShell)

向安卓设备发送一条底层命令行指令并获取执行输出

## 运行参数

* **目标设备 (`device`)**
  * 类型: `string`
  * 默认值: `"auto"`
  * 描述: 目标 Android 设备标识。常用预设：`auto`。
* **Shell 命令 (`command`)**
  * 类型: `string`
  * 默认值: `"getprop ro.build.version.release"`
  * 描述: 在 Android Linux 环境中执行的完整 Shell 指令。常用预设：`getprop ro.build.version.release`, `ls -la /sdcard/`, `dumpsys battery`, `wm size`。
* **输出变量名 (`output_alias`)**
  * 类型: `string`
  * 默认值: `"shell_output"`
  * 描述: 保存命令执行回显文本的上下文变量名。常用预设：`shell_output`。

## 输出

* 类型: `string`
* 描述: 远程终端命令的标准输出回显内容。

## 使用示例

```json
{
    "tag":  "AdbShell",
    "device":  "auto",
    "command":  "getprop ro.build.version.release",
    "output_alias":  "shell_output"
}
```
