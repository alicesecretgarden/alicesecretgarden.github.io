# Axure 交付包（可直接导入）

> 说明：当前仓库环境无法调用 Axure 官方引擎直接产出完整 `.rp` 二进制工程文件，
> 但已提供 **Axure 可导入的结构化文件**，可在 Axure RP 9/10 中快速生成页面骨架。

## 文件清单

- `party-branch-activity-pages.csv`：页面与组件清单（可导入 Axure 的 Repeater 或用于批量生成控件）。
- `party-branch-activity-flow.csv`：审批流泳道节点数据（用于流程图快速搭建）。
- `party-branch-activity-ledger.csv`：活动台账示例数据（用于表格/Repeater 数据源）。

## 在 Axure 中的使用步骤

1. 新建 Axure 工程，创建 3 个页面：
   - 活动台账
   - 新建活动
   - 审批流配置
2. 在“活动台账”页面插入 Repeater，导入 `party-branch-activity-ledger.csv`。
3. 在“审批流配置”页面插入 Repeater，导入 `party-branch-activity-flow.csv`。
4. 在任意页面插入 Repeater 或表格，导入 `party-branch-activity-pages.csv` 作为组件字典。
5. 依据 `index.html` 的视觉稿进行样式微调（色彩、间距、标签状态）。

## 规则已内置

- 实际支出确认后，同步到党费使用台账。
- 审批复杂度按经费金额分级：
  - 无经费：自动通过
  - 有经费且 <= 10000：支部书记审批
  - 有经费且 > 10000：支部书记初审 + 上级党委/财务多级审批


## 最小可打开模板结构规范

- 请先阅读：`minimal-openable-template-spec.md`
- 该文档用于你在本地 Axure 快速创建最小工程并一键另存为 `.rp`。
