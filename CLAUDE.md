# CLAUDE.md

## Commits
- Format: `:gitmoji: [scope] Message` — message starts uppercase, written in English.
- Scopes: `back` · `front` · `infra` · `ci` · `doc`
- No co-author lines — never add `Co-Authored-By` trailers.
- No session/agent trailers either (e.g. `Claude-Session:`) — commit messages stay generic, no links back to an assistant session. Leaking a session URL into public commit history is a security concern.

## Before committing to a project
- Read that project's own `CLAUDE.md` first, every time — don't assume a convention from one sibling project (commit format, co-author lines, etc.) applies to another.

## Reference implementations
- If one project is named as the reference for a shared pattern, only bring the others in line with it. Never modify the reference itself to match the others — that inverts the fix.

## Cross-project changes
- Before touching multiple sibling projects for consistency, confirm which one (if any) is the fixed reference before writing any diff.
