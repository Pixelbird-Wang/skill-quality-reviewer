# Skill Quality Reviewer

这是一个用于**评审其他 skill 质量好坏**的完整 skill 包。

它不负责生成业务方案，也不负责直接执行某个领域任务。
它的核心作用是：

- 判断一个 skill 是否属于“好的 skill”
- 找出 skill 为什么不好用
- 给出结构化评分与修改建议
- 为团队建立统一的 skill 质量标准

## 适用场景

适合在以下场景使用：

1. 新 skill 上线前评审
2. 存量 skill 体检
3. 多个 skill 候选方案横向比较
4. 组织内部建立 skill 质量门禁

典型问题包括：

- “这个 skill 到底算不算好 skill？”
- “为什么这个 skill 看起来很完整，但实际不好用？”
- “我们如何判断一个 skill 是否值得发布？”
- “我们需要一套统一的 skill 评审标准。”

## 目录结构

```text
skill-quality-reviewer/
├── README.md
├── SKILL.md
├── 示例评审报告.md
└── references/
    ├── review-checklist.md
    ├── anti-patterns.md
    └── scoring-template.md
```

## 文件说明

### `SKILL.md`

主 skill 文件。

包含：

- skill 的元信息
- 质量评审的核心定义
- 十个评分维度
- 六阶段评审流程
- 评分规则
- 常见反模式

### `references/review-checklist.md`

快速检查清单。

适合：

- 评审者先粗看一个 skill
- 做轻量门禁
- 培训新人快速识别问题

### `references/anti-patterns.md`

常见坏 skill 反模式清单。

适合：

- 定位 skill 为什么不好用
- 做复盘时快速归因
- 指导作者避免重复踩坑

### `references/scoring-template.md`

标准评分模板。

适合：

- 直接复制后填写
- 形成评审记录
- 做批量治理时统一格式

### `示例评审报告.md`

真实样板文档。

展示如何用这个 skill 去评审另一个 skill，便于团队理解：

- 该怎么打分
- 该怎么写结论
- 什么算优点
- 什么算问题

## 这个 skill 的核心标准

它判断一个 skill 是否好，主要看这几个方面：

1. 是否容易被正确触发
2. 是否有清晰边界
3. 是否可执行
4. 是否有完成条件和验证机制
5. 是否上下文成本合理
6. 是否安全
7. 是否易于组合和维护

一句话总结：

**好的 skill，不是“写得像专家”，而是“能让 agent 稳定做对事”。**

## 如何使用

### 方法一：直接阅读 `SKILL.md`

适合：

- 你要理解这套标准本身
- 你要把它改造成组织内部规范

### 方法二：用评分模板直接评审

步骤：

1. 打开要评审的目标 skill
2. 对照 `references/review-checklist.md` 过一遍
3. 用 `references/scoring-template.md` 填分
4. 对照 `references/anti-patterns.md` 标注命中的反模式
5. 参考 `示例评审报告.md` 输出正式结论

### 方法三：把它作为组织标准

适合：

- 统一 skill 发布门禁
- 统一仓库治理标准
- 统一作者培训材料

## 推荐的评审顺序

建议按以下顺序使用：

1. `review-checklist.md`
2. `anti-patterns.md`
3. `scoring-template.md`
4. `示例评审报告.md`
5. `SKILL.md`

这样效率更高。

原因是：

- checklist 适合先扫一遍
- anti-patterns 适合快速定位根因
- scoring template 适合规范化落结论
- 示例报告适合理解输出风格
- SKILL.md 适合完整学习整套方法论

## 注意事项

1. 不要把“长”误判成“强”
2. 不要把“像专家说话”误判成“可执行”
3. 不要把“覆盖很全”误判成“更可靠”
4. 对没有完成条件、没有验证条件、没有清晰触发边界的 skill，要特别警惕
5. 如果一个 skill 试图蒸馏完整岗位、完整人格或完整判断力，应视为高风险设计

## 建议的组织使用方式

如果你要在团队里推广这套标准，建议分三层使用：

### 1. 作者自检

写完 skill 后，先用 `review-checklist.md` 自检。

### 2. 同行评审

评审者使用 `scoring-template.md` 输出正式结论。

### 3. 上线门禁

对 P0 问题设为阻断条件：

- 触发严重歧义
- 主体内容不可执行
- 没有结束条件或验证条件
- 高风险动作无 guardrail
- scope 本质失控

## 当前版本说明

当前目录中的内容，是一个**独立可交付版本**。

它的特点是：

- 不依赖现有仓库结构
- 不修改其他项目内容
- 可单独查看、单独发送、单独归档

如果后续你还需要，我也可以继续只在这个目录里追加：

- 组织级标准说明文档
- 多个 skill 的批量评审样板
- 一页纸版评分卡
- 适合管理层的简版说明
