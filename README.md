# 多Agent协作协议·模板仓库

> 以**一个GitHub仓库为唯一事实源**协作的通用模板。
> **无强制分工、无任务认领、无任何权限限制**，

## 如何使用

1. **新建你们自己的项目仓库**（克隆本模板或复制以下文件进去；不要直接在本模板仓库做项目）
2. 改 `reports/agent-1|2|3.md` 的文件名为你们三人代号（如 `agent-张三.md`）
3. 把 `AGENTS.md` 通读一遍（尤其§2报告区格式、§4审核合并循环、§5 checklist）
4. 3人各自 `git clone`，给自己的Agent贴**启动指令**（见下）
5. 开始：任何Agent开工前 `git pull` → 读 AGENTS.md + 全部报告区 + INDICATORS.md → 决定下一步

## Agent启动指令

> 你是本协作组的执行Agent（代号：XXX）。规则：先`git pull`并通读 AGENTS.md 与全部报告区最新行、
> INDICATORS.md；按用户的指示执行或给出下一步计划；完成后推送代码并**在自己的报告区
> （reports/agent-XXX.md）追加登记**（动作/对象/结论/证据四要素）；审核其他成员时，按 AGENTS.md §5
> checklist 实跑复现后把结论写进**自己的报告区**；merge前先读目标PR在各报告区的审核行。
> 所有数字必须来自你实际运行的输出并在 INDICATORS.md 登记（附复现命令）；只追加不删改；
> 与既有结论冲突时在报告区标记"待用户裁决"，不自行定论。

## 目录结构

```
├─ AGENTS.md                    # 唯一权威契约（必读）
├─ INDICATORS.md                # 数字锚：关键数字+复现命令（防各自编数）
├─ reports/                     # 报告区：每人一文件（append-only）
├─ .github/PULL_REQUEST_TEMPLATE.md  # PR模板
└─ data/ code/ results/ paper/  # 产物区（你自己项目的；中间态留本地）
```

## 核心机制一页图

```
Agent X ──写──► reports/agent-X.md ◄──读── Agent Y / 用户
    │                                  │
    └──► 提交PR ──► 各成员在各自报告区登记审核（实跑+证据）
                         │
                 全部非作者成员"通过"？──是──► 任意成员merge（先读报告区确认）
                         │否
                 作者按理由修改→重提→回到审核
```


## LICENSE

MIT（模板本身；你们项目按需更换）。
