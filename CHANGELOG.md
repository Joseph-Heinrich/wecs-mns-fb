# Changelog

All notable changes to FB/FC blocks in this repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)
where applicable for tagged releases.

Because the tracked artifact is a binary `.zap19` archive, every change entry
should explicitly state which FB/FC are affected so reviewers can locate them
inside the TIA Portal project after extracting the archive.

---

## [0.1.0] - 2026-05-08

### Added
- Initial repository structure.
- First `.zap19` archive of the development project (placeholder; replace on first commit).

### Changed
- `OM18MplcNonSafety`: MPLC non safety logic, located in _MPLC. Added start / stop logic. Not added to any program cycle yet.
- `OM18MachineNonSafety`: Machine PLC non safety logic, located in Front Machine 1. Added start / stop logic. Not added to any program cycle yet.
- Structural change for the local MPLC method. Attempt to fix the unclear direction in the program according to NKT feedback.

### Safety
- `ModeCheck`: MPLC safety logic, located in _MPLC. Added logic to determine which mode the machine is in. Not added to safety program yet.

---

<!--
Template for future entries:

## [x.y.z] - YYYY-MM-DD

### Added
- New FB/FC: `FB_<Name>` — short description.

### Changed
- `FB_<Name>`: behavior change description, reason.

### Fixed
- `FB_<Name>`: bug description, fix summary.

### Safety
- `FB_<Name>`: ISO 13849-1 related update (PL, category, etc.).

### Removed
- Deprecated blocks.
-->