# Pro Git Bangla Translation — Style Guide

**Status: v1.0 (frozen, 2026-08-07)** — see [rule 23](#23-freeze-the-style-guide) before proposing another policy change. Spend effort translating chapters, not re-litigating rules.

Terminology lives in [GLOSSARY.md](GLOSSARY.md), not here. This file covers everything else: philosophy, audience, tone, and the mechanical rules that keep the translation reviewable and consistent as more contributors join.

## 1. Translation Philosophy

Translate ideas, not words. The goal is to help Bangla-speaking developers understand Git — not to produce a literal, word-for-word translation of the English.

When the English wording sounds unnatural in Bangla, rewrite it while preserving the original meaning.

Priority order:

```
Meaning → Readability → Consistency → Literal translation
```

## 2. Target Audience

University students, junior developers, professional software engineers, DevOps engineers, and open source contributors. They already know many English programming terms — don't replace common technical vocabulary with uncommon Bangla words just to sound more "translated."

## 3. Language Style

Use standard, modern Bangla. Avoid overly literary Bangla, Sanskrit-heavy vocabulary, and colloquial regional dialects. The tone should read like a senior engineer teaching a junior engineer.

## 4. Formality

Use **আপনি** consistently. Never mix তুমি / আপনি / তুই within the book.

✅ আপনি যদি Git ব্যবহার করেন...

## 5. Git Terms

See [GLOSSARY.md](GLOSSARY.md) for the full, authoritative term list — which terms are transliterated into Bangla script (ব্রাঞ্চ, কমিট, মার্জ...) and which stay in English/Latin script (Git, HEAD, Checkout, Rebase, Cherry-pick). Don't invent new Bangla equivalents outside that list without adding them there first.

## 6. Introduce Terms Once

The first time a technical term appears, include both forms if helpful, e.g.:

> Version Control (ভার্সন কন্ট্রোল) হলো এমন একটি ব্যবস্থা...

After that, use whichever single form the glossary specifies, consistently.

## 7. Commands Must Never Change

Everything inside code blocks must remain byte-for-byte identical to the original.

✅ `git commit -m "Initial commit"`
❌ `গিট কমিট -m "Initial commit"`

## 8. Preserve File Names and Paths

Never translate `README.md`, `.gitignore`, `src/`, `package.json`, or any other literal file/path name.

## 9. Keep Terminal Output Intact

Never translate terminal output or error messages inside code blocks.

## 10. Use Natural Bangla Sentence Structure

Don't translate sentence-by-sentence. Ask: "How would I explain this concept to a Bangladeshi developer?"

- English: *Git stores snapshots.*
- Literal (avoid): Git স্ন্যাপশট সংরক্ষণ করে।
- Natural (prefer): Git প্রতিটি গুরুত্বপূর্ণ পরিবর্তনের একটি স্ন্যাপশট সংরক্ষণ করে, যাতে পরে সেই অবস্থায় ফিরে যাওয়া যায়।

## 11. Prefer Active Voice

- Avoid: পরিবর্তনগুলো সংরক্ষণ করা হয়।
- Prefer: Git পরিবর্তনগুলো সংরক্ষণ করে।

## 12. Keep Paragraph Structure

Don't merge or split paragraphs unnecessarily — this keeps future synchronization with the English source easy to diff.

## 13. Do Not Change Examples

Keep example names (John, Alice, Bob) and identifiers (`origin`, `master`, `main`) unchanged unless the upstream English project later updates them.

## 14. Markdown/AsciiDoc Must Match Upstream

Keep headings, bullet lists, numbered lists, blockquotes, tables, admonitions (NOTE/TIP/WARNING/CAUTION), images, and anchors structurally identical to the original.

## 15. Consistent Punctuation

Write naturally in Bangla, but don't force Bangla punctuation (।) into code or Markdown syntax.

✅ Git খুব দ্রুত কাজ করে।
❌ Git খুব দ্রুত কাজ করে.

## 16. Numbers

Prefer English digits (10, not ১০) for consistency with commands, version numbers, and code examples throughout the technical documentation.

## 17. Use English for GitHub UI Terms

Don't translate UI labels that appear verbatim in the GitHub interface: Commit, Pull Request, Clone Repository, Settings, Actions, Issues, Releases.

## 18. Explain Difficult Concepts Clearly

Don't force a literal translation of a hard concept — explain it.

- English: *Distributed Version Control*
- Better: Distributed Version Control এমন একটি ব্যবস্থা যেখানে প্রতিটি ডেভেলপারের কম্পিউটারেই রিপোজিটরির সম্পূর্ণ ইতিহাস সংরক্ষিত থাকে।

## 19. Keep Consistent Terminology

Never vary a term mid-book (always ব্রাঞ্চ, never sometimes শাখা). See [GLOSSARY.md](GLOSSARY.md) and update it — don't drift silently — whenever a new term needs a decision.

## 20. Review Checklist

Before submitting a chapter:

- [ ] Meaning matches the original.
- [ ] Technical terms are consistent with GLOSSARY.md.
- [ ] Commands are unchanged.
- [ ] Code blocks are untouched.
- [ ] Markdown/AsciiDoc structure matches upstream.
- [ ] Spelling is consistent.
- [ ] Grammar has been reviewed by a native Bangla speaker.
- [ ] Another developer has verified the technical accuracy.
- [ ] Read each paragraph aloud once — if it sounds like translated English rather than spoken Bangla, rewrite it (catches awkward phrasing better than silent reading).
- [ ] Reviewed again after a short break, with fresh eyes.

## 21. Translator's Notes

Don't introduce translator's notes into the main text — the goal is a faithful translation, not an annotated one. If a note is absolutely necessary (e.g. a Bangla-specific clarification with no equivalent in the English), it must be clearly marked as a translator's note (e.g. a `[NOTE]` admonition explicitly labeled "অনুবাদকের নোট") and used sparingly — not as a substitute for finding the right natural phrasing.

## 22. Preserve the Author's Voice

Scott Chacon writes in a conversational, approachable style — not academic, not a dry reference manual. Preserve that in Bangla: if the English is light-hearted, let the Bangla be light-hearted too; if it's concise, don't pad it out. This is about tone, distinct from rule 1 (which is about meaning) — a technically accurate translation can still flatten the author's voice if it over-formalizes every sentence.

## 23. Freeze the Style Guide

This guide and GLOSSARY.md are v1.0. From here on:

- Don't revisit earlier chapters just because you found a new preference.
- Don't alternate between Latin and Bangla script for the same term.
- Don't tweak wording that already reads fine, just because you found a "slightly better" phrasing.

Only go back to previously translated chapters for:
- factual mistakes,
- terminology inconsistencies with GLOSSARY.md,
- grammar or spelling errors,
- upstream source changes.

## Pull Requests

- Treat each chapter as an independent, reviewable unit — one chapter per PR whenever possible.
- Include a brief summary of what was translated.
- Mention that Markdown/AsciiDoc structure and code examples are unchanged.
- State that terminology follows GLOSSARY.md.
- Respond to review feedback with technical reasoning, but stay open to language improvements from native speakers.
