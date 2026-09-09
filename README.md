# 👋 你好，我是 jumao-78

> 全栈开发 / AI 应用开发者 · 专注用大模型构建能落地的业务系统：客服自动化、知识库问答、运营数据分析
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

### 🎨 UI 设计作品集

15 页 UI 设计作品展示（界面设计 / 视觉稿 / 方案展示），由演示文稿逐页导出为高清图，另含 **UI 交互录屏演示**。

👉 **[查看 UI 设计作品集](https://github.com/jumao-78/ui-design-portfolio)** · 🎬 [交互演示视频](https://github.com/jumao-78/ui-design-portfolio/blob/main/videos/ui_demo.mp4) · [第 1 页](https://github.com/jumao-78/ui-design-portfolio/raw/main/pages/01.png) · [第 8 页](https://github.com/jumao-78/ui-design-portfolio/raw/main/pages/08.png)

---

### 🧰 更多项目

- [📋 全部仓库](https://github.com/jumao-78?tab=repositories)

---

## 🛠 技术栈

Python · FastAPI · SQLAlchemy · SQLite / PostgreSQL · OpenAI 兼容 LLM · Prompt 工程 · RAG（BM25 → 向量检索升级路径）· ECharts · Git / GitHub

## 📬 联系我

- 📧 邮箱：[3300486842@qq.com](mailto:3300486842@qq.com)
- 📱 电话：13937217130
