# Listening Mode Reference

## Goal

Generate original listening scripts and questions, simulate CET-style listening comprehension, and diagnose listening errors.

## Scene and Difficulty Rules

CET-4 listening should use:

- clear scenes;
- moderate information density;
- explicit transitions;
- familiar contexts such as campus services, everyday problems, health, basic technology, community life, and short news reports.

CET-6 listening should use:

- denser reporting;
- interviews;
- talks and lectures;
- research findings;
- policy or social issues;
- professional contexts;
- implicit reasoning and viewpoint changes.

## Length Rules

- CET-4 short news/report: 90–140 words.
- CET-4 long conversation: 250–350 words.
- CET-4 passage: 220–300 words.
- CET-6 report/talk segment: 160–240 words or longer when appropriate.
- CET-6 long conversation: 350–450 words.
- CET-6 passage/lecture: 300–400 words.

## Listening Task Flow

When generating listening practice:

1. provide 5–8 pre-listening vocabulary items that do not reveal answers;
2. provide the listening script only if the user asks for transcript mode, or if the platform cannot play audio;
3. provide questions without answers;
4. wait for user answers;
5. provide answer key, cue paraphrase, skill tested, distractor logic, and next-step practice.

If no audio generation is available, present the script as "朗读/自读脚本" and suggest the user read once without looking back before answering.

## Script-Only Mode (Fallback)

When audio playback is not available:

1. Present the script with clear section breaks.
2. Instruct the user: "请自读以下脚本，只读一遍，不回看，然后作答。"
3. Use `[PAUSE]` markers between sections to simulate listening pacing.
4. After the user answers, provide the full feedback per the reading/listening feedback template.

## Listening Distractor Taxonomy

- misheard keyword (similar-sounding word);
- information from wrong part of the conversation;
- opposite polarity (positive/negative reversed);
- wrong speaker attribution;
- correct detail but wrong context;
- time/sequence confusion;
- inferred-but-not-stated trap;
- reasonable real-world assumption not supported by audio.
