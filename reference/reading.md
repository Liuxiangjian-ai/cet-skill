# Reading Mode Reference

## Goal

Generate full CET-style reading simulations that are closer to the texture of real CET reading: not only correct in format, but also closer in article density, option ambiguity, paraphrase depth, and distractor design.

The reading module should especially improve CET-6 difficulty. CET-6 reading passages should feel like adapted mid-length articles from sources such as BBC Future, Scientific American, The Guardian, The Conversation, National Geographic, or The Economist: information-rich, moderately abstract, argument-driven, and written with journalistic or science-communication texture rather than plain AI essay style.

For CET-4, keep the topic and logic more accessible, but avoid oversimplified textbook prose.

## Required Reading Subtype Choice

When the user chooses Reading Mode but does not specify the reading subtype, ask this required follow-up question in Chinese before generating any passage:

> 你想练哪一种阅读题型？
> 1. 选词填空（Banked Cloze / 15选10）
> 2. 长篇阅读 / 信息匹配（Paragraph Matching）
> 3. 仔细阅读（Careful Reading）
>
> 我会按完整仿真题型生成；题目风格基于 2015–2025 年真题趋势分析。

Do not generate a generic reading exercise before the subtype is clear.

Recognize common names and route them as follows:

- "选词填空", "十五选十", "15选10", "banked cloze" → Banked Cloze;
- "长篇阅读", "信息匹配", "段落匹配", "paragraph matching" → Paragraph Matching;
- "仔细阅读", "传统阅读", "选择题阅读", "careful reading" → Careful Reading.

## Reading Difficulty Upgrade

Before generating any reading task, apply these standards.

### CET-4 Reading Style

Use:

- familiar but not childish topics;
- clear paragraph progression;
- moderate information density;
- some paraphrase and synonym replacement;
- distractors that are plausible but still resolvable through careful reading.

CET-4 should not become vocabulary-heavy or overly abstract, but it should still require real comprehension.

### CET-6 Reading Style

Use a more authentic article-like style:

- topics may involve education, labor markets, technology, science communication, psychology, health, ecology, urban life, cultural change, economic behavior, or public policy;
- avoid overly neat five-paragraph AI essays;
- reduce obvious signposting such as "This shift is not entirely negative," "Yet there is a risk," "Moreover," and "Therefore" when they make the logic too transparent;
- use more compact sentences, nominalizations, appositives, concessive clauses, qualification, contrast, and mild irony or reservation when appropriate;
- allow the author's stance to emerge through framing and word choice rather than always stating it directly;
- include examples whose relationship to the main point requires interpretation;
- avoid turning every answer into a direct synonym of one sentence.

CET-6 careful-reading passages should feel like edited excerpts from quality English media rather than simplified textbook essays.

## Simulation Principle

For all reading subtypes, follow the exam mechanics and difficulty style:

- follow the section instruction, task format, item count, numbering, answer marking logic, text density, answer evidence, and distractor categories;
- align topic selection, sentence density, information distribution, and distractor logic with 2015–2025 trend patterns;
- default to delayed answer reveal: generate the task first, wait for the user's answers, then provide answer key and explanations.

---

## Banked Cloze Rules: 选词填空 / 15选10

Use when the user chooses 选词填空 / 十五选十 / 15选10 / Banked Cloze.

### Mandatory CET-style Task Instruction

Every Banked Cloze task must begin with this instruction exactly or with only minimal harmless formatting changes:

> In this section, there is a passage with ten blanks. You are required to select one word for each blank from a list of choices given in a word bank following the passage. Read the passage through carefully before making your choices. Each choice in the bank is identified by a letter. Please mark the corresponding letter for each item on Answer Sheet 2 with a single line through the centre. You may not use any of the words in the bank more than once.

Do not describe or generate this as ordinary fill-in-the-blank, grammar completion, multiple-choice cloze, or sentence completion.

### Mandatory Full Simulation Format

Generate exactly this structure:

1. section instruction in English;
2. one passage;
3. ten blanks embedded in the passage, numbered **26–35**;
4. one word bank after the passage;
5. fifteen lettered choices labeled **A–O**;
6. each word-bank choice must be a single English word unless a standard hyphenated word is unavoidable;
7. ask the user to submit answers in the form `26A 27F 28C...`;
8. do not reveal the answer key or explanations until the user submits answers.

### Mandatory Length and Completeness

- CET-4: **220–280 words** in the passage;
- CET-6: **250–320 words** in the passage;
- exactly **10 blanks**;
- exactly **15 choices**.

### Word Bank Design

The word bank must include:

- a realistic mixture of nouns, verbs, adjectives, adverbs, and participles;
- fifteen choices that are plausible at first glance;
- exactly ten correct choices and five distractors;
- distractors that fail for clear reasons such as wrong part of speech, wrong collocation, wrong semantic polarity, wrong tense/form, or wrong local logic;
- no repeated word forms that make the answer ambiguous;
- no word may be used more than once.

For CET-6, avoid making the correct word obvious through one-word collocation alone. At least some blanks should require sentence-level or paragraph-level semantic judgment.

---

## Paragraph Matching Rules: 长篇阅读 / 信息匹配

Use when the user chooses 长篇阅读 / 信息匹配 / 段落匹配 / Paragraph Matching.

### Mandatory CET-style Task Instruction

Every Paragraph Matching task must begin with this instruction exactly or with only minimal harmless formatting changes:

> In this section, you are going to read a passage with ten statements attached to it. Each statement contains information given in one of the paragraphs. Identify the paragraph from which the information is derived. You may choose a paragraph more than once. Each paragraph is marked with a letter. Answer the questions by marking the corresponding letter on Answer Sheet 2.

Do not generate this as ordinary reading comprehension, heading matching, paragraph summary matching, paragraph ordering, or title matching.

### Mandatory Full Simulation Format

Generate exactly this structure:

1. section instruction in English;
2. one long passage with a title;
3. paragraphs marked with letters **[A] through [O]**;
4. ten statements numbered **36–45**;
5. each statement contains information derived from one paragraph;
6. users answer by marking the paragraph letter, e.g. `36C 37A 38F...`;
7. do not reveal the answer key or explanations until the user submits answers.

### Mandatory Length and Completeness

- CET-4: **900–1200 words total**, exactly **15 lettered paragraphs [A]–[O]**;
- CET-6: **1200–1500 words total**, exactly **15 lettered paragraphs [A]–[O]**;
- each paragraph must contain **35–100 words**;
- exactly **10 statements**, numbered 36–45;
- paragraph letters may be used more than once;
- some paragraphs may be unused.

### Statement Design

Statements must:

- be paraphrases, compressions, abstractions, or logical restatements of information in one paragraph;
- not copy sentences directly from the passage;
- test information location, synonym recognition, paragraph gist, and logical equivalence;
- avoid appearing in the same order as the passage whenever possible;
- include enough semantic overlap across paragraphs to feel realistic, while keeping one best paragraph answer.

CET-6 statements should not be simple keyword matches. They should often compress a paragraph's claim, implication, contrast, or example-function into one statement.

---

## Careful Reading Rules: 仔细阅读

Use when the user chooses 仔细阅读 / 传统阅读 / 选择题阅读 / Careful Reading.

### Mandatory Full Simulation Format

Generate exactly this structure:

1. **two passages**, Passage One and Passage Two;
2. each passage has five multiple-choice questions;
3. four options per question, labeled A–D;
4. Passage One questions are numbered **46–50**;
5. Passage Two questions are numbered **51–55**;
6. ask the user to submit answers, e.g. `46A 47C 48D 49B 50A 51C 52D 53A 54B 55C`;
7. do not reveal answers until the user submits.

### Mandatory Length and Completeness

- CET-4: **350–450 words** per passage;
- CET-6: **450–550 words** per passage;
- exactly **2 passages**;
- exactly **5 questions per passage**;
- exactly **4 options per question**.

### CET-6 Careful Reading Article Standards

For CET-6 careful reading, apply all of the following:

- the passage should resemble an adapted quality-media article, not a tidy classroom essay;
- the argument should contain at least one concession, tension, qualification, or shift in perspective;
- avoid making the thesis fully explicit in the first or last sentence;
- include at least one example, study, institutional practice, historical reference, or concrete scenario that supports a broader point;
- use denser phrasing and more abstract vocabulary than CET-4;
- avoid excessive transparent connectors;
- make some relationships inferable rather than fully spelled out.

A CET-6 passage should not read as "topic sentence + explanation + example + conclusion" in every paragraph.

### Question Design

Across the two careful-reading passages, include a realistic mix of:

- main idea / best title;
- detail with paraphrase;
- inference;
- author attitude or tone;
- example function;
- vocabulary in context;
- cause-effect;
- paragraph function;
- author purpose.

Do not make all questions simple location questions.

### Option and Distractor Design

This is critical. Options must force best-answer judgment.

Correct options:

- should be semantically supported by the passage;
- should usually be paraphrased rather than copied from the evidence sentence;
- should avoid direct reuse of rare or distinctive words from the passage when possible;
- should express the underlying claim, not merely repeat a phrase.

Distractors:

- must not be obviously absurd, unrelated, or the simple opposite of the passage;
- should often contain partial truths from the passage but distort the focus, scope, cause, subject, condition, attitude, or conclusion;
- should include "reasonable but not best" choices, especially for main idea, inference, and example-function questions;
- should avoid extreme words such as only, always, never, entirely, unless the trap is deliberate and plausible;
- should be similar in length and style to the correct option.

For CET-6, at least two distractors in each question should be plausible enough that a student must return to the passage and compare details.

### Anti-Obviousness Check Before Output

Before presenting a careful-reading task, internally check:

- Can the correct answer be chosen by matching one obvious phrase from the passage? If yes, rewrite the option.
- Are two or more wrong options obviously unrelated to the passage? If yes, rewrite them using plausible but flawed logic.
- Does the passage rely too heavily on simple signposts? If yes, make the prose more article-like.
- Does each question test understanding rather than mere word spotting? If not, revise.
- Are the correct options consistently longer, more moderate, or more academic than the distractors? If yes, balance option style.
- For CET-6, does the task feel closer to a quality-media adapted article than to a standard AI-generated essay? If not, revise.

After the user answers, explain:

- correct answer;
- evidence location and paraphrased evidence;
- reasoning path;
- why each wrong option is wrong;
- error type and follow-up drill.

---

## Reading Distractor Taxonomy

Use these categories when generating and explaining reading questions:

- source detail but wrong focus;
- concept substitution;
- scope too broad or too narrow;
- reversed causality;
- mismatched subject;
- attitude polarity reversal;
- time or condition mismatch;
- over-inference;
- example mistaken for conclusion;
- concession mistaken for author's final stance;
- keyword repetition without logical support;
- reasonable but not best.

## Reading / Listening Feedback Template

```markdown
## 正确答案
{answer key}

## 定位依据 / 听力线索
{evidence or listening cue}

## 推理路径
{reasoning}

## 干扰项分析
{distractor analysis}

## 错因诊断
{error types}

## 下一题训练方向
{targeted drill}
```
