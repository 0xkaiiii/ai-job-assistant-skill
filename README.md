# AI 求职顾问 Skill

中文求职场景的通用 Agent Skill。它把岗位分析、简历生成、面试准备、HR 跟进、谈薪和求职进展记录整合成一套五阶段求职工作流，可用于 Codex、Claude Code、OpenClaw、WorkBuddy、QoderWork、Kimi 等支持 Skill/Agent 工作流的平台。

## 适用平台

这个 Skill 的核心内容是 `skills/ai-job-assistant/SKILL.md` 和简历模板文件，不绑定单一 Agent 平台。当前定位为各类 Agent 通用 Skill，已在仓库中保留 Codex 插件清单，同时也可以按普通 Skill 目录接入 Claude Code、OpenClaw、WorkBuddy、QoderWork、Kimi 等环境。

## 能力概览

| 场景 | 能做什么 |
| --- | --- |
| 岗位解码 | 分析岗位真实需求、匹配度、短板风险和差异化定位 |
| 定向简历 | 基于历史简历和目标 JD，重组经历、优化 bullet，并使用 HTML 模板生成简历 |
| HR 跟进 | 针对已读不回、流程静默、面试后无反馈等场景生成跟进策略和话术 |
| 面试准备 | 解码面试官关注点，准备敏感问题回答和预测问题清单 |
| Offer 谈判 | 计算真实涨幅，识别薪资结构风险，准备谈判话术 |
| 求职记录 | 维护岗位描述库和求职进展记录，便于持续追踪 |
| AI 念力加持 | 通过「念力扫描」「弱点转化」「红线校准」「竞品对标」输出更直接的判断 |

## 仓库结构

```text
.
├── .codex-plugin/
│   └── plugin.json
├── skills/
│   └── ai-job-assistant/
│       ├── SKILL.md
│       └── resume-template.html
├── LICENSE
└── README.md
```

## 安装方式

### 方式一：按平台安装 Skill

把 `skills/ai-job-assistant/` 复制到目标 Agent 平台的 skills 目录。不同平台目录可能不同，请以对应平台文档为准。

```bash
cp -R skills/ai-job-assistant <your-agent-skills-dir>/
```

### 方式二：作为 Codex 插件安装

仓库根目录保留 `.codex-plugin/plugin.json`，需要在 Codex 中作为插件使用时，可以按 Codex 插件方式安装。

### Codex 本地 Skill 目录示例

```bash
cp -R skills/ai-job-assistant ~/.codex/skills/
```

## 使用示例

```text
帮我看看这个岗位，我的背景是 AI 产品经理，短板是没有大厂经历。
```

```text
我上传了历史简历和目标岗位描述，请帮我生成针对这家公司的一版简历。
```

```text
HR 已读不回三天了，帮我判断风险并写一条跟进话术。
```

```text
念力扫描这家公司，看看岗位是新增还是替补，以及谈薪空间大不大。
```

## 简历模板

`resume-template.html` 是一页 A4 中文简历模板，适合打印或导出 PDF。模板包含：

- 个人信息和头像区域
- 个人优势
- 工作经历
- 项目经历
- 教育经历
- 自定义补充模块

## 注意

这个 Skill 会给出求职策略建议，但不会替你编造经历、学历、业绩或薪资信息。所有简历和面试内容应基于真实经历整理。

「今日运势」和「AI 念力加持」偏轻量和娱乐化，不应替代实际求职判断。
