# Rules for agents working in this repo

1. **Never edit anything under `skills/` here.** This repo is a BUILD OUTPUT. The golden copy
   lives in the monorepo at `md/cellcog/openclaw_skills/` — edit there, then run:
   ```bash
   python3 scripts/sync_skills.py --execute
   ```
2. The sync is a **pure copy + validation** (no content transformation). Skill files are
   universal: their install sections carry labeled lines for npx / OpenClaw / plugin / manual,
   and the reader self-selects. If a skill needs channel-specific content, fix the golden copy's
   wording — do not add transformation logic here.
3. `scripts/sync_skills.py --check` exits 1 if this repo has drifted from the golden copy.
   Run it before any release work.
4. The README catalog table is generated between the CATALOG markers by the sync script —
   never hand-edit it.
5. Naming invariant: folder name == frontmatter `name` == the ClawHub slug. Identical across
   all channels (ClawHub, skills.sh, the CellCog plugin). Never rename here.
