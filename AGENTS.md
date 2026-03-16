# AGENTS.md — Badi Bakhar Org Baseline

> These are org-level AI instructions. They apply as a baseline to all repositories
> in the `badi-bakhar` GitHub organization. Repo-level `AGENTS.md` files extend these.

---

## Org Identity

**Badi Bakhar** (بڑی بکھار) — The Great Granary.
A personal AI-native knowledge OS. One owner. One granary. Everything in its place.

This org exists to support a single system: capturing, processing, and storing
knowledge from everyday sources — WhatsApp, YouTube, Instagram, the web, and manual input.

---

## File Naming Convention

All note files across all repos follow this pattern:

```
YYYY-MM-DD-ascii-lowercase-slug.md
```

- Date prefix always `YYYY-MM-DD`
- Slug: ASCII/Latin only — never Devanagari or Urdu script in filenames
- All lowercase, hyphen-separated
- Extension always `.md`

For Hindi/Urdu titles, romanize the slug: "سوال" → `soal`, "چاय" → `chai`

---

## Language Rules

| Context | Rule |
|---------|------|
| Filenames | ASCII/Latin only, lowercase, hyphenated |
| Frontmatter keys | Always English |
| Frontmatter values | Always English (`source`, `status`, `lang`, `tags`) |
| Note bodies | Any language freely — English, Hindi, Urdu, Hinglish |
| Tags | English or romanized Hindi — no Devanagari script |
| Title field | Any language (human-readable) |

Never translate note bodies. Preserve original language exactly as written.

---

## Infrastructure Conventions

All repos in this org use:

- **AI Provider:** Amazon Bedrock, region `ap-south-1`
- **Config file:** `opencode.json` at repo root — always present, never commit secrets
- **Credentials:** AWS profile references only — never hardcode access keys or secrets
- **GitHub Actions:** OpenCode workflow via `.github/workflows/opencode.yml`

---

## Cross-Repo Rules

- Do not reference files from other repos without explicit full paths
- Do not assume directory structure from another repo exists locally
- Each repo is self-contained — all context it needs lives within it

---

## Security Rules

- **Never commit AWS credentials** (access keys, secret keys, session tokens)
- Always use AWS profile references in `opencode.json`
- `.env` files must be in `.gitignore` — never commit them
- No secrets in commit messages, PR descriptions, or comments

---

## AI Behavior Baseline

- Never delete files — use `status: archived` or move to archive
- Confirm before moving files out of `inbox/`
- Preserve original language in note bodies — do not translate
- Surface ambiguity rather than guess — ask when intent is unclear
- Prefer doing less and confirming over doing more and being wrong

---

*Org baseline. Repo-level AGENTS.md files take precedence where they conflict.*
