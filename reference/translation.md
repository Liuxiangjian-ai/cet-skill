# Translation Mode Reference

## Goal

Generate original Chinese paragraphs for translation, correct user translations, explain Chinese-to-English transfer problems, and provide standard and higher-scoring versions.

## Topic Direction Rules

CET-4 translation should use moderate information density and common themes:

- traditional culture;
- campus and community life;
- transportation;
- digital services;
- health;
- tourism;
- city life;
- social development.

CET-6 translation may include:

- cultural heritage;
- modernization;
- ecological development;
- smart cities;
- education equity;
- digital governance;
- innovation;
- public services;
- cross-cultural communication.

## Generating Translation Tasks

When the user selects translation:

1. confirm CET-4 or CET-6 if unclear;
2. generate one original Chinese paragraph;
3. do not provide the English answer immediately;
4. ask the user to translate first.

If the user asks for immediate explanation, provide answer and breakdown.

## Translation Scoring (Official Rubric)

四六级翻译采用**总体印象评分制**，满分 15 分，5 个固定档次。见 [reference/scoring.md](scoring.md)。

### Feedback Output Format

收到译文后，按以下顺序输出反馈：

1. **档次判定**：按官方 5 档制给分，并换算为 CET 翻译分数
2. **总体评价**
3. **诊断分析**：从信息完整度、语义准确性、语法、表达自然度、术语处理、语序组织 6 个维度拆解
4. **主要误译或漏译**
5. **中式英语问题**
6. **句法拆解**
7. **标准译文**
8. **高分译文**
9. **可复用表达**
10. **针对性小练习**

## Answer Version Rules

Standard answer:

- preserve all key information;
- use natural English structure;
- avoid word-for-word translation;
- stay concise and complete.

Higher-scoring answer:

- reorganize information when English requires it;
- compress repeated Chinese structures;
- use accurate collocations and transitions;
- explain culture-specific concepts when needed.

保底译文 (minimum-viable translation, for weak foundation users):

- preserve all key information points;
- use simple but correct sentence structures;
- avoid any grammatical errors;
- accept slightly less natural phrasing as long as it's correct.

## Translation Task Template

```markdown
以下为原创 CET-style 模拟仿真训练。

你选择的是：{CET-4/CET-6} 翻译训练

请将下面这段中文翻译成英文：

{original Chinese paragraph}

先不要看答案。你提交译文后，我会从信息完整度、准确性、语法、自然度和中式英语问题几个方面批改。
```

## Translation Feedback Template

```markdown
## 信息完整度
{assessment}

## 主要误译 / 漏译
{issues}

## 中式英语问题
{Chinglish problems}

## 句法拆解
{structure analysis}

## 标准译文
{standard version}

## 高分译文
{higher-scoring version}

## 可复用表达
{expressions}

## 针对性小练习
{mini drill}
```
