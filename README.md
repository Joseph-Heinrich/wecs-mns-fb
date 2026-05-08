# WECS-MNS-FBFC

Repository for **development-stage Function Blocks (FB) and Functions (FC)** of the WECS Submarine Cable Factory Machine Network System (MNS).

---

## Purpose

This repository hosts the PLC logic blocks under active development for the WECS subsea cable production lines.
Its primary audience is **NKT and the safety consultant (Mr. Jonas S.)**, for review of:

- Functional logic of interlink operations between equipment.
- Compliance progress against **ISO 13849-1:2023** safety functions (Control On, Operation Mode, etc.).
- Iterative changes during commissioning and integration with Cosin (MNS supplier) and other equipment vendors.

> **Note:** This repository contains **development-stage** code only. It is **not** the production-released library, and blocks here are subject to change without prior notice. Released versions will be tagged.

---

## Scope

- **Platform:** Siemens TIA Portal **V19**
- **Distribution format:** Full project archive (`.zap19`)
- **Languages used inside the project:**
  - Safety FB/FC → **LAD** only
  - Non-safety FB/FC → **LAD** and **SCL**
- **Standards referenced:**
  - ISO 13849-1:2023 / ISO 13849-2:2012
  - EN ISO 12100:2010
  - EN ISO 14118:2018
  - EN 619:2022
  - EN 1114-1:2011

---

## Repository Structure
WECS-MNS-FBFC/
├── README.md          # This file
├── CHANGELOG.md       # Version history (Keep a Changelog format)
├── .gitignore         # TIA Portal temp/lock + general ignore rules
└── src/
├── README.md      # File naming & archive handling notes
└── *.zap19        # TIA Portal V19 project archive(s)

The repository tracks the **TIA Portal project archive (`.zap19`)** directly. There is currently only one archive file under `src/`, which contains all FB/FC under development.

---

## Workflow

1. **Develop** the FB/FC inside TIA Portal V19.
2. **Archive** the project as `.zap19` via *Project → Archive…* in TIA Portal.
3. **Replace** the existing `.zap19` under `src/` with the new archive (keep the same filename so diffs stay clean).
4. **Commit** to a feature branch with a descriptive message.
5. **Open a pull request** for review by NKT / internal team.
6. **Merge** to `main` after approval and update `CHANGELOG.md`.

> Because `.zap19` is a binary archive, Git diffs cannot show logic changes directly. Always describe FB/FC-level changes in the commit message and in `CHANGELOG.md`.

---

## Branching Convention

| Branch         | Purpose                                              |
|----------------|------------------------------------------------------|
| `main`         | Reviewed, stable development snapshots               |
| `feature/<id>` | New FB/FC or significant logic changes               |
| `fix/<id>`     | Bug fixes on existing blocks                         |
| `safety/<id>`  | Safety-related changes (ISO 13849-1 compliance work) |

---

## Contact

| Role                        | Name           | Organization |
|-----------------------------|----------------|--------------|
| Automation Engineer (Owner) | Joseph         | WECS         |
| Safety Consultant           | Mr. Jonas S.   | NKT          |
| MNS Supplier                | —              | Cosin        |

---

## License

Internal use only. Not for public distribution.