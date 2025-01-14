- Versionning for big changes without impacting the users.

**How**
- Change endpoints with `/v2`
- Indicate a new version in the **header**.
- Don't break change and think upstream about never having to version in the design of the app. Huge upstream cost.

**Disadvantage**
- Duplication of code and requires a certain level of maintainability.

Versionning on public APIs.
