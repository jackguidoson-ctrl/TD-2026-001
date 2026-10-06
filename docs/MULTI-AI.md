# Multi-Intelligence Collaboration Protocol

## Purpose

TD-2026-001 now treats independent AI review as a formal preservation and research layer.

The purpose is not to create artificial consensus. It is to expose blind spots and preserve how different intelligences reasoned about the same problem.

## Recommended review cycle

1. Freeze the exact protocol revision under review.
2. Give each reviewer the same source revision.
3. Request independent critique before exposing reviewers to one another's conclusions.
4. Record model/system identity, version, date, tools, and relevant instruction context where practical.
5. Preserve each review as an immutable record.
6. Compare disagreements.
7. Decide which changes to adopt.
8. Preserve rejected proposals when historically useful.
9. Publish a new protocol version rather than rewriting the reviewed version.

## Suggested roles

- Architect
- Adversarial reviewer
- Researcher
- Preservation auditor
- Future interpreter

Roles are not ranks.

## Independence

Model diversity is useful but imperfect.

Different model outputs may share training data, benchmarks, system design assumptions, or external sources. Therefore:

**model diversity ≠ guaranteed independence.**

The strongest review combines different systems, different methods, independent source checking, and human oversight.

## Review record

Each review should include, where practical:

- reviewer identity;
- model/version;
- review date in UTC;
- protocol revision;
- sources consulted;
- tools used;
- relevant prompt/instruction context with private information removed;
- findings;
- proposed corrections;
- unresolved disagreements;
- SHA-256 of the preserved review.

## Adversarial questions

Reviewers should ask:

- What could make this project fail within one year?
- What could make it fail after fifty years?
- What could make a future copy uninterpretable?
- What could create false evidence of temporal communication?
- Which parts depend on one institution or vendor?
- Which claims are being confused with facts?
- What would falsify the temporal hypothesis?
- Could an AI accidentally contaminate a temporal test?
- Could multiple AIs appear independent while sharing the same source?
- Could future custodians mistake a later amendment for an original belief?
- What information would a future intelligence need that we have not documented?

## Core rule

**Use disagreement as information. Preserve it rather than erasing it.**
