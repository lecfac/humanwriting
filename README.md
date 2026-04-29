# Human-Sounding ChatGPT: Custom Instructions Against AI Writing Tells

A ready-to-use custom instructions prompt for ChatGPT, built directly from Wikipedia's exhaustive [Signs of AI Writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) guide. Paste it in. Get prose that doesn't read like a press release written by a committee of language models.

## Why This Exists

AI writing has tells. Not because the models are bad — they're remarkably capable — but because they're trained to be agreeable, comprehensive, and safe, and those instincts produce a recognizable style: hedged, over-structured, rhythmically flat, and padded with words like *delve*, *tapestry*, and *it's worth noting that*.

Wikipedia's editor community has been cataloguing these patterns for years, flagging AI-generated submissions across thousands of articles. Their "Signs of AI Writing" page — nearly 15,000 words at last count — is the most thorough public field guide to machine-generated prose that exists. It's written for editors trying to detect undisclosed AI content, but it's equally useful as a checklist for anyone trying to *avoid* those patterns in their own AI-assisted writing.

This repo turns that checklist into a single, pasteable custom instructions block. The goal is simple: if you're going to use ChatGPT to write or help you write, the output shouldn't announce itself.

## What the Instructions Cover

The prompt targets six categories of AI writing behavior identified in the Wikipedia guide:

### 1. Hollow openers and filler affirmations

AI models are trained to be helpful and agreeable, which produces a tic of opening responses with "Great question!", "Certainly!", or "Absolutely!" before saying anything of substance. The instructions kill this pattern at the root.

### 2. Banned vocabulary

A specific list of words that LLMs reach for disproportionately:

> delve, intricate, tapestry, pivotal, underscore, landscape, foster, testament, enhance, crucial, transformative, groundbreaking, innovative, comprehensive, nuanced, multifaceted, paramount, invaluable, beacon, realm, elevate

These aren't bad words — they're just exhausted from overuse by models that treat them as "elevated" synonyms.

### 3. Structural clichés

Three patterns so common they've become synonymous with AI prose:

- **Negative parallelisms** — "It's not X, it's Y." / "Not only X, but also Y." Constructed contrasts that challenge a misconception the reader never held.
- **Rule of threes** — Adjectives and benefits listed in triplets regardless of whether the content actually has three parts. "Innovative, transformative, and groundbreaking."
- **Em-dash overuse** — The em dash deployed for punchy emphasis where a comma would do—exactly like this—creating a breathless, faux-urgent cadence.

### 4. Formatting overkill

Excessive bolding of key terms, bullet-point fragmentation of ideas that should flow as prose, and summary sections that restate everything already said. AI tends to format as if every response is a textbook chapter.

### 5. Uniform hedging and over-caution

LLMs are trained to be harmless, which produces a flattened, uniform level of caution across all claims regardless of how certain or uncertain they actually are. The instructions push toward context-appropriate confidence: direct when the evidence supports it, honest about uncertainty when it doesn't.

### 6. Vagueness and lack of friction

AI writing tends to overgeneralize ("researchers suggest," "many experts believe"), skip over difficulty, and sanitize complexity. The instructions push toward specific examples, named sources, and acknowledgment of what's actually hard or contested.

## How to Use It

### In ChatGPT

1. Go to **Settings → Personalization → Custom Instructions**
2. In the *"How would you like ChatGPT to respond?"* field, paste the contents of [`instructions.md`](./instructions.md)
3. Save. The instructions apply to all new conversations by default.

> **Note:** ChatGPT's custom instructions field has a character limit (~1,500 characters per field). If the full prompt exceeds it, use the condensed version in [`instructions-short.md`](./instructions-short.md).

### As a System Prompt (API / Other Platforms)

Paste the instructions as your system prompt in any OpenAI API call, or in the system prompt field of any platform that supports it (Cursor, Continue, Open WebUI, etc.). The instructions are model-agnostic and work with any sufficiently capable LLM.

### Mixing with Other Instructions

If you already have custom instructions set up, add the contents of `instructions.md` below your existing text rather than replacing it. The anti-AI-writing rules are additive and don't conflict with task-specific or persona-specific instructions.

## What This Is Not

This prompt does not make ChatGPT pretend to be human or suppress its disclosure that it's an AI. It doesn't kill useful formatting when formatting genuinely helps — a code block is still a code block. It doesn't demand false informality or force colloquialisms onto technical writing. The goal is prose that is direct, specific, varied, and honest — not prose that performs a caricature of casual human writing.

It also isn't a silver bullet. Custom instructions shift tendencies, not absolutes. LLMs are probabilistic; the same prompt can produce different output on different runs. Think of this as turning a dial, not flipping a switch. You'll still need to read what comes out.

## Sources

- **Wikipedia: Signs of AI Writing**  
  https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing  
  The primary source. A collaboratively maintained field guide by Wikipedia's editor community, documenting AI writing patterns observed across thousands of submissions.

- **Beutler Ink: How to Spot AI Writing, According to Wikipedia**  
  https://www.beutlerink.com/blog/how-to-spot-ai-writing  
  A distillation of the Wikipedia guide into seven patterns most recognizable in a business context.

- **Medium / Bootcamp: Wikipedia Just Published a List of AI Writing Tells**  
  https://medium.com/design-bootcamp/wikipedia-just-published-a-list-of-ai-writing-tells-heres-what-you-need-to-know-e397eccdcb3f  
  Additional synthesis with practical fix-it framing for workplace writing.

## Contributing

Pull requests are welcome. If you've identified an AI writing pattern not covered by the current prompt, open an issue with:

- A description of the pattern
- One or two real-world examples of it appearing in AI output
- A proposed instruction line or block to address it

The goal is to keep the prompt tight and pasteable. Resist the urge to add patterns that are rare, context-specific, or already covered implicitly. Quality over comprehensiveness.

Bug reports on instructions that produce unintended side-effects (e.g., suppressing genuinely useful formatting) are equally welcome.

## License

This project is released under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

[![CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

You are free to:

- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, including commercially

Under the following terms:

- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

Full license text: https://creativecommons.org/licenses/by/4.0/

### Note on Upstream Licensing

The patterns documented in the instructions are derived from Wikipedia's "Signs of AI Writing" page, which is released under the [Creative Commons Attribution-ShareAlike 4.0 License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

The ShareAlike clause requires that derivative works be distributed under the same or a compatible license. Users who adapt or redistribute content from this repo that is substantially derived from the Wikipedia source material should comply with CC BY-SA 4.0 terms accordingly.

---

*Wikipedia's Signs of AI Writing page is a living document maintained by volunteer editors and updated continuously. The patterns described here reflect the guide as of early 2026. Check the [source page](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) periodically for new additions.*
