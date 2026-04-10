# Surge 规则集 (surge-rulesets)

## 🚀 项目简介

`surge-rulesets` 是一个精心维护的 Surge 代理工具规则集仓库，旨在为用户提供高效、稳定且功能丰富的网络代理配置。本规则集涵盖了广告屏蔽、特定国家/地区服务优化、隐私保护等多个方面，帮助用户更好地管理网络流量，提升上网体验。

## ✨ 主要特性

*   **广告与追踪屏蔽**：有效拦截各类广告、恶意追踪器和潜在的恶意域名，提供更纯净的浏览环境。
*   **服务优化**：针对特定应用和服务（如 Apple 服务、Microsoft 服务）进行优化，确保其稳定运行和最佳性能。
*   **地域路由**：提供针对不同国家/地区的流量分流规则，例如 `china.list` 用于回国加速，`us.list` 用于访问美国服务。
*   **易于集成**：规则文件设计简洁，可轻松导入到 Surge 等兼容代理工具中。
*   **持续更新**：规则集会定期进行维护和更新，以适应不断变化的网络环境和应用需求。

## 📦 规则文件列表

本仓库包含以下主要规则文件：

| 文件名           | 描述                                     | 目的                                       |
| :--------------- | :--------------------------------------- | :----------------------------------------- |
| `adblock.list`   | 广告屏蔽规则                             | 拦截广告、追踪器和恶意域名                 |
| `apple.list`     | Apple 服务优化规则                       | 确保 Apple 官方服务、iCloud、App Store 正常运行 |
| `bytedance.list` | 字节跳动服务优化规则                     | 优化抖音、TikTok 等字节跳动系应用访问      |
| `china.list`     | 中国大陆服务直连规则                     | 优化回国访问，确保中国大陆服务流量直连     |
| `malaysia.list`  | 马来西亚服务优化规则                     | 优化马来西亚地区网络服务访问               |
| `microsoft.list` | 微软服务优化规则                         | 确保 Microsoft 官方服务、Office 365 正常运行 |
| `porn.list`      | 成人内容屏蔽规则                         | 屏蔽成人网站和相关内容                     |
| `us.list`        | 美国服务优化规则                         | 优化美国地区网络服务访问                   |
| `BackCN.conf`    | 综合回国配置 (Surge 配置)                | 针对回国访问的完整 Surge 配置文件          |

## 🛠️ 如何使用

### 1. 导入规则集

您可以选择导入单个规则文件，或将 `BackCN.conf` 导入 Surge 作为完整配置。

**方法一：导入单个规则文件 (推荐)**

在您的 Surge 配置中，可以通过 `RULE-SET` 语法引用本仓库的规则文件。例如，要导入 `adblock.list`，请在您的 `[Rule]` 部分添加：

```ini
RULE-SET,https://cdn.jsdelivr.net/gh/SantaG3225/surge-rulesets@main/adblock.list,REJECT
```

请将 `adblock.list` 替换为您希望导入的其他规则文件名，并根据需要调整策略（例如 `DIRECT`, `PROXY`, `REJECT`）。

**方法二：导入 `BackCN.conf` (完整配置)**

`BackCN.conf` 是一个完整的 Surge 配置文件，包含了回国访问所需的全部规则和配置。您可以直接将其作为您的 Surge 配置导入。

1.  复制 `BackCN.conf` 的原始链接：`https://cdn.jsdelivr.net/gh/SantaG3225/surge-rulesets@main/BackCN.conf`
2.  在 Surge 应用中，选择“配置” -> “从 URL 下载配置”，然后粘贴上述链接并导入。

### 2. 更新规则集

为了确保规则集的时效性，建议您定期更新。如果您通过 URL 导入规则集，Surge 通常会自动检查更新。您也可以手动在 Surge 应用中触发更新。

## 🤝 贡献

我们欢迎社区成员对本规则集进行贡献！如果您发现任何规则失效、有新的规则建议，或者希望改进现有规则，请通过以下方式参与：

1.  **提交 Issue**：报告问题或提出建议。
2.  **提交 Pull Request**：直接修改规则文件并提交。

在提交 Pull Request 之前，请确保您的修改符合现有规则格式，并附上简要说明。

## 📜 许可证

本仓库的所有规则集均采用 [MIT 许可证](https://github.com/SantaG3225/surge-rulesets/blob/main/LICENSE) 开源。这意味着您可以自由使用、修改和分发本规则集，但需保留版权声明。

## ⭐ Star 历史

[![Stargazers over time](https://starchart.cc/SantaG3225/surge-rulesets.svg)](https://starchart.cc/SantaG3225/surge-rulesets)

## 📅 更新日志

*   **2026-04-11**：新增详细 README.md 文档，增加 MIT 许可证。
*   **2026-04-04**：首次发布，包含基础规则集。

---

**作者**：Manus AI
**日期**：2026年4月11日
