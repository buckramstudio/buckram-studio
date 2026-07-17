<p align="center">
  <img src="media/avatar.gif" alt="Buckram Studio" width="128" height="128" />
</p>

<h1 align="center">Buckram Studio</h1>

<p align="center">
  <em>Guided book writing studio — setup, plan rooms, draft, editorial pipelines.</em>
</p>

<p align="center">
  <a href="https://open-vsx.org/extension/buckram/buckram-studio">
    <img alt="Open VSX Version" src="https://img.shields.io/open-vsx/v/buckram/buckram-studio" /></a>
  <a href="https://open-vsx.org/extension/buckram/buckram-studio">
    <img alt="Open VSX Downloads" src="https://img.shields.io/open-vsx/dt/buckram/buckram-studio" /></a>
  <img alt="License: Proprietary" src="https://img.shields.io/badge/license-Proprietary-blue" />
  <img alt="Platform: Cursor" src="https://img.shields.io/badge/platform-Cursor-black" />
</p>

> **Stop copy-pasting your world bible into a blank prompt.**

Buckram Studio is a Cursor extension for the full novel lifecycle — from empty folder to final draft. It wraps professional book craft around plain Markdown on your disk, so AI works as a structured co-writer and multi-pass editorial engine instead of a chaotic blank chat. Your files stay where they belong: local, readable, and yours.

<!-- TODO: produce media/readme/hero.gif — main demo loop: Work Tree -> Chat about -> draft appears (~1200px wide, < ~8 MB) -->
<p align="center">
  <img src="media/readme/hero.gif" alt="Buckram Studio in action" width="820" />
</p>

_Buckram Studio is for writers, not engineers._

---

## Why writers want it

- **One clear next step** — The Work Tree shows your book as stages: canon, outlines, drafts, post-production. You always know what to open next.
- **Canon that sticks** — Personas, world bible, and style rules feed every **Chat about** and draft, so you stop pasting the same world rules into every prompt.
- **Edit safely** — Multi-pass editorial pipelines run on a test sample first. Real chapter drafts change only when you choose to run production.
- **Your files, always** — Plain Markdown on _your_ disk. Buckram never stores your manuscript in the cloud; uninstall or leave Premium and every file stays readable and yours.

---

## What you get

- **Work Tree** — Command center for canon, books, chapters, scenes, pipelines, translations, export, and embedded docs. One obvious next action per row.
- **Canon & world-building** — Personas with voice profiles, world bible, stage/location bible, research vault, and a writing codex (glossary, motifs, clue ledger, relationship matrix, off-screen tracker).
- **Plan rooms & Director** — Chapter outlines with professional scene blocks, per-scene plan rooms, director slates, pacing/camera matrix, and beat-to-prose expansion.
- **Chat about** — Opens Cursor Agent chat with the right files already attached; you type first after **"Your turn."** Orchestrated runs end with **"Press Enter to start"** and never auto-spend without confirmation.
- **Editorial pipelines** — Author multi-pass post-production packs, test them on a sandbox sample, then run on real chapters when you are ready. Batch plans for multi-chapter runs.
- **Continuity intelligence** — Presence dashboard, clue ledger, and off-screen tracking flag forgotten personas, unpaid clues, and stale threads — no LLM tokens required.
- **Context compression** — Smart briefing (Eco / Pro) with scene census routing, so the model gets what a chapter needs instead of the whole series bible every click.
- **Craft floor** — Anti-slop rules, forbidden-phrase and gesture squiggles, and per-persona humanization keep the prose in your voice, not a generic AI one.
- **Export** — KDP-ready DOCX, Markdown, and PDF out of the box; EPUB via Pandoc (enhanced).

---

## Screenshots

| Work Tree | Get Started |
|-----------|-------------|
| <img src="media/readme/work-tree.png" alt="Work Tree sidebar" width="420" /> | <img src="media/readme/get-started.png" alt="Get Started panel" width="420" /> |

| World bible & canon | Cast |
|---------------------|------|
| <img src="media/readme/canon-world.png" alt="World bible and canon" width="420" /> | <img src="media/readme/cast.png" alt="Cast and personas roster" width="420" /> |

| Outline & Director | Chat about |
|--------------------|------------|
| <img src="media/readme/outline-director.png" alt="Chapter outline with scene blocks and director slate" width="420" /> | <img src="media/readme/chat-about.png" alt="Chat about opens Agent chat with context" width="420" /> |

| Post-production (Testing) | Context compression |
|---------------------------|---------------------|
| <img src="media/readme/pipelines-testing.png" alt="Pipelines panel testing sandbox" width="420" /> | <img src="media/readme/context-compression.png" alt="Context compression Eco/Pro settings" width="420" /> |

| Presence dashboard | Export |
|--------------------|--------|
| <img src="media/readme/presence-dashboard.png" alt="Presence dashboard continuity intelligence" width="420" /> | <img src="media/readme/export.png" alt="Export book wizard: DOCX, Markdown, PDF, EPUB" width="420" /> |

---

## Getting started

1. Open **Cursor**.
2. Install **Buckram Studio** from the Extensions view (Cursor uses [Open VSX](https://open-vsx.org/extension/buckram/buckram-studio)).
3. Open a folder for your series or book, then click the **book icon** in the Explorer to open the Work Tree.
4. Use **Get Started** to create a new series, a standalone book, or add a book to a series, then follow the guided setup tour.

Full getting-started and feature help live inside the extension under **Work Tree → Documentation**.

---

## Free & Premium

Buckram charges for **automation scale, not access to your manuscript**. Your book stays as plain Markdown on your disk regardless of tier — files are never locked, deleted, or held hostage.

- **Free** — Work Tree, Chat about, canon, and craft floor; unlimited pipeline authoring; the **Testing** sandbox (max 5 starts/hour per pipeline or test batch, then a 3-hour cooldown); a **50,000-word** cap on manuscript drafts; export up to **2 chapters** per run.
- **Premium** — Chapter and batch production runs, execution plans, full-book export, unlimited words, and unlimited Testing.
- **Bring your own key** — LLM usage runs through your Cursor Agent, so you pay your provider directly. Buckram never bills for tokens or meters your writing.

---

## Requirements

- **Cursor** — **Chat about** and orchestrated runs use Cursor's Agent chat (not available in plain VS Code).
- **Zero setup for the basics** — A marketplace install works with **no Python, pip, LibreOffice, or Pandoc**. Work Tree, Chat about, bundled pipelines, and DOCX / Markdown / PDF export all run on the extension's own Node runtime.
- **Optional (enhanced)** — EPUB export uses **Pandoc**; DeepL translation packs use a **DeepL API key** (via Settings → BYOK). Both are clearly labeled and never block core features.

---

## Extension settings

Configure these under **Settings → Extensions → Buckram Studio** (search `buckramStudio`):

- `buckramStudio.changeHistory.mode` — How change history is recorded on disk: on `save`, on an `interval`, or `gitOnly` (never sent to the LLM).
- `buckramStudio.premium.freeWordLimit` — Free-tier manuscript word cap (default `50000`).
- `buckramStudio.proseLint.enabled` — Show squiggles for forbidden phrases and gesture-cooldown violations in manuscripts.
- `buckramStudio.canonLinks.enabled` — Ctrl+click canon anchors in prose to open persona, stage, or setting files.
- `buckramStudio.workTree.autoRefresh` — Refresh the Work Tree when chapters, drafts, plans, or codex files are created or removed.
- `buckramStudio.byok.deeplPlan` — Which DeepL endpoint to use (`free` or `pro`) for DeepL translation packs.

The full list of settings is available in the Cursor settings UI under **Buckram Studio**.

---

## Getting the most from chat

Chat models only "see" a fixed desk each turn. Chapter work piles the _same_ pages again and again, so answers go soft, lose your voice, or loop in circles when that desk fills with near-copies. That is how the models work (attention math), not a Buckram limit and not you asking wrong. Inside the extension, open **Documentation → Read me first → How chat context works** (and _Getting the most from the context window_) for a short mental model and habits that keep Agent chats sharp.

---

## Known limitations

- Requires Cursor; plain VS Code lacks the Agent chat that **Chat about** and orchestrated runs depend on.
- EPUB export and DeepL translation are optional enhanced paths (Pandoc / DeepL key); core export is DOCX, Markdown, and PDF.
- On the Free tier, chapter and batch **production** runs are Premium; use the **Testing** sandbox for safe runs.

---

## License

Proprietary — see [LICENSE](LICENSE). Your books and other output remain yours, as plain files on your disk.
