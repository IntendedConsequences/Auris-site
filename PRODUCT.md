# Auris — Product context

## What it is

Voice-to-text for Mac and Windows. Hold a hotkey, speak, release. Clean text lands at your cursor in any app, in your voice, polished by an LLM you control.

## Register

Brand. This is a marketing site (`auris.talk`) for an indie desktop product. Design IS the product surface here — every section sells.

## Users

Knowledge workers who type all day and want speech to do the heavy lifting:
- Writers and editors composing prose
- Engineers writing prompts, comments, commits, Slack
- People with RSI or hand pain who need an alternative to typing
- Bilingual users switching language per app (English in Slack, Spanish in Notes, etc.)
- Privacy-leaning professionals who want either BYOK cloud OR fully on-device

Not enterprise IT. Not mass-market consumers. Solo professionals and small teams who pick their own tools.

## What it does (the short version)

1. Whisper transcribes the audio.
2. An LLM polishes the transcript (fixes fillers, grammar, punctuation, tone).
3. Auris types the result at the user's cursor in whatever app is in focus.

Differentiators that aren't theoretical:
- **BYOK.** User brings their own Anthropic / OpenAI / Groq key, or runs Ollama/llama.cpp/LM Studio locally. Auris doesn't proxy keys or charge per minute.
- **Or fully local.** Whisper-local for STT + Ollama for polish = zero outbound network.
- **One-time license, no subscription.** $49 founder / $79 standard / $29 student. 30-day money back.
- **App-aware modes.** Per-app overrides for tone, format, language, plus freeform custom rules.
- **Privacy patterns.** Built-in regex for email, phone, SSN, credit card, plus custom — matched dictations skip history.
- **Dictionary auto-learn.** Watches user edits and clipboard rewrites to silently fix recurring transcription mistakes.
- **Memos as real .md files** on disk in `memos/`. Sync via Dropbox, git, iCloud.
- **Snippets** on spoken triggers with variables (`{date}`, `{clipboard}`).
- **Em-dashes off by default** — Anthropic models love them, most users don't.

## Status

Pre-launch beta. Hero CTA is email-capture for the launch alert (not a buy button yet). Buyer-facing pricing page is live but no checkout. Today is 2026-05-19.

## Tone & voice

- Editorial, not SaaS. Plain language. Punchy short sentences.
- No marketing hyperbole, no rocket emoji, no "AI-powered" anywhere.
- Specific numbers over hand-waving (160 wpm speaking vs 65 wpm typing).
- Confident but not chest-thumping. The product is the argument.
- **No em-dashes** (their own product strips them; the site does too). Use commas, colons, semicolons, periods, parentheses.

## Anti-references

What Auris is NOT trying to look like:
- Generic SaaS landing (centered hero + 3 feature cards + pricing + testimonials carousel).
- Gradient mesh / glass / blur "premium" aesthetic.
- Loud crypto / AI-tool neon.
- Apple-clone monochrome white.
- Subscription-funnel pages with "$X/mo" social-proof spam.

What it IS trying to look like:
- Editorial / publication: warm dark paper, generous type, working diagrams, restrained use of one signal color.
- Spec-sheet honest: real numbers, real keyboard shortcuts, real screenshots, no stock illustration.

## Competitors worth referencing

- **Resonant (onresonant.com)** — newer competitor, visually polished, "voice suite" positioning. Dictation + meeting transcription, cloud-or-local, subscription. Wins on: hero clarity, named-customer social proof, integration logo row. Loses on: subscription, no BYOK, no fully-local polish, less differentiated pricing.
- **Wispr Flow, Whisper Memos, Aiko, MacWhisper, SuperWhisper** — adjacent. Most are Mac-only and/or transcription-only without per-app tone/format polish.

## Strategic principles for the site

1. **Wedge first.** "$49 once" + "BYOK" + "fully local option" are the real differentiators against Resonant and the subscription pack. They must be visible in the first scroll.
2. **Show the product, don't only describe it.** Real HUD / settings screenshots from `assets/screenshots/` over abstract illustration.
3. **Integration anchors.** Slack / Gmail / Notion / ChatGPT / Cursor / Claude / VS Code logos as a visual answer to "does it work with my stack."
4. **No buyer-funnel theater.** Pre-launch CTA is honest ("get the launch alert"). Don't fake urgency or scarcity.
