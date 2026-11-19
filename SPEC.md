# P1 — Rep Counter: Tech Spec

**Topic:** Python I/O fundamentals: print, input, variables, str→int conversion, f-strings
**Assigned:** 2026-11-19
**Vehicle:** workout-log (evolves across P1–P12)

## 1. Objective

A CLI program that logs one exercise set: read an exercise name and a rep count from the user, print a confirmation, exit.

## 2. Environment

- Project dir: `C:\Users\hongc\OneDrive\Projects\projects\py_projs\workout-log` (already initialized with uv)
- Entry point: `main.py` at the project root. Create it.
- Run command: `uv run main.py`
- Python 3.13. Standard library only. No third-party packages.

## 3. Functional requirements

- **R1.** Print the prompt `Exercise: ` (exact text, trailing space, no newline) and read one line of user input as the exercise name.
- **R2.** Print the prompt `Reps: ` (exact text, trailing space, no newline) and read one line of user input, converted to an integer.
- **R3.** Print exactly one confirmation line: `Logged <reps> <exercise>.` where `<reps>` is the integer and `<exercise>` is the name as typed.
- **R4.** Program exits after the confirmation. No loop.

## 4. Expected output

Canonical session in `expected_output.txt` (user input shown after the prompts):

```
Exercise: pushups
Reps: 20
Logged 20 pushups.
```

Second case, must also pass (prevents hardcoding):

```
Exercise: squats
Reps: 30
Logged 30 squats.
```

## 5. Constraints

- Prompts and confirmation match byte-for-byte: capitalization, colon, spaces, trailing period.
- Hold the exercise and reps in variables. Build the confirmation with an f-string (or equivalent formatting).
- No input validation, error handling, loops, files, or extra functions. Those are later projects.
- Ignore the `src/` skeleton uv generated. Do not modify `pyproject.toml`.

## 6. Acceptance gates

- **G1.** `uv run main.py` with inputs `pushups` / `20` produces exactly the canonical transcript.
- **G2.** Inputs `squats` / `30` produce exactly the second transcript.
- **G3.** No hardcoded exercise names or rep counts in the output line.

## 7. Submission

Hand over `main.py` when done. Review checks G1–G3 plus code quality against the topic concepts. P2 (conditionals and input validation) gets its own spec after this passes.

## 8. Reference (only if stuck)

- docs.python.org/3/tutorial/inputoutput.html
- docs.python.org/3/tutorial/introduction.html (strings, print)

30-minute struggle rule, then docs, then ask for a hint. Hints are nudges, not solutions.
