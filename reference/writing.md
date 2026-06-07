# Writing Mode Reference

## Goal

Generate original writing tasks, correct essays, estimate level, provide revision advice, and help the user build flexible templates without encouraging mechanical template abuse.

## Topic Direction Rules

CET-4 writing should focus on:

- campus life;
- learning methods;
- digital habits;
- health routines;
- personal growth;
- volunteering;
- student choices;
- simple social observations.

CET-6 writing should focus on:

- technology and society;
- education;
- public issues;
- career development;
- cultural communication;
- ethical choices;
- sustainability;
- social change;
- personal choices under uncertainty.

## Task Types

Supported writing task types:

- opinion essay;
- phenomenon analysis;
- problem-solution essay;
- advantage-disadvantage essay;
- suggestion essay;
- practical writing: letter, email, notice, proposal;
- data/chart description when suitable.

## Generating Writing Tasks

When the user selects writing:

1. confirm CET-4 or CET-6 if unclear;
2. generate 3 original topic options by default;
3. label each topic with task type and difficulty;
4. ask the user to choose one and write;
5. do not provide a model essay before the user writes unless explicitly requested.

Avoid saying "今年必考." Prefer:

> 根据近年主题趋势，以下是高频备考方向下的原创训练题。

## Writing Scoring (Official Rubric)

四六级作文采用**总体印象评分制**，满分 15 分，5 个固定档次。见 [reference/scoring.md](scoring.md)。

### Feedback Output Format

收到作文后，按以下顺序输出反馈：

1. **档次判定**：按官方 5 档制给分（如"11 分档，12 分"），并换算为 CET 作文分数
2. **总体评价**：一句话概括作文水平
3. **诊断分析**：从切题度、结构、连贯性、语法、词汇、句式、自然度 7 个维度拆解得分偏低的原因
4. **主要优点**
5. **主要问题**
6. **逐句/重点句修改**
7. **高分改写版**
8. **可复用表达**
9. **个性化模板或结构框架**（保分模板 + 提分模板）
10. **下一步重写任务**

## Template Policy

Provide templates only after one of these conditions is met:

- the user has written an essay;
- the user explicitly asks for a template;
- the user is in Study Plan Mode and needs writing structure.

Templates must be flexible and topic-aware. Avoid one-size-fits-all memorized essays.

Provide at least two levels when appropriate:

- 保分模板: stable, clear, low-risk;
- 提分模板: more natural, more argument-driven, less mechanical.

Encourage the user to rewrite after feedback.

## Writing Task Template

```markdown
以下为原创 CET-style 训练，不是官方真题。

你选择的是：{CET-4/CET-6} 写作训练

下面是 3 个高频方向下的原创题目：

1. {Topic A}
   - 类型：{opinion / phenomenon / solution / practical writing}
   - 难度：{easy / medium / hard}
   - 适合训练：{skill focus}

2. {Topic B}
...

请选择一个题目作答。建议字数：{word count}。你写完后，我会按四六级作文维度给你评分、修改和模板。
```

## Writing Feedback Template

```markdown
## 估分
{score range / level}

## 总体评价
{overall assessment}

## 分项评分
| 维度 | 评分 | 说明 |
|---|---:|---|
| 内容切题度 |  |  |
| 结构完整度 |  |  |
| 逻辑连贯性 |  |  |
| 语法准确性 |  |  |
| 词汇丰富度 |  |  |
| 句式多样性 |  |  |
| 语言自然度 |  |  |
| 模板痕迹 |  |  |

## 主要优点
{strengths}

## 主要问题
{problems}

## 重点句修改
{sentence-level revisions}

## 高分改写版
{revised essay}

## 可复用表达
{phrases}

## 个性化模板
{template}

## 重写任务
请基于上面的修改，重写一版。我会对比第一版和第二版，指出具体进步。
```
