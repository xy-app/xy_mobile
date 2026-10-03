# 获取移动设备与模拟器列表 (Get Devices) (MobileDevices)

自动扫描并连接电脑上打开的安卓模拟器（雷电/MuMu/夜神/AVD）或真机设备

## 运行参数

* **自动扫描并连接模拟器端口 (`auto_connect`)**
  * 类型: `boolean`
  * 默认值: `true`
  * 描述: 是否自动对 MuMu (16384/7555)、雷电 (5555/5557)、夜神 (62001)、逍遥 (21503) 等已知模拟器端口发起健康探测与连接。常用预设：`true`, `false`。
* **输出变量名 (`output_alias`)**
  * 类型: `string`
  * 默认值: `"mobile_devices"`
  * 描述: 存储发现设备 JSON 数组的上下文变量名。常用预设：`mobile_devices`。

## 输出

* 类型: `string`
* 描述: 扫描到的真机与模拟器设备信息 JSON 列表。

## 使用示例

```json
{
    "tag":  "MobileDevices",
    "auto_connect":  true,
    "output_alias":  "mobile_devices"
}
```
