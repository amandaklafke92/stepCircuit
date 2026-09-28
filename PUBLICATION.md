# Publication policy

StepCircuit is a public learning and portfolio project. Public visibility is intentional, but not every working file belongs in the repository.

## Suitable for publication

- Project documentation, decisions, experiments, and results written for a public audience.
- Source code, hardware designs, schematics, and bills of materials created for StepCircuit.
- Deliberately selected photos, diagrams, renders, and demonstration media after they have been reviewed for personal or third-party information.
- Test data that is synthetic, anonymised, or explicitly approved for public release.

## Keep private by default

- Credentials, API keys, access tokens, private keys, environment files, and account or service configuration containing secrets.
- Personal contact details, precise location data, health data, private calendar information, device identifiers, or identifiable participant data.
- Raw recordings, meeting exports, transcripts, screenshots, and other media that may expose people, notifications, browser tabs, or private surroundings.
- Proprietary, confidential, licensed, or course/community material that Amanda does not have permission to republish.
- Unreviewed data exports, logs, backups, local working files, and generated files that do not add value to the public project record.

## Before publishing

1. Review both the file content and metadata for secrets, personal information, and third-party material.
2. Prefer a redacted, anonymised, or purpose-made public version when the original contains private context.
3. Put reviewed public media in `docs/assets/`; keep raw source media outside Git or under the ignored `content/` directory.
4. Check the staged diff and run a secret scan before pushing.
5. If publication rights or privacy are uncertain, keep the material private until Amanda decides.

Removing a secret from the latest version does not remove it from Git history. If sensitive material is ever committed, rotate the affected credential where relevant and clean the history before relying on deletion.
