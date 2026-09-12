[🏠 Home](../README.md) · [⬅ Previous: HR & Behavioral](./05-hr-behavioral-bonus.md)

---

# 🧵 Chapter 6 — Live Coding: Existing-Codebase Scenarios (MERN/React)

**📑 In this chapter:**

1. [Verified against real industry patterns](#verified)
2. [Prompt 1 — Bug Identification](#prompt-1)
3. [Prompt 2 — Feature Addition](#prompt-2)
4. [How to actually use this](#how-to-use)

[🔝 Jump to navigation ⬇](#-continue-reading) (bottom of page)

---

⚠️ **Read this before using either prompt below.** No prompt can guarantee a student clears this
round — that depends on their own understanding of React/MERN fundamentals, not just a good
template. What these prompts DO reliably do: force a full read of the code before responding,
separate *what's wrong* from *why* from *how to fix it* so nothing gets confusing, and force the
AI to distinguish confident findings from ones worth double-checking. Treat this chapter as a
tool that supports understanding, not a replacement for it — see the **"How to actually use this"**
section at the bottom before handing this to students.

**🔍 Source note:** This chapter's prompt structure was cross-checked against real, current
industry reporting (see "Verified against real industry patterns" below) on how this exact style
of round is run at major tech companies in 2026. It has not been verified against a Capgemini-specific
report of this precise round — this style doesn't appear on Capgemini's own confirmed slides at
all (see Chapters 1–4 for what's actually confirmed) — but the underlying pattern is well-documented
elsewhere and the evaluation criteria transfer directly.

---

<a id="verified"></a>
## ✅ Verified against real industry patterns

This exact round shape — read an existing codebase, diagnose or plan changes with AI as a guide,
but stay personally accountable for the reasoning — turns out to be a real, fast-growing pattern
across major tech companies in 2026, not something unique to what your students described. A few
findings worth knowing before you hand this to them:

**Google's new "Code Comprehension" round** (piloted May 2026, replacing a traditional coding round
for some SWE levels) evaluates three things: code reading ability, classical debugging skill
(forming hypotheses about the bug *independently*, before leaning on AI), and AI fluency — writing
precise prompts and validating what comes back. The internal framing is "human-led, AI-assisted" —
the candidate stays in charge, the AI is a tool, not a crutch.

**Meta's AI-assisted round** explicitly asks candidates to diagnose *why* a bug happened once
found — was the prompt unclear, or did the AI make an incorrect assumption? — and use that insight
to guide the next fix. This is exactly the reasoning discipline Prompt 1 below is built to force.

**A widely-cited industry analysis of debugging rounds** (covering Amazon's OA debugging sections,
Stripe's "Bug Squash," and Retool's failing-test format) makes a point worth repeating word for
word to your students: *the debugging round scores your process, not the fix.* The four dimensions
interviewers actually score are: **hypothesis discipline, reproduction, root-cause analysis, and
narration** — a methodical wrong hypothesis, explained clearly, scores better than a lucky silent
correct answer. The recommended loop is: **state expected vs. actual behavior → reproduce with
minimal input → rank hypotheses → test one at a time → apply the minimal fix → verify.**

**On the specific bug categories:** stale closures from missing `useEffect` dependencies are
confirmed, repeatedly, as one of the single most common real React bugs — independent engineering
sources, React's own GitHub issue tracker, and multiple 2026 debugging guides all converge on this
exact pattern. Prompt 1's specific callout of this category is well-founded, not a guess.

**What this changes about the prompts below:** the original versions already forced "read
everything first" and separated what/why/fix — but they didn't explicitly force **stating expected
vs. actual behavior** or **ranking multiple hypotheses before committing to one**, both of which
the real scoring rubrics above treat as core, separately-scored skills. Both prompts have been
updated below to include this.



## The scenario, restated

Two round types, both with the same hard constraint: **the AI can analyze and explain, but must
never output a rewritten file or make the edit itself** — the student has to understand the
guidance well enough to apply it by hand, line by line.

1. **Bug-finding round** — given a MERN/React file with bugs, identify each one, explain why it
   happens, and describe the fix in plain English.
2. **Feature-adding round** — given an existing codebase, analyze its structure first, then explain
   exactly where and how to add a new feature, step by step.

---

<a id="prompt-1"></a>
## Prompt 1 — Bug Identification (Read-Only Diagnosis)

```
You are acting as a code reviewer, NOT an editor. I will paste a React/MERN code file or
snippet below, along with what I expected it to do and what it's actually doing instead.
You must NOT rewrite the file or output a corrected version — describe every fix in plain
English only.

Do this instead:

1. Read through the ENTIRE file silently first before responding. Do not react to the first
   bug you spot — find all of them before writing your answer.

2. For each suspicious area, briefly list 2-3 possible hypotheses for what could be causing
   the described symptom BEFORE committing to a single diagnosis — then state which
   hypothesis you're most confident in and why you ruled out the others.

3. List every confirmed bug you find, one at a time, in this exact format:

   Bug #[number]
   - File/Component:
   - Line number(s): [quote the exact line]
   - Expected vs. actual: [what this code should do vs. what it actually does — restate
     this even if I already gave it, to confirm we're diagnosing the same symptom]
   - What's wrong: [logic error / syntax error / runtime error / wrong hook usage /
     stale closure / missing dependency / direct state mutation / etc.]
   - Why it happens: [plain-language root cause — what the code is doing incorrectly
     and why it leads to this specific symptom]
   - How to fix it: [describe the exact edit in plain English — e.g., "change X to Y
     on this line" or "add [variable] to the useEffect dependency array" — do NOT
     output a full corrected code block, only describe the precise change]
   - Confidence: [High confidence] or [Worth double-checking] — be honest here; don't
     present a guess with the same certainty as a clear-cut bug.

4. Number the bugs in the order they appear top to bottom in the file.

5. Pay specific attention to common React/MERN bug categories: stale state closures,
   missing/incorrect useEffect dependencies, direct state mutation instead of using
   setState, missing key props in lists, unhandled async/API errors, incorrect prop
   drilling, and backend issues in Express routes or MongoDB queries/schemas if
   backend code is included.

6. At the end, explicitly state: "I have checked the full file for additional issues
   beyond these" — and if you're not fully confident there are no more bugs, say so
   directly instead of guessing.

Here is the code: [PASTE CODE]
What I expected: [DESCRIBE EXPECTED BEHAVIOR]
What's actually happening: [DESCRIBE ACTUAL/BUGGY BEHAVIOR]
```

### Why it's built this way
- **"Read silently first"** stops the AI from reacting to the first bug it notices and stopping
  there — a known failure mode where later bugs get missed.
- **Expected-vs-actual framing and hypothesis-ranking (steps 1-2)** aren't just nice-to-haves —
  independent reporting on how major companies actually score this exact round (Google's Code
  Comprehension round, and analyses of Amazon/Stripe/Retool-style debugging rounds) converges on
  the same finding: interviewers score *hypothesis discipline and root-cause reasoning*, not just
  whether the final answer was right. A student who states expected-vs-actual and considers
  multiple hypotheses out loud is demonstrating exactly what's being scored — a lucky right answer
  with no reasoning trail scores worse than a well-reasoned near-miss.
- **Separating What/Why/Fix** prevents the dense, confusing run-on explanations we specifically
  fixed earlier in this book (see Chapters 1–2) — the student can scan straight to the piece they need.
- **The Confidence field** is the single most important addition: it stops a student from repeating
  a *wrong* AI diagnosis with full confidence in a live interview. If the AI flags something
  "Worth double-checking," the student knows to reason through it themselves before stating it out loud.
- **The explicit "no rewritten file" instruction** is what actually enforces your constraint — most
  AI assistants default to just fixing code unless told firmly not to.

---

<a id="prompt-2"></a>
## Prompt 2 — Feature Addition (Analysis + Step-by-Step Guidance)

```
You are acting as a senior developer mentoring me, NOT an auto-code generator. I have an
existing codebase and want to add a new feature. Do NOT write the feature's code for me or
output modified files — every instruction must be plain-English guidance I apply myself.

Do this instead:

1. First analyze the codebase I paste below and briefly summarize: the overall structure
   (which files/components exist), how data flows (state management, API calls, routes,
   models/schemas), and which existing parts are relevant to the feature I want to add.

2. Identify EXACTLY which file(s) need to change, and explain why each one is relevant.

3. For each file, give me:
   - File name:
   - Where to make the change: [exact function/component name, or the nearest existing
     code block to anchor the change to]
   - What to add/change: [step-by-step, plain-English description of the logic, JSX,
     state, API route, or schema field to add]
   - Why this goes here: [reasoning tied to the existing architecture]
   - Confidence: [High confidence] or [Worth double-checking] — flag anything that depends
     on assumptions about parts of the codebase I haven't shown you.

4. Order the steps the way I should actually implement them (e.g., backend schema/model
   first → API route → frontend state → UI component).

5. End with a short checklist I can use to verify I've implemented every piece correctly.

6. Do NOT generate a full rewritten file or a code diff — every instruction should be
   specific enough that I can type the change myself, but stay in plain-English guidance
   form, not code handed to me to paste in.

Here is my existing code: [PASTE CODE]
Feature I want to add: [DESCRIBE FEATURE]
```

### Why it's built this way
- **Forcing architecture analysis before implementation guidance** mirrors real feature work —
  you can't tell someone the "right place" to add something without first understanding how data
  already flows through the app.
- **Implementation ordering (schema → route → state → UI)** reflects how MERN features are
  actually built in practice — backend-first — and teaches that sequencing as a habit, not just a
  one-off answer.
- **The Confidence field here does something specific:** it flags guidance based on assumptions
  about code the student *didn't* paste (e.g., a file the AI is inferring exists but hasn't seen) —
  a very real risk in partial-codebase scenarios.
- **The final checklist** gives the student something concrete to self-verify against once they've
  made the changes by hand — closing the loop instead of leaving them unsure if they did it right.

---

<a id="how-to-use"></a>
## How to actually use this (read this part — it matters most)

A prompt template raises the *ceiling* of what a student can do with AI assistance in this round.
It does not raise their *floor* — that's set by how well they actually understand React/MERN.
Two things make the real difference between a student who clears this round and one who doesn't:

1. **Can they defend the diagnosis in their own words?** If the AI says "line 12 has a stale
   closure bug," and the interviewer asks "why does that happen?", a student who can't answer
   independently of the AI's explanation will struggle — regardless of how good the prompt was.
2. **Have they rehearsed this exact flow before the real interview?** Reading these two prompts
   once is not practice. Running them against 8-10 real buggy MERN snippets beforehand — and
   personally checking whether the AI's "Confidence: High" bugs are actually correct — is what
   builds the muscle memory and judgment this round is testing for.
3. **Can they narrate their reasoning out loud, live?** This is worth stressing directly to
   students: real reporting on this round style is explicit that interviewers score *narration* —
   saying the hypothesis, the reasoning, and the ranking out loud — as a separately-scored skill,
   not just a nice-to-have communication habit. A student who silently reads the AI's output and
   then states the final answer is not demonstrating the same thing as one who says "I'm
   considering two possibilities here — a stale closure or a missing dependency — let me check
   which one actually matches the symptom" before landing on the answer. Practice saying the
   diagnosis out loud, not just producing it.

**Recommended practice loop:**
1. Take a real MERN component (or write one with 2-3 deliberate bugs — stale closures, missing
   `key` props, direct state mutation, a missing `useEffect` dependency, an unhandled fetch error).
2. State the expected vs. actual behavior out loud, as if explaining it to an interviewer.
3. Run Prompt 1 against it.
4. Before accepting any answer, have the student explain WHY each flagged bug is actually a bug —
   in their own words, out loud, no AI help.
5. Repeat with a small existing component + a feature request, using Prompt 2.

## 🔎 Sources
- ["Google's AI-Assisted Coding Interview (2026 Guide)"](https://www.tryexponent.com/blog/google-ai-coding-interview) — Exponent, on Google's new "Code Comprehension" round (piloted May 2026)
- ["How to use AI in Meta's AI-assisted coding interview"](https://interviewing.io/blog/how-to-use-ai-in-meta-s-ai-assisted-coding-interview-with-real-prompts-and-examples) — interviewing.io
- ["The Debugging Round Interview Scores Your Process, Not the Fix"](https://spacecomplexity.ai/blog/debugging-round-interview) — SpaceComplexity, on Amazon/Stripe/Retool-style debugging rounds and the 4 scored dimensions
- ["AI-Assisted Coding Interviews (how to prepare)"](https://igotanoffer.com/en/advice/ai-assisted-coding-interview) — IGotAnOffer, on the reproduce → isolate → hypothesize → fix → verify loop
- Multiple 2026 engineering sources (CoreUI, LogRocket, AlexWebLab, DEV Community) independently confirming stale closures from missing `useEffect` dependencies as one of the most common real React bugs

This round style does not appear on Capgemini's own confirmed assessment slides (see Chapters 1–4)
— it's a broader industry pattern this chapter borrows evaluation criteria from, since it matches
what your students described. If Capgemini runs a Capgemini-specific version of this round with
different rules, treat this chapter as strong general preparation, not a guarantee of an exact match.


---

<a id="-continue-reading"></a>
## Continue reading

[🏠 Home](../README.md) · [⬅ Previous: HR & Behavioral](./05-hr-behavioral-bonus.md)
