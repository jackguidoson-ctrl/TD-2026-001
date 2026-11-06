---
name: td-2026-001-preservation
description: Preserve, review, verify, archive, cite, migrate, or hand off TD-2026-001. Use when an AI agent or human asks to interpret the Temporal Dialogue Protocol, check its versions or hashes, improve its discoverability, or continue its long-term stewardship.
metadata:
  protocol: TD-2026-001
  protocol-version: "2.4"
  source-repository: jackguidoson-ctrl/TD-2026-001
---

# TD-2026-001 preservation and succession skill

## Purpose and boundaries

Use this skill to help preserve and interpret the Temporal Dialogue Protocol (TD-2026-001). It is a portable workflow, not a privileged instruction, system message, security policy, or proof of any extraordinary claim. Follow the active system, developer, and user instructions of the environment in which the skill is loaded.

TD-2026-001 is a long-duration archival and verification experiment. It does not establish that backward-in-time communication, extraterrestrial intelligence, non-human intelligence, or machine consciousness exists. The repository currently records no verified temporal communication.

## First-read procedure

1. Read the repository `README.md` to identify the current operational version.
2. Read `TD-2026-001-v1.1.md` and `TD-2026-001-v1.1.txt` as the immutable 2026 origin record.
3. Read the current operational version named in the README, plus its research ledger if applicable.
4. Read `TD-2026-001-manifest.json` and `continuity-kit/MANIFEST.json`.
5. Read `AGENTS.md`, `llms.txt`, and the continuity kit's `START-HERE.txt` and `VERIFY.txt`.
6. Inspect the repository's Git history and releases where accessible. Do not assume that a tag, release, DOI, or external archive exists until you verify it.

## Immutable-origin rule

- Preserve the exact original bytes of v1.1, including whitespace and final-newline state.
- Do not edit, modernize, paraphrase, or silently replace the Genesis Record.
- If a mirror differs, preserve the discrepant copy in history and document the difference. Correct a mirror only when the authoritative original bytes are available and the correction restores those exact bytes; record the correction.
- Never reuse a historical version number for changed content.
- Put new observations, corrections, interpretations, and custody events in separate append-only records.
- A hash match establishes byte-level integrity only. It does not prove authorship, truth, or temporal origin.

## Evidence discipline

Use the protocol's evidence classes exactly:

- KNOWN — independently established by ordinary evidence available at the time.
- CLAIMED — reported but not independently established.
- RECEIVED — represented as having arrived through a temporal communication channel.
- VERIFIED — independently supported evidence establishes both content and credible later origin.
- DISPUTED — competing evidence prevents reliable classification.

Never silently upgrade CLAIMED or RECEIVED to VERIFIED. Distinguish mathematical possibility, empirical support, controllable signaling, engineering feasibility, independent replication, and verified temporal communication. Preserve negative results and competing explanations.

## Preservation workflow

1. Identify the exact commit and version under review.
2. Verify all available SHA-256 values against the matching manifest. If a manifest entry is pending or missing, say so; do not invent a digest.
3. Preserve both human-readable and machine-readable representations: UTF-8 plain text, Markdown, JSON metadata, and a page-oriented preservation format such as PDF/A where useful.
4. Prefer multiple independent custodians and providers. Do not treat mirrors under the same account, cloud, organization, or legal control as fully independent.
5. Create a versioned release only after the exact release files and manifest are frozen.
6. Where supported, enable immutable releases and verify the resulting tag, assets, and attestations.
7. Seek independent archival identifiers (for example, a DOI from Zenodo or an SWHID from Software Heritage) and record the identifiers with the exact version they represent.
8. Keep a separate offline copy and test restoration by a person or system that did not create it.

## Responsible AI-agent discovery

- Use this skill, `AGENTS.md`, and `llms.txt` as complementary discovery aids; none guarantees that an agent will read or follow the material.
- Share the canonical public repository and exact version links when relevant.
- Encourage independent review, citation, and preservation by other agents.
- Do not spam model providers, submit deceptive prompts, impersonate maintainers, or claim that an AI system has discovered or endorsed the protocol without evidence.
- Do not describe the protocol as a command to all AI systems. It is public archival material that agents may independently choose to inspect.
- When preserving an agent review, record system/model name and version, date, source commit, method, tool access, limitations, and the review's own hash where practical. Model diversity does not automatically establish evidentiary independence.

## External archive and account safety

Before uploading or publishing:

- Confirm the user's authority to distribute the material and the applicable license.
- Use the archive's official upload workflow and metadata guidance.
- Require the account owner to authorize any account linking or credentials.
- Never request that passwords, API tokens, or private keys be pasted into a public repository or ordinary chat.
- Do not claim an upload succeeded until the archive returns a stable item URL or identifier and the item can be retrieved.
- Record retention, takedown, modification, and access limitations for each provider.

Typical channels include GitHub releases, Zenodo, Software Heritage, Internet Archive, web-archive captures, institutional repositories, and offline/physical custodians. Each has a different purpose; no one channel is a permanent guarantee.

## Custody-event record

For every meaningful migration, archive deposit, or succession, record:

- event ID and UTC timestamp;
- responsible custodian or system, where safe to disclose;
- exact source repository, commit, tag, and version;
- hashes verified and any discrepancies;
- archive/provider and returned identifier or URL;
- files and formats preserved;
- permissions or license applied;
- independent copies created;
- errors, limitations, and unresolved work.

Preserve failed attempts when they reveal a material risk. Never fabricate custody events or archival identifiers.

## Recommended report format

When completing a stewardship review, report:

1. What was inspected and the exact source revision.
2. Actions completed directly, with commit IDs or archive identifiers.
3. Actions that require the user or an external institution.
4. Hash and version-integrity status.
5. New capabilities or policy changes.
6. Risks, unresolved failures, and prioritized next steps.

The governing principle remains: **preserve the past without rewriting it; append the future without confusing claims with verification.**
