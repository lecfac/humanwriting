# humanwriting

AI writing is recognizable. Not because AI is bad at grammar or logic, but because it defaults to patterns that no human writer would choose — opener affirmations, noun-stack sentences, triplet lists, em-dash overuse, filler hedges, and a relentlessly smooth tone that flattens every topic to the same texture. After a while, the sameness is the tell.

This repo is a plain-language set of instructions you can paste into any AI system to push it away from those patterns. No model fine-tuning required. Just give the model better rules to write by.

---

## What's in this repo

`instructions.md` — a single file of writing rules organized into five areas: voice and tone, word choice, sentence rhythm, structure and formatting, and substance. The rules are specific, not vague. They name the patterns to avoid, give the reason, and show the fix.

The list draws on Wikipedia's documented signs of AI writing and extends it with practical guidance for getting cleaner output from any major model.

---

## How to use it

Copy the contents of `instructions.md` and paste them wherever your AI platform accepts persistent instructions or a system prompt:

- **ChatGPT** — Settings → Personalization → Custom Instructions
- **Claude** — Add to a Project's custom instructions, or paste into the system prompt of any API call
- **Gemini** — Paste at the top of a conversation, or use in a system instruction via the API
- **API / custom apps** — Drop the text into the system prompt before your user messages

You don't need to use every rule. If only certain sections are relevant to your use case, take those and leave the rest.

---

## Contributing

If you find a pattern that belongs on the list — something AI models reliably do that human writers don't — open an issue or a pull request. Keep proposed additions specific: name the pattern, explain why it's a problem, and describe the fix.

What doesn't belong here: rules that are just stylistic preferences with no connection to AI writing patterns, and rules so broad they'd apply to any writing guide.

---

## License and copyright

Copyright (C) 2026 lecfac

This project is licensed under the GNU General Public License v3.0. You are free to use, copy, modify, and distribute this work, provided that any modified versions carry the same license and make their source available.

See [LICENSE](LICENSE) for the full terms.

The goal of open-sourcing this is straightforward: AI writing patterns are a shared problem, and fixing them should be a shared effort. Anyone should be able to use these instructions, improve them, and pass the improvements on.
