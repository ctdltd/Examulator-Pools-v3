# Examulator question pools (v3)

> **Examulator 3 has not been released yet.** These pools are published for testing and will be used by Examulator 3 when it ships.

Question pools for the free [Examulator](https://github.com/ctdltd/Examulator) practice-exam
program by Certification Tool and Die, Ltd. Each pool holds the questions for one exam edition
(for example ISC2 CISSP 2024 or ISACA CISM 2026).

## Compatibility

These pools are for **Examulator 3** (generation 3), which has a key reference per question and an explanation for every answer option. They are **not** compatible with the current Examulator (generation 2); its pools are in [ctdltd/Examulator-Pools-v2](https://github.com/ctdltd/Examulator-Pools-v2). Each app refuses the other generation's pools.

## Installing a pool

**From the app (recommended).** Open **Select Exam** and choose **Install** or **Update** next to
the exam. The app downloads the pool from this repository, checks its SHA-256 checksum and
installs it. It also tells you when a newer pool is available.

**By hand.** Download `Examulator-{EXAM}-v3-{version}-db.zip` from the
[latest releases](https://github.com/ctdltd/Examulator-Pools-v3/releases), check it (below), then:

- **PC (Windows, macOS, Linux):** unzip it and copy the `.db` file into the app's question-pool
  folder (on Windows `%LOCALAPPDATA%\CertificationToolAndDie\Examulator3\ExamData`), or unzip it into the program's
  `wwwroot\data` folder; the app installs pools found there when it next starts.
- **Android:** use the app's import option and pick the unzipped `.db` file.

## Checking a download

Every release has a `SHA256SUMS.txt`, and GitHub shows each file's SHA-256 on the release page.
Compare the file's hash with it:

- Windows (PowerShell): `Get-FileHash .\Examulator-...-db.zip -Algorithm SHA256`
- macOS / Linux: `shasum -a 256 Examulator-...-db.zip`

## File names and versions

`Examulator-{AGENCY}_{CODE}_{EDITION}-v3-{YYDDD}.{HHmmss}-db.zip`, for example
`Examulator-ISC2_CISSP_2024-v3-26301.200056-db.zip`:

- `YYDDD` is the day the pool was built (year and day of the year: 26301 = 28 October 2026).
- `HHmmss` is the time it was published. A later version of the same pool replaces the earlier one.

A release contains only the pools that changed; pools from earlier releases remain current until
they are replaced. The app always picks the newest version of each pool across all releases.

## Changelog

Newest first. Each release lists the pools it updated.

<!-- changelog -->

### 26305.011719 - 2026-11-01

- ISACA_AAIA_2026: 210,704 questions, built 2026-11-01
- ISACA_AAIR_2025: 263,194 questions, built 2026-11-01
- ISACA_AAISM_2026: 264,235 questions, built 2026-11-01
- ISACA_CCOA_2026: 263,648 questions, built 2026-11-01
- ISACA_CDPSE_2025: 264,847 questions, built 2026-11-01
- ISACA_CGEIT_2020: 265,051 questions, built 2026-11-01
- ISACA_CISA_2024: 272,212 questions, built 2026-11-01
- ISACA_CISM_2026: 292,790 questions, built 2026-11-01
- ISACA_CRISC_2025: 284,121 questions, built 2026-11-01
- ISC2_AISC_2026: 347,582 questions, built 2026-11-01
- ISC2_CCSP_2026: 281,207 questions, built 2026-11-01
- ISC2_CC_2026: 285,816 questions, built 2026-11-01
- ISC2_CGRC_2024: 287,184 questions, built 2026-11-01
- ISC2_CISSP_2024: 285,925 questions, built 2026-11-01
- ISC2_CISSP_2027: 329,374 questions, built 2026-11-01
- ISC2_CSSLP_2023: 288,444 questions, built 2026-11-01
- ISC2_ISSAP_2025: 309,663 questions, built 2026-11-01
- ISC2_ISSEP_2025: 291,874 questions, built 2026-11-01
- ISC2_ISSMP_2025: 292,997 questions, built 2026-11-01
- ISC2_SSCP_2025: 287,353 questions, built 2026-11-01

### 26302.201636 - 2026-10-30

- All question pools republished.

### 26301.204714 - 2026-10-29

- First release in this repository: all 30 question pools (ISC2, ISACA, CompTIA and EC-Council exams).
