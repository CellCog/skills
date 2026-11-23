# Rules for agents working in this repo

1. **Never edit anything here.** This repository is published from CellCog's own source by a release, and the next
   release overwrites every change made here (a commit or a pull request). To report a problem or ask for a change in
   a skill, open an issue instead; the fix reaches this repository with the next release.
2. Skill files are published verbatim: their install sections carry labeled lines for npx / OpenClaw / plugin /
   manual, and the reader self-selects.
3. The README catalog table between the CATALOG markers is generated from each skill's `description` at every
   release. Never hand-edit it.
4. Naming invariant: folder name == frontmatter `name` == the ClawHub slug. Identical across all channels (ClawHub,
   skills.sh, the CellCog plugin).
