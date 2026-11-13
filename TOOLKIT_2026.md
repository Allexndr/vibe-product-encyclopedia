# 🔥 Autumn 2026 Vibe-Coding & AI Engineering Toolkit

**[ 🇬🇧 English ](README.md)** • **[ 🇷🇺 Русский ](README.ru.md)** • **[ 🇰🇿 Қазақша ](README.kk.md)** • **[ 🇨🇳 简体中文 ](README.zh.md)** • **[ 🇪🇸 Español ](README.es.md)**

Curated, battle-tested open-source tools, agent configurations, and security checklists added in November 2026.

---

## 1. 🛡️ AppSec: Shannon AI Pentester & 12-Step Hardening Prompt

- **Shannon (`+48K⭐` Open Source AI Pentester):** Instead of "deploy and pray", give Shannon your app-it attacks like a real hacker, executes real exploits (*no exploit = no report*), and outputs PDF + SARIF reports.
- **`cloudflare/security-audit-skill`:** Official Cloudflare security audit skill (`github.com/cloudflare/security-audit-skill`).

### 12-Step Website Security Hardening Prompt (Copy & Run in Claude/Codex)
```text
Perform a full security audit of my website and implement all 12 defense layers:
1. Enforce Two-Factor Authentication (2FA).
2. Strip all API keys and secrets from client code and git history (.env only).
3. Enforce HTTPS (HSTS + Secure Cookies).
4. Lock database ports (bind 127.0.0.1:5432:5432 in Docker, block 0.0.0.0).
5. Store passwords ONLY as cryptographic hashes (Argon2id / bcrypt).
6. Log suspicious logins, failed attempts, and anomalies.
7. Implement strict server-side form & DTO validation (Zod .strict()).
8. Add XSS, CSRF, and injection defenses (CSP headers + sanitization).
9. Lock down the admin panel (dedicated auth + role/IP allowlist).
10. Add Rate Limiting on all public and auth endpoints.
11. Restrict allowed MIME types, extensions, and max file upload sizes.
12. Write and run automated penetration/security tests verifying all defenses.
```

---

## 2. 🎨 Anti-AI-Slop Visual Engineering & Cross-Agent Asset Generation

- **Impeccable (`npx impeccable detect <url>`):** 62 deterministic rules (zero AI keys required) catching generic AI-slop tells (low contrast, card-in-card nesting, purple SaaS clichés) before client handoff. Agent commands: `critique`, `polish`, `bolder`.
- **Claude + Codex Image Synergy:** Claude Code cannot natively generate raster mockups, while Codex on the entry tier can. Wrap Codex CLI as a local Skill inside Claude Code so Claude delegates UI concept & asset generation automatically.
- **Curated AI Design References:**
  - `studio.motionsites.ai` - fast motion sites (cheaper than Lovable)
  - `motionsites.ai` - 800+ prompts for 3D, animations, and dynamic sections
  - `land-book.com`, `recent.design`, `landdding.com` - landing page inspiration
  - `devault-ascii.pages.dev/ascii-generator/app/` - ASCII art generator for CLI & READMEs

---

## 3. ⚡ Token Economy & Clean Git Configs

### Remove `"Co-authored-by: Claude"` from Git Commits & PRs
Add to `~/.claude/settings.json`:
```json
{
  "attribution": {
    "commit": "",
    "pr": ""
  },
  "includeCoAuthoredBy": false
}
```

### 50% Context Hook (Codex / Claude)
- **Why:** Smaller context windows (e.g., 373K vs 1M) degrade rapidly past 50% fill, burning weekly limits and causing circular loops.
- **Fix:** Trigger a hook at **45–50% context** that serializes current state, architectural decisions, and next steps into `HANDOFF.md`, then continue in a fresh session (reduces daily limit burn to ~14%).

---

## 4. 🤖 Agentic Web, GEO/AEO & Memory

- **`claude-seo` (`github.com/AgriciDaniel/claude-seo`):** SEO for AI bots (ChatGPT, Perplexity, AI Overviews): `/llms.txt`, `Content-Signal` in `robots.txt` (*allow indexing, disallow training*), and `citability` audits.
- **Lightpanda Browser (`github.com/lightpanda-io/browser`):** Headless browser built from scratch for AI agents - **16x lighter and 9x faster than Chromium**.
- **Mika (`github.com/wangzan101/Mika`):** Autonomous Android UI agent operating any app/site without APIs on a hidden background screen.
- **Memorilla (`github.com/snap-stanford/memorilla`):** Stanford agent long-term memory architecture.
- **`ALNIuser/agency-agents` & `lemomo-ai/lemo-opuscar`:** Multi-agent orchestration frameworks.

---

## 5. 🎬 3D, Video Production, Voice & GameDev Pipelines

- **AI 3D Animation Pipeline:** `Claude (Director Spec) → Claude Code + Blender MCP (Python scene) → Poly Haven (lighting & PBR textures) → Remotion (composition) → FFmpeg (export)`.
- **AI Video & Shorts:** `kurbaitaev/ghost-editor`, `kajisho5/ffmpeg-skill`, `AgriciDaniel/claude-shorts`, `calesthio/OpenMontage`, `Autom8AI/Open-Higgsfield-AI`.
- **Programmatic Pixel VFX (`github.com/patch-gg/pixelfx`):** 244 procedural pixel effects (fire, lightning, magic, weather) drawn purely in code with Godot/Unity sprite-sheet export + Claude Code skill. *Workflow: generate 5–10 variants → inspect → pick → refine.*
- **Open-Source Character Animation (Viggle alternatives):** `Tencent/MimicMotion`, `Francis-Rings/StableAnimator` (less face drift), `TMElyralab/MusePose` (MIT).
- **Aura Autopilot:** AI playtester for Unreal Engine, Unity, and Godot.
- **VoxCPM2:** Open-source 2B-parameter TTS supporting 30 languages (including Russian) and voice cloning.
- **Local GPU Unlock (`github.com/zagitta/gpu-unlock`):** Unlocks factory compute caps on NVIDIA RTX 20/30/40 while preserving thermal & power protections.
- **Anthropic Startup Program:** `claude.com/programs/startups`.
