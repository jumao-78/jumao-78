# 👋 你好，我是 jumao-78

> 全栈开发 / AI 应用开发者 · 专注用大模型构建能落地的业务系统：客服自动化、知识库问答、运营数据分析、企业风险监测
> （把“业务痛点 → 系统 + AI 需求”做成真能跑、能演示、有评测数字的产品）

---

## 🚀 精选项目

### 🚢 跨境物流智能客服工作台（Logistics Copilot）

把客服收到的非结构化求助消息（邮件 / 微信 / 电话记录）**自动变成结构化工单 + 智能分类 + 建议回复**，配套 **RAG 知识库问答** 和 **运营看板**。

| | |
|---|---|
| ⚙️ 技术栈 | FastAPI · SQLAlchemy · OpenAI 兼容 LLM（GLM-4-Flash）· BM25 RAG · ECharts · SQLite/PostgreSQL |
| ✨ 工单结构化 | 一次 LLM 调用提取 8 字段（分类/紧急度/意图/提单号/柜号/起运港/目的港）+ 建议回复；无 API Key / 断网自动降级规则模式，全流程不中断 |
| 📚 知识库问答 | Obsidian Markdown 幂等同步 → 切块 → BM25 检索 → 回答带【来源】标注；答不上自动建议转人工 |
| 📊 运营看板 | 4 KPI + 近 7 日趋势 / 分类分布 / Top 意图 / 超时工单，指标全部 SQL 聚合，前端零写死数字 |
| 🧪 评测背书 | 20 条人工标注集：分类准确率规则 100% / LLM 经两轮 Prompt 调优 40% → 95%+，字段提取幻觉 3 处 → 0 |

👉 **[查看项目仓库](https://github.com/jumao-78/logistics-copilot-workbench)** · 全部代码 / 评测报告 / 数据库切换指南 / 知识库管理指南

![运营看板](https://raw.githubusercontent.com/jumao-78/logistics-copilot-workbench/main/docs/screenshots/dashboard.png)

![工单台](https://raw.githubusercontent.com/jumao-78/logistics-copilot-workbench/main/docs/screenshots/tickets.png)

![知识库问答](https://raw.githubusercontent.com/jumao-78/logistics-copilot-workbench/main/docs/screenshots/qa.png)

> ⚠️ 本项目为演示项目，所有数据均为模拟数据（管道真实、数据为造），可在本地完全离线运行。

---

### 🏢 企业风险监测系统（Enterprise Risk Monitor）

把分散在信用中国、企查查、地方黑名单里的企业风险，汇总成 **「一屏能看出问题」的结论**并留痕可追溯。原系统只有 9 页 PPT、无代码无手册，本项目在其基础上做 **增强重设计（非复刻）**：信息一项不少、版式重做，交付 6 页签高保真原型 + 四套工程文档 + 可复现取数管道。

| | |
|---|---|
| ⚙️ 技术栈 | Python 3.12 · MySQL 8（独立实例 / 7 表）· pymysql · deepseek-flash · Playwright · ddddocr · APScheduler · smtplib(QQ SSL) |
| 🖥 6 页签原型 | 总览 / 风险明细 / 取数任务 / AI 与邮件 / 配置 / 系统设置，桌面 + 移动双端；单文件原型零依赖，双击即开 |
| 🧭 工程约束 | 取数**四态**而非布尔（`NO_RECORD` ≠ 无风险）· AI 只解读**不定级**（等级由 11 类规则映射，出参禁 `level`）· 徽章后端算、前端只渲染 · 状态单一来源 `task_record` · 演示标识强制常驻 |
| 📄 文档体系 | 需求分析 / 技术选型 / 开发实施 / UI 设计说明书 v3.0 / 决策台账 / PRD，约 3 万字，每条结论可追溯到决策来源 |
| 🔌 数据管道 | 信用中国批量查询 → 密云黑名单解析 → 快照归一化 → MySQL 入库；25 家真实名单 + 20 家脱敏演示名单 |
| 🎯 设计取向 | 受众是「看结论的领导」与「排障的操作者」——取数链路、异常状态、数据来源全部显性化，不让空白格看起来像"没问题" |

👉 **[查看项目仓库](https://github.com/jumao-78/enterprise-risk-monitor)** · [单文件原型](https://github.com/jumao-78/enterprise-risk-monitor/blob/main/%E4%BC%81%E4%B8%9A%E9%A3%8E%E9%99%A9%E7%9B%91%E6%B5%8B_%E5%8E%9F%E5%9E%8B%E6%B1%87%E6%80%BB.html) · [UI 设计说明书 v3.0](https://github.com/jumao-78/enterprise-risk-monitor/blob/main/%E4%BC%81%E4%B8%9A%E9%A3%8E%E9%99%A9%E7%9B%91%E6%B5%8B%E7%B3%BB%E7%BB%9F_UI%E8%AE%BE%E8%AE%A1%E8%AF%B4%E6%98%8E%E4%B9%A6_v3.0.md)

![总览](https://raw.githubusercontent.com/jumao-78/enterprise-risk-monitor/main/docs/screenshots/overview.png)

![风险明细](https://raw.githubusercontent.com/jumao-78/enterprise-risk-monitor/main/docs/screenshots/detail.png)

<img src="https://raw.githubusercontent.com/jumao-78/enterprise-risk-monitor/main/docs/screenshots/mobile.png" width="260" alt="移动端总览" />

> ⚠️ 本项目为**设计交付 + 可交互原型**，未上线；数据为 2026-10-21 快照而非实时抓取，页面常驻「演示模式」标识。企查查账号无查询权限，取数以 `no_permission` 显式暴露，不静默降级为"无风险"。

---

### 🎨 UI 设计作品集

15 页 UI 设计作品展示（界面设计 / 视觉稿 / 方案展示），由演示文稿逐页导出为高清图，另含 **UI 交互录屏演示**。

👉 **[查看 UI 设计作品集](https://github.com/jumao-78/ui-design-portfolio)** · 🎬 [交互演示视频](https://github.com/jumao-78/ui-design-portfolio/blob/main/videos/ui_demo.mp4) · [第 1 页](https://github.com/jumao-78/ui-design-portfolio/raw/main/pages/01.png) · [第 8 页](https://github.com/jumao-78/ui-design-portfolio/raw/main/pages/08.png)

---

### 🧰 更多项目

- [📋 全部仓库](https://github.com/jumao-78?tab=repositories)

---

## 🛠 技术栈

Python · FastAPI · SQLAlchemy · SQLite / PostgreSQL · OpenAI 兼容 LLM · Prompt 工程 · RAG（BM25 → 向量检索升级路径）· ECharts · MySQL · Playwright · Git / GitHub

## 📬 联系我

- 📧 邮箱：[3300486842@qq.com](mailto:3300486842@qq.com)
- 📱 电话：13937217130
