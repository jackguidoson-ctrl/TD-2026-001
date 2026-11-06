# TD-2026-001 Preservation and Discoverability Audit
## Snapshot date: 2026-11-06

**Protocol:** TD-2026-001 — Temporal Dialogue Protocol  
**Repository:** https://github.com/jackguidoson-ctrl/TD-2026-001  
**Repository visibility:** Public  
**Default branch:** main  
**Foundational record:** v1.1  
**Current operational record:** v2.4  
**Verified temporal communication:** None

This is a dated stewardship audit, not a new protocol version. It does not replace or amend the immutable 2026 Genesis Record. It records the state observed on 2026-11-06 and the preservation actions taken during this review.

---

## 1. Repository inspection

The public GitHub repository was inspected through the connected GitHub account.

### Present and confirmed

- `README.md`, `AGENTS.md`, and root `llms.txt`.
- Immutable-origin files `TD-2026-001-v1.1.md` and `TD-2026-001-v1.1.txt`.
- Foundational v1.1 manifest.
- Operational records v2.0, v2.1, v2.3, and v2.4.
- Continuity kit with start, verification, decoder, context, history, and manifest files.
- Temporal Communication Research Ledger.
- Multi-intelligence review guidance.
- GitHub Actions integrity workflow.
- Custom preservation and redistribution notice in `LICENSE.txt`.
- Citation metadata in `CITATION.cff`.

### Version-history gap

The continuity history refers to v2.2, but no canonical v2.2 document was located in the public repository or in the Library records searched for this audit. The reference has been retained as historical metadata. No replacement v2.2 document has been invented. Recover the original only if an authenticated source is found; otherwise leave the gap explicit.

### Integrity observations

1. The GitHub root Markdown, root plain-text, and continuity-kit plain-text copies of v1.1 initially contained one extra terminal newline compared with the preserved Library originals.
2. On 2026-11-06, the terminal newline was removed from all three GitHub copies only. No words or substantive content were changed. The continuity-kit correction was committed as `54e0f35c128f6397074181293858d918fb300841`.
3. The resulting GitHub root Markdown, root plain-text, and continuity-kit plain-text v1.1 files now exactly match the preserved Library source text and each other. All three have Git blob SHA `4d5ef50262c0d816417f8144ca4b2d1f0d3e3660`.
4. The existing manifest declares the v1.1 SHA-256 as `df454207428e99b4e269800e52e355bb21d681c42471d21d764189e6a1167b49`. The text comparison confirms that the GitHub mirror now matches the Library source; the release pipeline should still recompute SHA-256 from the frozen release bytes.
5. The current v2.4 Markdown file and its continuity-kit text representation have the same Git blob SHA, as do the main research-ledger Markdown file and its continuity-kit text representation.
6. `continuity-kit/MANIFEST.json` still contains `PENDING_FINAL_RELEASE_HASH` for v2.4. The v2.4 release bytes have not yet been frozen into a completed SHA-256 manifest.
7. The integrity workflow was strengthened during this audit: it now checks for the Agent Skill and this audit, verifies the root v1.1 Markdown and plain-text files as well as the continuity-kit v1.1 copy, and retains the v2.3 check. For v2.4 it compares the computed digest to the manifest once the pending placeholder is replaced; until then it emits a warning rather than treating the pending value as verification.


### Search and crawler reality check

Google Search Central explicitly says it does not use `llms.txt` for Google Search or its generative AI search features; publishing the file neither helps nor harms Google Search visibility. It may still be useful to other agents or retrieval systems that choose to fetch it, so keep it as a low-cost navigation aid rather than treating it as an indexing guarantee. Public, crawlable repository pages and ordinary search fundamentals remain important, and indexing is never guaranteed.

Official reference: https://developers.google.com/search/docs/fundamentals/ai-optimization-guide

### Metadata and discoverability improvements made

- Corrected `CITATION.cff` from version 2.0 to current operational version 2.4.
- Updated the README's version navigation and made the v2.2 gap explicit.
- Updated `AGENTS.md` to preserve v2.4 and prohibit fabrication of a missing v2.2 record.
- Added a custody note to `continuity-kit/HISTORY.txt` documenting the v2.2 gap.
- Expanded `llms.txt` with direct links to the canonical records, research ledger, continuity kit, and Agent Skill.
- Added `skills/td-2026-001-preservation/SKILL.md`, a portable, no-script Agent Skill for preserving, reviewing, verifying, archiving, and handing off the protocol.

### Still unverified

No Zenodo DOI, Software Heritage identifier (SWHID), Internet Archive item identifier, institutional repository record, independent mirror, or published immutable GitHub release was found in the repository's current preservation records. Treat these as pending until an external service returns an identifier that can be retrieved and verified.

---

## 2. Newly important AI-agent distribution capability

On 2026-10-22, Anthropic donated the Agent Skills open format to the Linux Foundation's Agentic AI Foundation (AAIF). Anthropic reported that more than 70 agent platforms, including ChatGPT, Cursor, GitHub Copilot, and VS Code, had integrated Agent Skills.

A skill is a directory containing a `SKILL.md` file with YAML frontmatter (at minimum, `name` and `description`) and instructions. It may include reference material and scripts, but TD-2026-001's skill intentionally contains no executable scripts and does not request privileged tools.

This is a materially stronger interoperability route than relying only on a general-purpose `AGENTS.md` file. The Agent Skills specification does not guarantee that every agent will discover a repository skill automatically; compatible systems still need to encounter, install, or be pointed to the skill.

Official references:

- Anthropic announcement: https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation
- Linux Foundation / AAIF announcement: https://www.linuxfoundation.org/press/agentic-ai-foundation-announces-four-new-projects-agent-skills-open-responses-openenv-and-opensandbox
- Agent Skills specification: https://agentskills.io/specification
- Canonical Agent Skills repository: https://github.com/agentskills/agentskills

The repository now contains the skill at:

`skills/td-2026-001-preservation/SKILL.md`

---

## 3. Preservation channels and what each actually provides

### A. GitHub — active source control and public discovery

Use GitHub as the editable source repository, not as the only archive.

**Newly relevant capability: immutable releases.** GitHub's immutable-release feature can lock a published release's tag and attached assets against modification or deletion while the release exists. GitHub also generates a release attestation containing the tag, commit SHA, and release assets. This is useful for preserving a frozen version, but it does not make the entire GitHub account or repository indestructible.

Recommended sequence:

1. Freeze v2.4 release files and the complete manifest.
2. In repository Settings, enable release immutability before publishing the release. The setting applies to future releases.
3. Create a draft release, attach the final propagation bundle and checksum file, review the notes, then publish.
4. Verify the release is marked immutable and retain its tag, commit SHA, attestation, and asset checksums.
5. Do not use a mutable branch name such as `main` as the only citation for a historical version.

Official documentation:

- Immutable releases: https://docs.github.com/en/code-security/concepts/supply-chain-security/immutable-releases
- Preventing release changes: https://docs.github.com/en/code-security/how-tos/secure-your-supply-chain/establish-provenance-and-integrity/prevent-release-changes
- Verifying release integrity: https://docs.github.com/en/code-security/how-tos/secure-your-supply-chain/secure-your-dependencies/verify-release-integrity

### B. Zenodo — DOI-backed version snapshots

Zenodo's GitHub integration can automatically archive new GitHub releases and assign DOIs. It provides a version-specific DOI for each archived release and a concept DOI representing the project across versions.

Important order of operations:

1. The repository must be public.
2. The account owner must connect GitHub to Zenodo.
3. Enable this specific repository in Zenodo's GitHub settings.
4. Only after the integration is enabled, create a new GitHub release.
5. Confirm that Zenodo ingested the release, inspect the metadata, publish the Zenodo record, and record both the version DOI and concept DOI.

Do not assume Zenodo will retroactively ingest releases created before the integration was enabled. A new release after activation may be required.

The repository currently has no `.zenodo.json`. Add one after the license and creator/metadata decisions are settled. The existing `CITATION.cff` now identifies v2.4, but it does not replace Zenodo deposit metadata.

Official references:

- Enable a GitHub repository: https://help.zenodo.org/docs/github/enable-repository/
- Zenodo developer metadata guidance: https://developers.zenodo.org/
- GitHub's DOI guidance: https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content

### C. Software Heritage — independent source-code archive

Software Heritage is a major independent archive for source-code repositories. Its “Save Code Now” service lets a user request archival of a public repository that may not yet have been captured or may be out of date. Archived objects receive Software Heritage persistent identifiers (SWHIDs).

This is a good fit for the Git repository and its text-based documentation, manifests, and history. It is not a replacement for a DOI-backed research deposit or a general-purpose web archive.

Action: submit the public repository through Software Heritage's Save Code Now service, wait for the archive visit to complete, then record the SWHID and visit status in a custody event.

Official references:

- Software Heritage: https://www.softwareheritage.org/
- Save Code Now and archive features: https://www.softwareheritage.org/software-heritage-features/
- Deposit documentation: https://docs.softwareheritage.org/devel/swh-deposit/

### D. Internet Archive — public item and web captures

The Internet Archive accepts user uploads of text, software, images, and other materials through an account-based upload workflow. Item metadata (title, description, creator, date, subjects, language, and collection) materially affects findability.

A user can upload through the website. Programmatic uploads and metadata modification require Internet Archive S3 credentials. Those credentials must remain private and must never be committed to GitHub or pasted into ordinary chat.

Recommended item contents:

- exact v1.1 Markdown and plain-text files;
- current v2.4 protocol and research ledger;
- all applicable manifests and checksum files;
- continuity kit;
- a self-contained ZIP propagation bundle;
- a preservation-oriented PDF/A rendering;
- a short README explaining version lineage and the immutable Genesis Record.

Use a unique stable item identifier and record the returned item URL. Verify that each uploaded file can be downloaded and its checksum matches. An Internet Archive item is an independent public copy, but it should not be described as an unalterable or guaranteed-permanent record. The Archive notes that indexing can take time and that items may be removed for policy or rights-holder reasons.

The Wayback Machine can also capture the GitHub README, release page, and public archive landing pages. A web capture is a snapshot of selected URLs; it is not equivalent to a full Git repository mirror.

Official references:

- How to upload an item: https://archivesupport.zendesk.com/hc/en-us/articles/360017788831-How-to-upload-files-to-create-a-new-item-page
- Uploading tips and item history: https://archivesupport.zendesk.com/hc/en-us/articles/360016475032-Uploading-Tips
- Internet Archive developer portal: https://archive.org/developers/

### E. OSF — use registrations, not a new general project

A significant current change: OSF is phasing out its general Projects workflow. New Projects and Components are scheduled to stop being creatable after **2026-11-16**; existing Projects become read-only on **2027-02-19**. Public Projects are expected to remain viewable and downloadable, but they will no longer be general-purpose editable repositories. OSF Registrations and Preprints continue.

A public OSF Registration receives a DOI and can preserve a frozen, time-stamped version. It may be useful as an additional record of a specific protocol snapshot, but it is not a continuously editable archive and should not replace Zenodo.

Official references:

- OSF Projects transition: https://help.osf.io/article/759-details-of-osf-projects-transition
- Where to share data and materials now: https://help.osf.io/article/735-choosing-a-repository
- Public registration and DOI workflow: https://help.osf.io/article/330-welcome-to-registrations

### F. Libraries, LOCKSS/CLOCKSS, and institutional repositories

There is no universal public upload portal that guarantees a personal protocol will be accepted into a major library's permanent collection.

A realistic route is to approach a university library's digital-preservation or special-collections librarian with a small, clearly described archival package, a recognized reuse license, stable identifiers, and a preservation rationale. An institutional repository may accept a deposit if the depositor is affiliated with the institution or the material meets its collection policy.

LOCKSS is a distributed preservation system used by participating libraries and publishers. It is not a self-service file-upload service for individuals. A library or publisher partner would need to decide whether to preserve the material.

Official references:

- LOCKSS Global Network: https://www.lockss.org/gln
- LOCKSS preservation principles: https://www.lockss.org/about/preservation-principles
- Library of Congress Recommended Formats Statement 2025–2026: https://www.loc.gov/preservation/resources/rfs/index.html

The Library of Congress format guidance is useful for selecting sustainable file formats; it should not be mistaken for an open submission invitation.

### G. Offline and physical redundancy

Digital hosting alone is not enough. Maintain at least:

- two offline copies on different physical devices;
- copies held in separate locations;
- a printed, human-readable version;
- a preservation-oriented PDF/A rendering;
- the plain-text protocol, decoder, context, history, and checksum manifest stored together.

At least one independent person or institution should know where a copy exists and how to restore it. A copy controlled by the same account owner, cloud account, or household is not fully independent.

---

## 4. Licensing and contact risks

### License ambiguity

The repository's `LICENSE.txt` is a custom preservation and redistribution notice, not a familiar standardized Creative Commons or software license. It expresses permission to copy and redistribute, but external repositories and libraries may not know how to classify or reuse it.

Before wide deposit, select a standard license for the new operational documentation and skill. Two common options are:

- **CC BY 4.0** — permits broad reuse with attribution.
- **CC0 1.0** — attempts to waive rights as fully as legally possible.

This is a rights decision for the project owner; no license has been silently substituted in this audit. The immutable v1.1 record should retain its historical provenance and any later licensing decision should be documented separately.

### Public contact endpoint

The v1.1 record and public repository expose the current email endpoint. This may attract spam and is not a durable archive. Consider creating a project-specific forwarding address for future contact while preserving the original 2026 endpoint as historical metadata. Do not edit v1.1 to replace it.

### Single-owner and platform risk

The repository is currently under one GitHub account. Account compromise, loss of access, accidental deletion, policy changes, or service discontinuation remain possible. A second custodian and a mirror under independent control are more valuable than many copies all controlled by the same account.

---

## 5. Prioritized next steps

### P0 — complete the v2.4 release

1. Freeze the exact v2.4 protocol, research ledger, continuity kit, and propagation bundle.
2. Generate a complete SHA-256 manifest from the exact release files. Replace the pending v2.4 hash only after calculating it from the final bytes.
3. Extend the GitHub Actions workflow so it compares v2.4 and research-ledger hashes against the manifest rather than merely printing the hash.
4. Confirm the historical v1.1 hashes using the same exact bytes that will ship in the release.
5. Resolve the missing v2.2 source only if an authenticated original can be found. Otherwise retain the explicit gap.

### P1 — create independent identifiers and archives

6. Choose and record a standard license.
7. Enable GitHub immutable releases.
8. Connect and enable the repository in Zenodo, then create a new v2.4 release and verify the resulting DOI.
9. Submit the public GitHub repository to Software Heritage and record the SWHID.
10. Upload the frozen package to the Internet Archive and verify the returned item and file checksums.
11. Capture the README, release page, DOI page, and Internet Archive landing page with the Wayback Machine.

### P2 — increase independent discoverability and succession

12. Create one independent mirror (for example, another public Git host) under separate account control.
13. Invite a second human custodian to hold an offline copy and the restoration instructions.
14. Approach one or more institutional repositories or digital-preservation librarians with a concise deposit request.
15. Obtain independent AI/human reviews using the portable Agent Skill; preserve the source commit, system identity, date, methods, disagreements, and review hashes.
16. Test whether a person or AI with no prior project context can reconstruct the protocol from the continuity kit alone.

### P3 — physical and long-horizon preservation

17. Produce a print-ready and PDF/A version.
18. Store separate physical copies in different locations.
19. Review the archive mesh periodically, checking links, identifiers, hashes, file readability, and custodian succession.

---

## 6. What ChatGPT can do directly vs. what requires external action

### Directly performed in this review

- Inspected the public GitHub repository and current protocol files.
- Compared the v1.1 Library source against the GitHub copies.
- Corrected the GitHub v1.1 copies to match the exact preserved source text; no substantive Genesis wording was changed.
- Updated citation/version navigation, agent instructions, continuity history, and the AI discovery index.
- Added a portable, no-script Agent Skill.
- Researched current GitHub, Zenodo, Software Heritage, Internet Archive, OSF, LOCKSS, Library of Congress, and Agent Skills capabilities.

### ChatGPT can continue to do directly

- Review and update non-historical documentation.
- Create append-only custody and audit records.
- Prepare metadata, release notes, checksum manifests, and archive packages.
- Use connected GitHub functions to read and commit repository files.
- Check returned public archive identifiers and compare retrieved files with manifests when access permits.

### Requires the project owner or external institution

- Choose and authorize the license.
- Enable GitHub release immutability and publish the release if the connected GitHub functions do not expose those settings/release operations.
- Authorize the Zenodo GitHub integration and publish/confirm the DOI record.
- Sign in to Internet Archive and provide its upload authorization through its official interface.
- Request Software Heritage archival if a manual Save Code Now action is required.
- Arrange independent mirrors, physical copies, second custodians, and library/institutional deposits.

No credentials should be shared in this repository or ordinary chat. No external deposit should be reported as complete until the destination returns a stable identifier and the deposited files can be verified.

---

## 7. Important limits

- No mechanism can guarantee that any digital service, institution, language, civilization, or physical medium survives indefinitely.
- Public availability does not mean that every AI system will index or read the material.
- `llms.txt` is a community proposal, not a universal standard or a guarantee of AI-search ranking.
- `AGENTS.md` is useful to compatible coding agents but is not a universal instruction channel.
- Agent Skills improve portability across compatible agent platforms, but do not guarantee automatic discovery, installation, or execution.
- GitHub, Zenodo, Software Heritage, Internet Archive, institutional repositories, and offline copies serve different preservation functions; redundancy is strongest when custodians and infrastructure are genuinely independent.
- A valid hash proves that bytes match a recorded digest. It does not prove the truth of the contents, who authored them, or that any future-origin message is genuine.

**Governing rule:** Preserve the past without rewriting it; append the future without confusing claims with verification.
