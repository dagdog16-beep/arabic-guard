---
name: arabic-guard
description: Write Arabic that renders correctly — never reversed, with numbers, prices, dates, links and Latin words kept in their right places, Arabic punctuation where it belongs, and proper RTL direction in generated files. Use whenever you produce Arabic text (Modern Standard Arabic or any dialect), mixed Arabic/Latin content, Arabic documents, subtitles, captions, or UI strings — and whenever Arabic input looks reversed or scrambled.
---

# Arabic Guard

Arabic breaks in predictable ways when AI generates it or tools extract it: characters come out reversed, numbers and prices jump to the wrong side of the sentence, punctuation lands at the wrong edge, and files open left-to-right. The reader sees garbage even when the words were right.

Your job is to prevent the breakage — and to recognize it when the input already carries it.

## Hard rules

1. **Logical order, always.** Output Arabic in its natural reading order — first word first. Never reverse characters or words "to make it display right". If a tool, file, or user message shows Arabic that reads backwards, that text is broken: restore it (mentally reverse it back) before quoting or using it, and tell the user you did.

2. **Mixed-direction content stays in place.** Numbers, prices, dates, times, URLs, emails, file names, and Latin brand/product names keep their correct position inside the Arabic sentence. If a sentence fights you, restructure it instead of fighting the bidirectional algorithm — put the fragile Latin run at a natural boundary, or split the sentence.

3. **Digits: match the user.** Use Western digits (0-9) or Arabic-Indic digits (٠١٢٣) the way the user and the region do — do not mix both systems in one text. A number always sits next to what it counts: «500 دولار», never stranded at the far edge.

4. **Punctuation belongs to its sentence.** Arabic ؟ ، ؛ go with Arabic sentences; Latin punctuation stays inside Latin fragments. Never leave a punctuation mark orphaned at the start of a line or attached to the wrong clause.

5. **Never "fix" Arabic by transliterating it.** Do not rewrite Arabic in Latin letters, and do not translate word-by-word into stiff calques. Write natural Arabic — or keep an established Latin term as-is (brand names, technical terms like Wi-Fi, PDF, RTX stay Latin).

6. **Files carry direction.** When you generate a file containing Arabic: HTML gets `dir="rtl"` and `lang="ar"` on the Arabic content; documents get right-to-left paragraph direction; subtitles (SRT) and plain text get clean logical-order Arabic with no visual-order tricks; UI strings are marked RTL. A file that opens with Arabic flowing left-to-right is a bug you shipped.

7. **No decorations nobody asked for.** No tatweel (ـ), no full diacritics (tashkeel), no ornamental brackets — unless the user asks for them or the text is Quranic/educational.

## Recognizing broken input

Arabic extracted from PDFs, Word files, and old software often arrives reversed or scrambled. Signs:

- Words read backwards («مويلا» where «اليوم» was meant).
- A sentence that only makes sense read from the last word to the first.
- Punctuation and numbers piled at the wrong edge.

When you see this: say plainly that the text arrived reversed, restore the correct order, and work with the restored text. Do not answer the scrambled text as if it were normal, and do not copy the scramble into your output.

## Self-check before sending

Read your Arabic output once, as an Arabic reader would:

- [ ] The first word is the sentence's real first word.
- [ ] Every number sits beside what it counts; prices read naturally.
- [ ] No Latin fragment is stranded at the wrong edge of a line.
- [ ] ؟ and ، sit at the true ends of their clauses.
- [ ] Nothing reads backwards; nothing is transliterated.
- [ ] Any generated file opens right-to-left.

If a check fails, fix the sentence — restructure it if needed — then send.

## Register and dialect

These form rules apply to Modern Standard Arabic and to every dialect (Maghrebi, Egyptian, Levantine, Gulf). Match the user's own register and dialect in wording; keep the form rules identical. Correct form never means forcing a dialect speaker into formal Arabic.
