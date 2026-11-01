# Clash-meta-Config

一份面向 [Mihomo（Clash Meta）](https://github.com/MetaCubeX/mihomo) 的规则配置，适用于桌面和移动设备。配置基于 [liuran001 的 mihomo 懒人配置](https://gist.github.com/liuran001/5ca84f7def53c70b554d3f765ff86a33) 修改；感谢原作者的整理与维护。

> 使用前请先填写自己的机场订阅地址。仓库中的订阅地址留空，不包含可直接使用的代理节点。

## 配置文件

| 文件 | 说明 |
| --- | --- |
| `Config.yaml` | 主配置，包含代理分组、DNS、规则和订阅提供者设置。 |
| `ConfigTiny.yaml` | 精简配置，计划逐步废弃；新配置建议以 `Config.yaml` 为准。 |

## 快速开始

1. 下载或克隆本仓库。
2. 用文本编辑器打开 `Config.yaml`，在 `proxy-providers` 中填写 `A` 的订阅地址；如需使用第二个订阅，也填写 `B`。
3. 如果只配置一个订阅，在上方 `use` 列表中移除 `B`。
4. 将配置导入支持 Mihomo 的客户端，并确认客户端可以访问配置中引用的规则集和 Geo 数据源。

请勿把包含个人订阅令牌的配置公开上传或分享。

## 分流与策略组

配置按用途组织策略组，方便在客户端中选择节点：

- **金融**：PayPal、Crypto
- **AI**：AI 服务及 Apple Intelligence / Siri 相关域名
- **视频**：YouTube、Twitch、TikTok；X 的 `video.twimg.com` 视频流量交由 YouTube 策略组处理
- **其他服务**：Telegram、GitHub、OneDrive、游戏和 X
- **平台与兜底**：Google、Apple、Microsoft、国内直连及漏网之鱼
- **地区节点**：香港、台湾、韩国、日本、美国、新加坡及其他地区

哔哩哔哩和巴哈姆特策略组放在服务组末尾。启用哔哩哔哩代理可能影响部分版权视频的可用性或播放速度。

具体匹配顺序以 `Config.yaml` 的 `rules` 列表为准；规则从上到下匹配，较具体的规则应放在较宽泛的规则之前。

## 自定义提示

- 主要可调整内容集中在 `Config.yaml` 的“基础配置”区域。
- 代理组名称需要与规则中使用的策略组名称一致。
- 如果修改了订阅提供者名称，也要同步更新 `use` 列表。
- 规则集和 Geo 数据需要由客户端按配置地址获取；网络环境可能影响更新。

## 致谢

- 配置模板与说明：[liuran001](https://github.com/liuran001)
- Mihomo 内核：[MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo)
- 上游配置：[mihomo 懒人配置](https://gist.github.com/liuran001/5ca84f7def53c70b554d3f765ff86a33)

如本项目对你有帮助，也欢迎为上游项目点亮 Star。

