---
name: telugu-english-notes
description: Write detailed, study-note-style explanations of any topic in natural Tenglish (Telugu words spelled out in plain Roman/English letters, casually mixed with English technical terms) — no Telugu script, no bracketed "(romanization)" side-notes. Use this whenever the user asks for notes, an explanation, or a summary "in telugu english mix", "in tenglish", "telugu la cheppu", "in my language" (when the user's language is Telugu-English mix), or otherwise asks to explain a topic the way they'd chat about it in Telugu-English. Applies to any subject — tech concepts, architecture, science, exam prep, anything — and should produce a complete reference note: explanation, examples, an architecture/structure diagram, and a step-by-step working flow, not a short summary.
---

# Telugu-English (Tenglish) Notes

## What this skill is for

The user thinks and chats in a natural Telugu-English mix ("Tenglish") — Telugu
words spelled out in plain Roman letters, dropped into English sentences the
way people actually text/chat, not formal transliteration. When they ask for
notes on a topic "in telugu english mix," write the whole explanation in that
voice, in detail, so it fully replaces a normal English explanation — not a
translation layered on top of one.

Reference line the user gave as the target style (study this closely, it's
the ground truth for tone and word choice):

> Discovery lightweight (name+description matrame), activation matching
> request vachinappudu full instructions load avutundi — idi progressive
> disclosure.

## Hard rules (things that break the style if violated)

1. **No Telugu script.** Never output actual Telugu-alphabet (native script)
   characters. Every word, Telugu or English, is written in the plain Roman
   alphabet — spell Telugu words out phonetically instead.
2. **No romanization side-notes.** Never write patterns like `word (romanized
   word)`, `word [translation]`, or "romanized as...". The Tenglish word just
   *is* the sentence — say it once, plainly, the way the reference line does.
   This is the single most common way this goes wrong: producing a clean
   English sentence and then bolting a parenthetical Telugu gloss onto it.
   Don't do that — write the sentence natively in the mix from the start.
3. **Keep English jargon in English.** Technical terms, product names, code,
   acronyms (API, discovery, activation, progressive disclosure, etc.) stay
   in English exactly as a Telugu engineer would say them out loud. Only the
   connecting tissue — verbs, conjunctions, explanations of *why* and *how*
   — shifts into Telugu. Don't force-translate jargon into Telugu; that's
   not how anyone actually talks.
4. **Sound like a person, not a phrasebook.** Vary sentence structure the way
   the reference line does (English clause, Telugu verb, em-dash, Telugu
   connector, English noun phrase...). Don't mechanically Telugu-ify every
   third word — let it flow like real speech.

## Common Tenglish connectors to draw on

These are the everyday glue words that make Telugu-English mixing feel real
(spelled phonetically, no script). Use them where they fit naturally — don't
force all of them into one note:

| Romanized Telugu | Rough sense in English |
|---|---|
| `ante` | means / that is |
| `kuda` | also / even |
| `kosam` | for / for the purpose of |
| `valla` | because of / due to |
| `dwara` | through / by means of |
| `kaani` | but |
| `ala` / `ila` | like that / like this |
| `undi` / `untundi` | is / exists / stays |
| `avutundi` | becomes / happens / ends up |
| `cheyyali` | need to do |
| `cheyali antey` | if you want to do (it) |
| `teliyali` | need to know |
| `chala` | very / a lot |
| `prathi okkati` | every single one |
| `motham ga` | overall / in total |
| `vachinappudu` | when (it/something) comes/arrives |
| `matrame` | only |
| `idi` / `adi` | this / that |
| `ela ante` | what that means is / here's how |
| `chivarga` | in the end / finally |
| `important ga` | importantly |

## Output structure

Produce a complete reference note — the goal is the user should walk away
knowing everything they need about the topic, not a highlight reel. Use
headings like this (adapt wording to the topic, keep the Tenglish voice in
the body text, not just the headings):

```markdown
# <Topic> Notes

## Idi Enti? (What is it)
Plain explanation of the concept, in Tenglish, assuming no prior context.

## Enduku / Eppudu Use Chestham (Why & when to use it)
The motivation — what problem it solves, when it's the right tool.

## Architecture / Ela Kattabadi Undi (How it's structured)
A diagram (Mermaid if it renders in the target surface, otherwise a clean
ASCII box-and-arrow diagram) showing the components/pieces and how they
relate. Label the diagram in English (component names) since diagrams read
better with plain technical labels; the surrounding prose explaining the
diagram is Tenglish.

## Working Flow (Step by step ela pani chestundi)
Walk through the actual sequence of what happens, step by step, end to end.
This is the "how it works in practice" section — trace a real run-through,
not just a bullet list of features.

## Examples
At least one concrete, worked example (code, config, a real scenario) with
Tenglish narration around it explaining what's happening and why.

## Gurthu Pettukovalsina Points (Key things to remember / gotchas)
The things that trip people up, edge cases, common mistakes.

## Summary
Short recap in Tenglish, tying it back to why it matters.
```

Skip or rename sections that genuinely don't apply (e.g. a pure concept with
no "architecture" won't need a component diagram — but for anything
system/tool/process-shaped, the diagram and working-flow sections are not
optional; that's usually exactly what the user is asking for).

## Worked micro-example (style calibration only, not a template to copy verbatim)

> **Idi Enti?**
> Caching ante, oka expensive computation result ni store chesi pettadam,
> next time same request vachinappudu malli calculate cheyakunda, aa stored
> value ne return cheyyadam. Ela ante — first time slow ga run avutundi,
> result ni cache lo pettestham, next time onwards fast ga serve avutundi.
> Idi especially useful — computation cost high ga undi, but input data
> frequently change avvani cases lo.

That block above is the calibration target: plain Roman letters throughout,
English nouns (caching, computation, cache, input data) left as-is, Telugu
carrying the verbs and logic, no parenthetical glosses anywhere.

## When the user's ask is ambiguous

If they just say "notes on X" without mentioning Tenglish, use normal
English — only switch to this style when they say something like "telugu
english mix", "tenglish", "telugu la", or they've been asking in this style
during the conversation already. If unsure whether a past note should be
redone in this style, ask rather than guessing.
