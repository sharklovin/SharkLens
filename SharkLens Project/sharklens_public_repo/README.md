# SharkLens

SharkLens is a cybersecurity investigation tool built to turn raw network evidence into investigation ready findings.

It helps analysts move from packets to answers by extracting host and user context, correlating evidence across protocols and records, and producing structured outputs that support faster triage and reporting.

## Why SharkLens

Analysts often spend too much time manually jumping between protocol trees, packet records, timestamps, and scattered artifacts just to answer basic but critical questions:

- Which endpoint was infected?
- What was the hostname?
- Which user account was involved?
- What evidence supports the conclusion?
- How do the findings connect into one incident story?

SharkLens was built to reduce that manual effort and make the evidence trail easier to follow.

## Current capabilities

- Extract infected client identifiers such as IP address, MAC address, hostname, user account name, and full user name when present in evidence
- Preserve protocol field order during parsing instead of flattening important structures
- Handle evidence paths that require duplicate field awareness instead of stopping at the first matching label
- Correlate clues across multiple evidence sources to build a clearer incident narrative
- Produce investigation friendly outputs that can support reporting and analyst review
- Emphasize evidence traceability so findings can be tied back to source records

## Example analyst questions SharkLens is built to answer

- What is the IP address of the infected Windows client?
- What is the MAC address of the infected Windows client?
- What is the host name of the infected Windows client?
- What is the user account name from the infected Windows client?
- What is the full name of the user from the user account?

## How it works

At a high level, SharkLens follows this flow:

1. Ingest evidence such as packet captures and related structured outputs
2. Parse relevant protocol trees and preserve field hierarchy where needed
3. Extract candidate values for hosts, users, sessions, and communications
4. Correlate linked evidence across records and timestamps
5. Return investigation ready findings with traceable supporting evidence

## Public repo contents

This public repository is intended to show the architecture, core logic, safe examples, screenshots, and sanitized outputs.

Recommended public contents:

- Clean source code that is safe to publish
- Screenshots or demo images inside `docs/screenshots/`
- Sanitized example inputs inside `sample_data/`
- Sanitized example outputs inside `sample_outputs/`
- Documentation that explains logic, evidence handling, and roadmap

## Suggested screenshots for this repo

Add these when you are ready:

1. Main interface or terminal workflow
2. Host and user extraction result
3. Evidence correlation view
4. Report output or summary view
5. One difficult edge case you solved

## Repository structure

```text
sharklens/
  README.md
  LICENSE
  .gitignore
  CHANGELOG.md
  docs/
    screenshots/
  sample_data/
  sample_outputs/
  src/
```

## Before publishing

Review the repo and remove or replace anything sensitive:

- API keys
- environment files
- real PCAPs that should not be public
- internal file paths
- personal data
- private notes or draft experiments

## Release notes

See [CHANGELOG.md](CHANGELOG.md).

## Roadmap

Planned public facing improvements:

- stronger evidence graph views
- richer evidence traceability in outputs
- clearer parser level provenance for every finding
- more screenshots and walkthrough material
- public safe demo dataset for reproducible examples

## License

This repository currently uses the MIT License. Update it if you want a different open source license.
