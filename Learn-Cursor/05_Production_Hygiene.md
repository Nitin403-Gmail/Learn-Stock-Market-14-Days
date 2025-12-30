# Module 05: Production Hygiene

*Using AI to clean, document, and harden your code.*

## 1. The "Boring Work" Engine

The part of coding everyone hates—writing docs, unit tests, and typing—is where AI shines brightest. It never gets bored.

**Rule**: Never write your own unit test boilerplate again.

## 2. Documentation Workflow

Documentation is usually stale. Cursor makes it "Live."

### Technique A: Inline Docs (`Cmd+K`)

1. Highlight a complex function.
2. `Cmd+K`: "Add JSDoc comments explaining parameters and returns."
3. **Result**: Perfect, standard-compliant comments.

### Technique B: The README Generator

1. Open Chat.
2. Prompt: "Based on @Codebase, write a README.md that explains how to install, run, and the architecture overview."
3. **Result**: A 90% complete README. You just fill in the nuanced details.

## 3. The Testing Machine

Writing tests is about covering edge cases. AI is great at imagining edge cases.

**Process**:

1. Open your logic file (e.g., `calc.ts`).
2. Open a new test file (e.g., `calc.test.ts`).
3. **Cmd+K** in the test file:
    > "Reference @calc.ts and write comprehensive unit tests. include edge cases for null/negative inputs."

**Pro Tip**: Ask the AI to *break* your code.
> **Chat**: "Look at @calc.ts. Are there any inputs that would cause this to crash?"

## 4. Guided Hands-On Exercise: The "Hardening" Loop

*Goal: Take a raw function and make it production-ready.*

**Step 1**: Write a raw function (or copy this):

```javascript
function processUser(u) {
    return u.name.toUpperCase() + " is " + u.age;
}
```

**Step 2 (Types)**:

- `Cmd+K`: "Add Typescript interfaces/types to this."
- *Result*: `interface User { name: string; age: number }`.

**Step 3 (Safety)**:

- `Cmd+K`: "Add error handling if 'u' or 'u.name' is missing."
- *Result*: Try/Catch or Guard clauses.

**Step 4 (Docs & Tests)**:

- `Cmd+K`: "Add Docstring."
- Open Chat: "Write a Jest test for this function."

**Outcome**: You turned 3 lines of risky code into a robust, documented, tested artifact in 60 seconds.

## 5. Course Conclusion: The Practitioner’s Checklist

| Phase | Action | Tool |
| :--- | :--- | :--- |
| **Start** | Planning / Architecture | **Chat** |
| **Build** | Scaffolding Files | **Composer** (`Cmd+I`) |
| **Logic** | Writing/Editing Function | **Cmd+K** |
| **Flow** | Typing Speed | **Tab** |
| **Finish** | Docs & Tests | **Cmd+K** / **Chat** |

## 6. Final Words

Cursor is a tool that **amplifies intent**.

- If you have **no intent** (don't know what you want), it amplifies confusion.
- If you have **clear intent**, it removes the friction of syntax.

**Go build something.**
