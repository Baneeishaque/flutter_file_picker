---
name: code-formatting-and-style-consistency
description: Workflow command scaffold for code-formatting-and-style-consistency in flutter_file_picker.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /code-formatting-and-style-consistency

Use this workflow when working on **code-formatting-and-style-consistency** in `flutter_file_picker`.

## Goal

Applies consistent code formatting and indentation across implementation and test files.

## Common Files

- `lib/src/**/*.dart`
- `test/**/*.dart`
- `example/lib/src/**/*.dart`
- `tool/**/*.dart`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Run code formatter (e.g., dart format .)
- Apply consistent indentation and style across multiple files
- Commit all affected files

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.