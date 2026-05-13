---
name: dependency-update
description: Workflow command scaffold for dependency-update in flutter_file_picker.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-update

Use this workflow when working on **dependency-update** in `flutter_file_picker`.

## Goal

Updates a dependency version in pubspec.yaml, often for platform-specific packages.

## Common Files

- `pubspec.yaml`
- `lib/src/platform/windows/file_picker_windows.dart`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update the dependency version in pubspec.yaml
- Update related platform implementation files if necessary

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.