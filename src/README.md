# `src/` — TIA Portal Project Archive

This folder contains the **TIA Portal V19 project archive (`.zap19`)** that holds all
Function Blocks (FB) and Functions (FC) under development for the WECS MNS.

There is currently **one** `.zap19` file in this folder. Subfolders or split archives
may be introduced later if scope grows.

## File Naming Convention
WECS_MNS_FBFC_v<Major>.<Minor>.zap19
- `<Major>.<Minor>` — Internal version of the development snapshot, independent
  from Git tags. Bump `<Minor>` for routine updates and `<Major>` for milestone
  reviews delivered to NKT.

### Example

| Filename                          | Note                          |
|-----------------------------------|-------------------------------|
| `WECS_MNS_FB_v0.1.zap19`        | First snapshot for NKT review |

> Keep the same filename across revisions of the same version. Bump the version
> in the filename only when delivering a reviewable milestone, so that Git
> history (commits) and version history (filenames) stay readable.

## How to Update the Archive

1. In TIA Portal V19, open the live project.
2. *Project → Archive…* → choose **Archive as compressed file (`*.zap19`)**.
3. Save it over the existing `.zap19` in this folder (same filename), unless
   bumping to a new version per the rule above.
4. `git add src/*.zap19`
5. Commit with a message that lists the affected FB/FC, for example:
update: FB_InterlinkMaster, SafeFB_EmergencyStopChain
6. Update `CHANGELOG.md` with the same details.

## Why a Single `.zap19` Instead of Per-Block Exports

- Preserves cross-references, tags, HMI links, and safety program structure
  that get lost when exporting individual blocks.
- Matches the way the project is actually developed and delivered to NKT.
- Trade-off: Git cannot diff binary archives. The commit message and
  `CHANGELOG.md` are the source of truth for what changed.

## Reviewing the Archive

Reviewers should:

1. Pull the latest `main` (or the specific branch under review).
2. Open the `.zap19` in TIA Portal V19 (*Project → Retrieve…*).
3. Cross-reference the changed FB/FC against the relevant `CHANGELOG.md` entry
   and commit message.