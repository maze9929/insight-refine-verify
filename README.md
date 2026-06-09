# insight-refine-verify（洞察·淬炼·验证）

一套结构化的代码改动方法论。适用于：bug 修复 / 功能添加 / 代码重构 / 安全审查 / 架构变更。

> **核心思想**：不动手先看，不通过不出，不复原不算完。

## 快速开始（Trae IDE）

1. **在项目根目录创建技能文件夹**：
   ```
   .trae/skills/insight-refine-verify/SKILL.md
   ```

2. **把本仓库的 `SKILL.md` 复制进去**

3. **或一键安装**（在 Trae 终端中执行）：
   ```bash
   # Windows PowerShell
   mkdir -p .trae/skills/insight-refine-verify
   curl -o .trae/skills/insight-refine-verify/SKILL.md https://raw.githubusercontent.com/maze9929/insight-refine-verify/main/SKILL.md
   ```

## 全局安装（所有 Trae 项目都能用）

```bash
# Windows PowerShell
mkdir -p "$env:USERPROFILE\.trae-cn\skills\insight-refine-verify"
curl -o "$env:USERPROFILE\.trae-cn\skills\insight-refine-verify\SKILL.md" https://raw.githubusercontent.com/maze9929/insight-refine-verify/main/SKILL.md
```

## 使用方法

在 Trae 的对话中直接说类似的话，AI 会自动加载本技能：
- "帮我修个 bug"
- "这个接口返回数据不对，排查一下"
- "重构一下这段代码"
- "做个安全审查"

## 文档

- **[SKILL.md](./SKILL.md)** — AI 读取的指令集（精简版）
- **[方法论完整文档.md](./方法论完整文档.md)** — 详细解释和案例（给人读的）

## 核心流程

```
Step 0 → 选强度（L0-L4）
Phase 1 → 洞察（只读不改）
Phase 2 → 淬炼（方案→审核→代码）
Phase 3 → 分析（影响矩阵+风险分级）
Phase 4 → 验证（部署+测试+日志观测）
Phase 5 → 闭环（结案报告）
```

## 三条铁律

1. 没找到根因，绝不改代码
2. 一次只解决一个问题
3. 产出必审核，审核必记录
