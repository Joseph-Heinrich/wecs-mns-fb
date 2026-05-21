# Changelog

All notable changes to FB/FC blocks in this repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)
where applicable for tagged releases.

Because the tracked artifact is a binary `.zap19` archive, every change entry
should explicitly state which FB/FC are affected so reviewers can locate them
inside the TIA Portal project after extracting the archive.

---

## [0.1.4] - 2026-05-21

### Changed
- `OM18MplcSafety`: Modified and tested to fit the requirements.
- `MplcSafetyLogic`: Modified and tested to fit the requirements.
- `MachineSafetyLogic`: Modified and tested to fit the requirements.
- `MplcNonSafetyLogic`: Modified and tested to fit the requirements.
- `MachineNonSafetyLogic`: Modified and tested to fit the requirements.

---

## [0.1.3] - 2026-05-18

### Changed
- `OM18MplcSafety`: MPLC safety logic, located in MPLC. Integrate all the previous safety FBs. Added in `Main_Safety_RTG1`.
- `OM18MplcNonSafety`: MPLC non-safety logic, located in MPLC. Integrate all the previous non-safety FBs. Added in `Main`.
- `OMMachineSafety`: Machine PLC safety logic, located in machine PLCs. Integrate all the previous safety FBs. Added in `Main_Safety_RTG1`.
- `OMMachineNonSafety`: Machine PLC non-safety logic, located in machine PLCs. Integrate all the previous non-safety FBs. Added in `Main`.

---

## [0.1.2] - 2026-05-15

### Changed
- `ModeCheck`: MPLC safety logic, located in MPLC. Change the logic of checking selected machine. Not added to any program cycle yet.
- `MachineDataTransferToOM18Group`: Machine PLC safety logic, located in MPLC. Added logic to select different machine in OM18. Not added to any program cycle yet.

---

## [0.1.1] - 2026-05-13

### Changed
- `MplcSafetyLogic`: MPLC non safety logic, located in MPLC. Added E-STOP / Guards OK / Control ON / Activate OM / Deactivate OM / Set Pay Off Mode / Set Take Up Mode / Dancer safety limit logic. Not added to any program cycle yet.
- `MachineSafetyLogic`: Machine PLC safety logic, located in Front Machine 1. Added E-STOP / Guards OK / Control ON / Switch modes / Dancer safety limit / Motors ON logic. Not added to any program cycle yet.
- `OM18MplcNonSafety`: MPLC non safety logic, located in MPLC. Added Line speed / Max speed / Max acceleration / Max deceleration / Dancer position / Dancer alarm setpoint / Dancer stop setpoint logic. Not added to any program cycle yet.
- `OM18MachineNonSafety`: Machine PLC non safety logic, located in Front Machine 1. Added Line speed / Max speed / Max acceleration / Max deceleration / Dancer position / Dancer alarm setpoint / Dancer stop setpoint logic. Not added to any program cycle yet.

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