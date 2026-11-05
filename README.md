# 全营销 GEO 优化助手

这是“全营销 GEO 优化助手”的下载分发仓库。技能面向营销团队：输入营销原稿、资料、行动计划或初步想法，获得 GEO（生成式搜索优化）建议及对应渠道的实际成品。

可以把启用搜索的 AI 理解为一个谨慎、时间有限、需要核对来源的研究助理：它理解问题、寻找相关资料，再组织答案并可能给出引用。这个技能帮助营销信息更容易被理解、发现、核查与总结，同时保留面向人的说服力和转化目标。这是工作模型，并非所有 AI 平台的统一内部流程。

[下载技能包](https://github.com/nicolas819919-Nick/geo-marketing-optimizer/releases/download/v1.0.0/geo-marketing-optimizer.zip) · [完整安装与使用说明](installation.zh-CN.md) · [GEO 培训与方法总结](geo-training.zh-CN.md)

## 能处理什么

覆盖品牌定位、官网与 SEO 内容、电商 listing、社媒与视频、广告、PR、KOL/UGC、邮件与私域、展会、促销、售后、渠道合作和新品上市整合方案。

技能会判断当前动作的 GEO 路径：公开资产可能直接支持检索与引用；广告、线下或私域可能间接支持信息一致性和证据积累；保密动作可以没有直接 GEO 目标。它不会把所有任务都改成 blog 或强行要求公开资料。

## “定痛数权客”

| 检查视角 | 要做什么 |
|---|---|
| 定：看得懂 | 明确品牌、型号、类目、适用人群与市场 |
| 痛：找得到 | 回答目标用户实际关心的问题 |
| 数：可核查 | 用有来源、条件和适用范围的事实支持主张 |
| 权：有源可引 | 区分官方规格、独立证据、转载及商业合作 |
| 客：好总结 | 表达清楚价值与限制，减少空泛口号 |

这是内容检查框架，允许“不适用”，不是五个硬门槛或真实推荐概率公式。广告和社媒仍可保留情绪、故事、品牌语气和 CTA。

## 默认输出

- 营销目标、GEO 路径与必要假设。
- 具体优化建议及修改依据。
- 完整的文案、脚本、页面、brief 或执行方案，按本次渠道与要求交付。
- 关键证据状态、缺失资料与待办事项。
- 对应业务指标，以及适用时的 GEO 观察方法。

资料不完整时，优先完成不依赖未知主张的版本；不能完成的部分会明确说明。图片、视频等媒体成品取决于使用环境的实际工具能力。

## Codex 手动安装

1. 下载并解压 [geo-marketing-optimizer.zip](https://github.com/nicolas819919-Nick/geo-marketing-optimizer/releases/download/v1.0.0/geo-marketing-optimizer.zip)。
2. 将整个 `geo-marketing-optimizer` 文件夹放入 Codex 用户技能目录：macOS/Linux 默认是 `~/.codex/skills/`，Windows 默认是 `%USERPROFILE%\.codex\skills\`；若配置了 `CODEX_HOME`，使用其下的 `skills/`。
3. 保留 `SKILL.md`、`agents/` 和全部 `references/`。升级时先备份旧版，再替换完整文件夹，避免混合版本或重复安装。
4. 新开 Codex 对话并输入 `$geo-marketing-optimizer` 调用；若未显示，重启应用后重试。组织使用统一发现目录时，以组织配置为准。

技能本身不需要 API key 或付费监测工具；离线可依据已提供材料工作。外部事实核查和页面测试需要相应访问能力。

```text
使用 $geo-marketing-optimizer 优化下面的营销动作。
请判断 GEO 路径，给具体建议，并输出对应渠道的完整成品，单列证据缺口。

目标市场与语言：
受众与业务目标：
营销动作与交付要求：
原稿、资料或行动计划：
已有事实与来源：
时间、预算和不可公开信息：
```

不必填满所有字段；也可以从一句想法开始。只有审核需求时，可明确要求“仅审核，不重写”。

## 仓库目录

仓库根目录提供以下分发文件；完整技能源码位于 ZIP 内，没有在仓库中展开。

```text
README.md
geo-marketing-optimizer.zip
installation.zh-CN.md
geo-training.zh-CN.md
```

解压 ZIP 后，完整 7 个技能文件按以下结构保留：

```text
geo-marketing-optimizer/
  SKILL.md
  agents/openai.yaml
  references/
    ai-selection-explainer.md
    channel-playbook.md
    evidence-rules.md
    measurement-and-access.md
    official-sources.md
```

安装时复制整个解压后的文件夹，不要只复制 `SKILL.md`。

## 能力边界

技能不编造参数、客户体验、认证、排名或第三方背书；保密资料不会因为被输入而自动成为公开材料。无联网或未测试时，不声称已经核查来源、页面或 AI 引用效果。

分析和起草不自动包含发布、发送邮件、联系达人、投放或修改线上站点的授权。技能不能保证任何平台收录、引用、推荐、排名或固定增长；被引用、被提及、被推荐与实际转化也应分别观察。平台机制和报告功能可能变化，具体执行时应核查当前官方文档。
