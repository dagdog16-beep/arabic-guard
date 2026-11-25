# Arabic Guard — حارس العربية

**A free agent skill that stops AI from breaking Arabic.**

AI agents reverse Arabic text, strand prices and numbers at the wrong edge of the sentence, misplace punctuation, and generate files that open left-to-right. Arabic Guard is a small instruction skill — one `SKILL.md` — that teaches any agent to write Arabic in correct logical order, keep mixed Arabic/Latin content in place, and set proper RTL direction in generated files. It also teaches the agent to *recognize* reversed Arabic in its input and restore it instead of answering garbage.

## Install

```
npx skills add dagdog16-beep/arabic-guard
```

Works with Claude Code, Codex, Cursor, Copilot, Gemini CLI and other agent platforms that support skills.

## What it fixes

| Broken | Fixed |
|---|---|
| `ءاثالثلا موي ةروتافلا ينتلصو` | `وصلتني الفاتورة يوم الثلاثاء` |
| `دولار يوم الثلاثاء 500 دفعت` | `دفعت 500 دولار يوم الثلاثاء` |
| `؟هل وصلتك الرسالة` | `هل وصلتك الرسالة؟` |
| `<p>مرحبا</p>` | `<p dir="rtl" lang="ar">مرحبا</p>` |

More pairs in [examples.md](examples.md). The full rules live in [arabic-guard/SKILL.md](arabic-guard/SKILL.md).

## Why free?

Arabic is one of the world's most-spoken languages and the one AI breaks most visibly. Prevention should be free. If your Arabic is *already* broken — reversed PDFs, scrambled Word exports — the companion repair tool is the free [Arabic Text Fixer](https://github.com/dagdog16-beep/arabic-text-fixer) by the same author.

Made by **Dagdog Tools** (Montréal) — small tools for real problems, offline-first: [Gumroad](https://dagdog2.gumroad.com) · [Payhip](https://payhip.com/DagdogTools)

License: MIT.

---

# حارس العربية

**مهارة مجانية للوكلاء توقف كسر العربية.**

الوكلاء يعكسون النص العربي، يرمون الأسعار والأرقام في الطرف الغالط من الجملة، يضيّعون علامات الترقيم، ويولّدون ملفات تنفتح من اليسار. «حارس العربية» بطاقة تعليمات صغيرة (SKILL.md واحد) تعلّم أي وكيل يكتب العربية بترتيبها الصحيح، يخلّي المحتوى المخلوط (عربي/لاتيني) في بلاصتو، ويضبط اتجاه RTL في الملفات — وتعلّمو أيضاً **يتعرف على العربية المعكوسة** في المدخلات ويصلحها بدل ما يجاوب على الخراب.

## التركيب

```
npx skills add dagdog16-beep/arabic-guard
```

## علاش مجانية؟

العربية من أكثر لغات العالم كلاماً وأكثرها انكساراً عند الذكاء الاصطناعي — الوقاية لازم تكون مجانية. وإذا عربيتك مكسورة أصلاً (PDF معكوس، ملفات Word مشوشة)، أداة الإصلاح المجانية هي [مُصلِح النص العربي](https://github.com/dagdog16-beep/arabic-text-fixer) من نفس الصانع.

من **Dagdog Tools** (مونتريال) — أدوات صغيرة لمشاكل حقيقية، تعمل بلا إنترنت: [Gumroad](https://dagdog2.gumroad.com) · [Payhip](https://payhip.com/DagdogTools)

الترخيص: MIT.
