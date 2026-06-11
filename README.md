<!--
  README for codyhxyz/stack — software I reach for daily.
  linked from github.com/codyhxyz/codyhxyz.
-->

# 🧰 cody's stack

awesome software i think more people should be aware of

*last updated 6/11/26*

**legend:**

| icon | meaning |
|------|---------|
| 🌐 | open-source |
| 🍋 | made by me |

---

## core software

- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=raycast.com&sz=64"/> **[Raycast](https://raycast.com)**: launcher / clipboard / window manager. Spotlight replacement.
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=cap.so&sz=64"/> **[Cap](https://cap.so)**: open-source Loom replacement. screen recording with shareable links. 🌐
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=github.com&sz=64"/> **[Muesli](https://github.com/pHequals7/muesli)**: WisprFlow + Granola in one. local voice dictation + meeting transcription on Apple Silicon. 🌐

---

## AI

- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=claude.com&sz=64"/> **[Claude Code](https://github.com/anthropics/claude-code)**: my primary interface for thinking with my computer.
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=pi.ai&sz=64"/> **[Pi](https://pi.ai)**

### Models

- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=deepseek.com&sz=64"/> **[DeepSeek V4 Pro](https://api-docs.deepseek.com/quick_start/pricing)** — **daily driver**: $0.435 / M input tokens, $0.87 / M output tokens (permanent 75% price cut, effective 2026-05-31, settling at 25% of the original rate). long-context inference at ~1/4 the compute and ~1/10 the memory footprint of its predecessor — that's why the cut is permanent rather than promotional.
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=ai.google.dev&sz=64"/> **[Gemini Flash 3.5](https://ai.google.dev/gemini-api/docs/pricing)** — **latency-dependent sessions**: $1.50 / M input tokens, $9.00 / M output tokens (cached input $0.15 / M). reach for it when round-trip time matters more than per-token cost.

---

## add-ons

*things that augment existing software rather than standing on their own.*

### Claude Code
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=github.com&sz=64"/> **[skills](https://github.com/codyhxyz/skills)**: my cognitive heuristics. the ways I talk to my computer. 🌐 🍋

### YouTube
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://github.com/user-attachments/assets/b0588941-61c1-48bc-8ca5-5c3754f27dca"/> **[YouTube Playlist Search](https://github.com/codyhxyz/playlist-search-extension)**: filter bar for YouTube's save-to-playlist dialog. bypasses the 200-playlist cap. 🌐 🍋

### Spotify
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="A-orb-128" src="https://github.com/user-attachments/assets/6b6ac4a6-645c-4208-84c0-c870d1cba97b"/> **[Spotify Notes](https://github.com/codyhxyz/spotify-notes)**: take notes on songs as you listen. for DJ library curation. 🌐 🍋

---

## building your own bespoke software

- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=github.com&sz=64"/> **[create-claude-plugin](https://github.com/codyhxyz/create-claude-plugin)**: end-to-end scaffold for building & publishing Claude Code plugins. 🌐 🍋
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=github.com&sz=64"/> **[create-chrome-extension](https://github.com/codyhxyz/create-chrome-extension)**: end-to-end scaffold for building & publishing Chrome extensions. 🌐 🍋
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=github.com&sz=64"/> **create** *(in development)*: scaffold to build anything in a self-consistent manner across projects. 🌐 🍋

---


## architecture

*chosen architecture — 2026.*

- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=astral.sh&sz=64"/> **[uv](https://github.com/astral-sh/uv)**: Python package & project manager, written in Rust. 10–100× faster than pip. 🌐
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=bun.sh&sz=64"/> **[bun](https://github.com/oven-sh/bun)**: JavaScript runtime, bundler, test runner & package manager in one. 🌐
- **Compute**: Hetzner CCX13 + Coolify (~$15/mo) → Render ($100–300/mo) → AWS / GCP managed ($1k+/mo, compliance)
- **Database**: Neon free / Postgres-on-Coolify ($0) → Neon Launch ($19/mo) → Neon Scale ($69+/mo)
- **Object storage**: Cloudflare R2 ($0.015/GB, zero egress)
- **Edge — CDN / DNS / WAF / DDoS**: Cloudflare free ($0) → Cloudflare Pro ($25/mo)
- **Frontend hosting**: Vercel free ($0) → Vercel Pro ($20/mo) → Cloudflare Workers + OpenNext (once Vercel bills exceed $200/mo)
- **Auth**: Neon Auth
- **Email**: Resend free (3k/mo) → Resend Pro ($20/mo)
- **AI inference**: OpenRouter as gateway — Groq / Cerebras for raw TPS, DeepSeek V4-Pro for pareto-curve intelligence
- **Monitoring / uptime**: BetterStack free (10 monitors + status page) → BetterStack paid ($21–29/mo)
- **Error tracking**: PostHog Error Tracking (free, 100k errors/mo) → PostHog Cloud (usage-based)
- **Product analytics**: PostHog self-hosted on Coolify (free) → PostHog Cloud (1M events free)
- **Background jobs / queues**: pg-boss / Graphile Worker ($0, Postgres-backed) → Trigger.dev v3 ($10/mo, Apache 2.0)
- **Vector embeddings** (AI-native only): pgvector on Postgres ($0, up to ~10M vectors) → Turbopuffer / Cloudflare Vectorize (scale)
- **Payments**: Stripe
- **CI/CD**: GitHub Actions hosted → self-hosted runner on existing Hetzner box

---

## knowledge tools

- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=annas-archive.org&sz=64"/> **[Anna's Archive](https://en.wikipedia.org/wiki/Anna%27s_Archive)**: free ebooks. the largest shadow library in existence.
- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=github.com&sz=64"/> **[Web Annotator]([https://github.com/codyhxyz/web-annotator](https://chromewebstore.google.com/detail/page-marker-draw-on-web/jfiihjeimjpkpoaekpdpllpaeichkiod/reviews))**: take notes on what you read, or remind yourself what you need to do on the page.

---

## see also

- <img style="display:inline-block;width:20px;height:20px;vertical-align:middle;margin-bottom:4px;pointer-events:none;" alt="" src="https://www.google.com/s2/favicons?domain=gist.github.com&sz=64"/> **[distbit0's stack](https://gist.github.com/distbit0/6df6026cf7285b481dcd723a65192eb8)**: a friend's list — notes/zettelkasten, reading & research, and anti-distraction tooling.

---

<sub>Suggestions welcome.</sub>

<div align="center">

[![🍋 make a suggestion](https://img.shields.io/badge/🍋_make_a_suggestion-FBBF24?style=for-the-badge&logoColor=000)](https://github.com/codyhxyz/stack/issues/new)

</div>
