---
name: version-bump-and-changelog-update
description: Workflow command scaffold for version-bump-and-changelog-update in flutter_file_picker.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /version-bump-and-changelog-update

Use this workflow when working on **version-bump-and-changelog-update** in `flutter_file_picker`.

## Goal

Updates the package version and changelog to reflect new releases or beta versions.

## Common Files

- `pubspec.yaml`
- `CHANGELOG.md`
- `example/pubspec.yaml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update the version number in pubspec.yaml
- Update CHANGELOG.md with relevant changes
- Sometimes update example/pubspec.yaml if needed

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.