# 自动授予隐私权限 (iOS Privacy Permission) (SimctlPermission)

自动给 iOS 模拟器中的 App 授予相机、相册或定位等权限，跳过系统授权弹窗

## 运行参数

* **目标模拟器 UDID (`device`)**
  * 类型: `string`
  * 默认值: `"booted"`
  * 描述: 目标 iOS 模拟器标识。常用预设：`booted`。
* **操作类型 (`action`)**
  * 类型: `string`
  * 默认值: `"grant"`
  * 描述: 权限操作类型：grant 为允许权限，revoke 为禁用权限。常用预设：`grant (授予)`, `revoke (撤回)`, `reset (重置)`。
* **权限服务名称 (`service`)**
  * 类型: `string`
  * 默认值: `"all"`
  * 描述: 隐私服务项：all=所有权限, camera=相机, photos=相册, location=定位。常用预设：`all`, `camera`, `photos`, `location`, `contacts`, `microphone`。
* **应用 Bundle ID (`bundle_id`)**
  * 类型: `string`
  * 默认值: `""`
  * 描述: 目标 App 的 Bundle 标识符。常用预设：`com.example.app`。

## 输出

* 类型: `string`
* 描述: 隐私权限配置生效结果回执。

## 使用示例

```json
{
    "tag":  "SimctlPermission",
    "device":  "booted",
    "action":  "grant",
    "service":  "all",
    "bundle_id":  ""
}
```
