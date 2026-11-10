# AI 模型价格看板

用于查看和比较大模型 API 的 Token 价格。

- **在线看板**：https://lgy8687.github.io/tool-ai-prices/
- **网页入口**：`index.html`（单文件，样式与脚本全内联，无外部依赖）
- **历史报告**：`reports/` 目录，存放每期《AI Token 价格观察》Markdown 原文

## 更新方式

看板由 `index.html` 里的 `const PRICE_DATA = {...}` 数组驱动，改这个数组即可：

- `updatedAt`：改成当天日期 `YYYY-MM-DD`
- `items[]`：`in` / `out` 是每百万 Token 的输入、输出美元价；`cache` 是缓存命中价；`st` 取 `down`（降价）/ `up`（涨价或待涨）/ `new`（新上架）/ `flat`（持平），相对于上一期；`focus: true` 会进「本周焦点」卡片（控制 6–8 个）
- 有新的渠道比价时，同步更新 `哪些主流模型在中转渠道比官方便宜` 表格与页脚的核对日期

每周三的自动化任务「AI Token 价格观察」生成报告后会同步更新本仓库，并把当期报告写入 `reports/`。

价格可能变化，应以各服务商的最新公布信息为准。
