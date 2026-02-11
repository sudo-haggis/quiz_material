# Bash Quiz Questions

A running list of questions based on real problems solved in chat.
Claude fetches this to avoid repetition and find gaps.

**Format:** Topic · Question summary · Date added

---

## Aliases & Functions

- Alias vs function: ghost alias in session mangling function definition on source · 2026-02-11
- Ghost alias: commenting out alias in .bashrc doesn't unset it in current session · 2026-02-11
- Alias persistence: aliases set in terminal are session-only, must go in .bashrc · 2026-02-11
- Alias argument passing: alias can't cleanly take arguments — needs a function with ${1:-1} · 2026-02-11
- unalias before function: use unalias NAME 2>/dev/null to safely clear ghost aliases · 2026-02-11
- Function default args: ${1:-1} provides fallback value if no argument passed · 2026-02-11

## Scripts & Execution

- Shebang: trailing slash in #!/bin/bash/ breaks ./script.sh but not bash script.sh · 2026-02-11
- PATH: chmod +x doesn't make a script runnable by name — needs ./ or to be in PATH · 2026-02-11
- bash -n: only syntax checks, does not expand aliases — can pass clean but source fails · 2026-02-11
- Commenting out lines: # must be the very first character on the line · 2026-02-11
- Sourcing vs executing: sourced file runs in current shell, executed script runs in subshell · 2026-02-11

## Redirections & Pipes

- 2>&1: redirects stderr (fd 2) to wherever stdout (fd 1) is pointing · 2026-02-11
- > vs >>: overwrite vs append · 2026-02-11
- Pipe |: connects stdout of one command to stdin of next · 2026-02-11
- Command groups: { cmd1; cmd2; } | pipe — grouping multiple outputs into one stream · 2026-02-11
- Command substitution: $() preferred over backticks — nestable and readable · 2026-02-11
- /dev/null: discard output with > /dev/null, discard both with &> /dev/null · 2026-02-11

## Debugging

- hexdump -C: inspect raw bytes when cat -A looks clean but something is wrong · 2026-02-11
- Variable syntax: missing $ checks literal string not variable value · 2026-02-11
- Array syntax: ${arr[@]} requires closing } — missing brace causes silent failures · 2026-02-11

---

## Suggested next topics to cover

- zoxide: requires re-source after stow setup (active TODO)
- here-docs: << vs <<- and delimiter rules
- trap: cleanup on script exit
- set -e / set -u: strict mode gotchas
- $?: exit code checking and chaining with && and ||
- while read loops: reading file line by line safely