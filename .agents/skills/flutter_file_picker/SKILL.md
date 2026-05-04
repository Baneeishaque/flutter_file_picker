```markdown
# flutter_file_picker Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill describes the core development patterns and workflows for the `flutter_file_picker` repository. It covers coding conventions, file organization, and common maintenance workflows such as version bumping, code formatting, dependency updates, and branch synchronization. The repository is primarily written in Swift (for platform integration), but the main codebase is Dart for Flutter plugins. No major frameworks are detected, and code style emphasizes clarity and consistency.

## Coding Conventions

- **File Naming:**  
  All files use `snake_case` naming for consistency.  
  *Example:*  
  ```
  file_picker_windows.dart
  file_picker_platform_interface.dart
  ```

- **Import Style:**  
  Relative imports are preferred within the package.  
  *Example:*  
  ```dart
  import '../platform/windows/file_picker_windows.dart';
  ```

- **Export Style:**  
  Named exports are used to control public API surface.  
  *Example:*  
  ```dart
  export 'src/file_picker.dart' show FilePicker, FilePickerResult;
  ```

- **Commit Messages:**  
  Mixed types, typically prefixed with `chore:` or `style:`.  
  *Example:*  
  ```
  chore: bump version to 5.2.3 and update changelog
  style: apply dart format to all source files
  ```

## Workflows

### Version Bump and Changelog Update
**Trigger:** When releasing a new version or pre-release (beta)  
**Command:** `/bump-version`

1. Update the version number in `pubspec.yaml`.
2. Update `CHANGELOG.md` with relevant changes.
3. If necessary, update `example/pubspec.yaml` to match the new version.
4. Commit the changes with a descriptive message (e.g., `chore: bump version to x.y.z`).

*Example:*
```yaml
# pubspec.yaml
version: 5.2.3
```
```markdown
# CHANGELOG.md
## 5.2.3
- Added support for XYZ
- Fixed issue #123
```

---

### Code Formatting and Style Consistency
**Trigger:** After major merges or to enforce code style  
**Command:** `/format-code`

1. Run the Dart code formatter:
   ```
   dart format .
   ```
2. Ensure consistent indentation and style across all Dart files, including tests and examples.
3. Commit all affected files with a message like `style: apply dart format`.

*Example:*
```dart
// Before formatting
Future <void>pickFile( )async{...}

// After formatting
Future<void> pickFile() async {
  ...
}
```

---

### Dependency Update
**Trigger:** When upgrading a dependency (e.g., win32)  
**Command:** `/update-dependency`

1. Update the dependency version in `pubspec.yaml`.
2. If the update affects platform-specific code, update the relevant implementation files (e.g., `lib/src/platform/windows/file_picker_windows.dart`).
3. Test the changes to ensure compatibility.
4. Commit with a message like `chore: update win32 to 3.0.1`.

*Example:*
```yaml
# pubspec.yaml
dependencies:
  win32: ^3.0.1
```

---

### Merge Master into Feature Branch
**Trigger:** To synchronize a feature or chore branch with the latest `master`  
**Command:** `/merge-master`

1. Merge `master` into your feature branch:
   ```
   git checkout feature/my-feature
   git merge master
   ```
2. Resolve any conflicts, especially in:
   - `.github/workflows/main.yml`
   - `CHANGELOG.md`
   - `pubspec.yaml`
   - Platform-specific files (e.g., `android/`, `darwin/`, `ios/`)
   - Example and configuration files
3. Test the branch to ensure nothing is broken.
4. Commit with a message like `chore: merge master into feature/my-feature`.

---

## Testing Patterns

- **Test Framework:** Unknown (not explicitly detected)
- **Test File Pattern:** Test files are named with the `.test.ts` suffix, though Dart tests typically use `.dart`.  
  *Example:*  
  ```
  file_picker_test.dart
  ```
- **General Approach:**  
  - Place tests under the `test/` directory.
  - Use clear, descriptive test names.
  - Group related tests using `group()` and `test()` blocks (if using Dart's test package).

## Commands

| Command         | Purpose                                                      |
|-----------------|-------------------------------------------------------------|
| /bump-version   | Bump the package version and update changelog for a release |
| /format-code    | Apply code formatting and style consistency                 |
| /update-dependency | Update a dependency version in pubspec.yaml              |
| /merge-master   | Merge latest master into a feature or chore branch          |
```
