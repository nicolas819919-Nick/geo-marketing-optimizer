# 全营销 GEO 优化助手：安装与使用

技能名：`geo-marketing-optimizer`；版本：1.0.0；更新：2026-11-05。

它接受营销原稿、文件、链接、行动计划或初步想法，自动判断 GEO 路径，给出具体优化建议，并输出对应渠道的文案、脚本、brief、页面或执行方案。支持全营销动作；不用先把任务改写成 blog。

## 分发哪些文件

- [geo-marketing-optimizer.zip](geo-marketing-optimizer.zip)：发给同事安装的技能包，包含完整技能文件。
- [GEO 培训与方法总结](geo-training.zh-CN.md)：可直接用于内部宣讲或公告。
- 本文件：安装和调用说明。

压缩包解开后应看到：

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

保留整个文件夹，不能只复制 SKILL.md，否则会丢失渠道、证据和测量规则。

## Codex 安装

按以下步骤在你的电脑上安装：

1. 解压技能包。
2. 将整个 `geo-marketing-optimizer` 文件夹复制到 Codex 用户技能目录。默认位置：macOS/Linux 为 `~/.codex/skills/`，Windows 为 `%USERPROFILE%\.codex\skills\`；如配置了 `CODEX_HOME`，使用其下的 `skills/`。
3. 若所在组织已统一使用其他 Codex skills 发现目录，依现有配置安装到一处即可，避免同名重复。不要在已有同名目录中混合新旧文件；升级时先备份旧版，再用完整新文件夹替换。
4. 新开一个 Codex 对话；如未显示技能，重启应用后再开对话。输入 `$geo-marketing-optimizer` 选择/调用。

若没有文件夹管理经验，也可在支持本地文件操作的 Codex 中粘贴下面的安装请求，并附上实际解压路径：

> 请把这个解压目录中的 geo-marketing-optimizer 完整安装到我的 Codex 用户技能目录，保留 references。先检查同名目录，若已存在先备份再替换，不修改其他技能。安装后检查 SKILL.md 和相对引用完整。

安装不需要 API key、付费监测工具或额外 Python 依赖。联网只在核查外部来源/实际页面时需要；无联网也能用已提供材料工作，会注明核查限制。

## 其他支持 SKILL.md 的工具

可复用相同的技能文件夹，安装路径与上传方式遵循目标工具当前文档。例如 Claude Code 使用其本地 skills 目录时可放到 `~/.claude/skills/`。Codex 的 `agents/openai.yaml` 是 UI 元数据，其他工具未必读取。这里没有验证所有客户端的导入与自动触发行为。

若工具不支持技能安装，可让它读取 SKILL.md 及本任务对应的 references 后工作；这是手动使用资料，不等于已安装技能。

## 最简单的调用

```text
使用 $geo-marketing-optimizer 优化下面的营销动作。
请先判断 GEO 路径，给具体建议，再直接输出对应渠道的完整成品，单列证据缺口。

目标市场/语言：
受众与业务目标：
营销动作/渠道：
原稿或行动计划：
已有事实与来源：
约束（选填：预算、时间、字数、不可公开内容）：
```

上面的信息用于提高质量，不是必须全部填完。只有一句想法也可以开始；关键事实不足时会删去未知主张或标明草稿状态。

## 各岗位可直接复制的请求

**内容/官网**

> 使用 $geo-marketing-optimizer 优化这篇面向美国用户的选购文章。保留原目标，给我完整英文修订稿、必要标题与描述、引用来源和待补证清单。原稿及资料如下：……

**社媒/视频**

> 使用 $geo-marketing-optimizer，把以下真实演示资料做成 Instagram post 和 30 秒短视频脚本。目标是引导访问产品页。保留吸引力，讲清具体型号和演示条件，不编用户体验：……

**投放**

> 使用 $geo-marketing-optimizer 审查这份 Meta 广告 brief。先指出无法支持的承诺，再给可用广告文案、创意脚本及必要的落地页修改。以转化为目标，不要求广告本身成为可索引文章：……

**达人/公关**

> 使用 $geo-marketing-optimizer 优化这次 KOL 合作方案。请输出 creator brief、实际测试任务、视频框架和合作披露；样机还未交付，不写成已有体验。资料：……

> 使用 $geo-marketing-optimizer，把真实参展记录做成新闻稿和媒体 pitch 草稿。请核对参展与背书的区别，不发送。资料：……

**邮件/渠道/线下**

> 使用 $geo-marketing-optimizer 优化这组经销商邮件，输出主题、正文和 CTA。资料含未上市信息，只供已授权收件人使用，不生成公开页面：……

> 使用 $geo-marketing-optimizer 优化展会获客动作，输出展板文案、演示话术和线索跟进流程。只有适合且可公开时才建议配套公开资料：……

**产品上市/整合营销**

> 使用 $geo-marketing-optimizer 优化下面的新品上市方案。请保留目标市场、预算和上市窗口，给整合执行方案、各渠道 GEO 作用及本次要求的核心物料成稿，不只给建议表：……

**内部培训**

> 使用 $geo-marketing-optimizer，给团队做一份 5 分钟宣讲稿。先讲启用搜索的 AI 怎么选答案，再讲定痛数权客，最后用我们本周的营销动作示范。不要把启发式公式当真实算法：……

## 如何检查输出是否合格

应能看到：营销目标和 GEO 路径、具体可执行修改、对应渠道的实际成品、关键证据状态、适合本动作的验证指标。没有实时测试时不应出现编造的引用率；未核实数据不应被写成“已验证”。

技能默认制作草稿和优化建议。发帖、发邮件、联系达人、投放、修改线上站点需要相应明确授权。内容进入团队现有发布审核流程，技能不替代事实确认与权限管理。
