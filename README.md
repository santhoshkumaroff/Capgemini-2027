# Capgemini 2027 Batch — Complete Interview & Assessment Prep Bank

Comprehensive prep material for Capgemini's fresher hiring process — covering every round shown in
the official slides, plus the typical HR/behavioral round most fresher hiring pipelines include.

## ⚠️ Read this first — how to use this repo honestly

Two kinds of content live here:

- **📌 Confirmed structure** — round names, number of questions, time limits, topics, languages,
  and evaluation criteria for the Technical Module, Debugging Assessment, and AI-Assisted Coding
  Assessment. This comes directly from Capgemini's own slides.
- **🔮 Practice questions & answers** — every question in Sections 1-4 is a predicted/standard
  practice question built to match the exact confirmed topics — not leaked real exam questions.
  Section 5 (HR/Behavioral) is a bonus addition not shown in your slides at all, included because
  most fresher pipelines include a human round like this.

Tell students plainly: confidence built on "I understand WHY this is the answer" transfers to the
real exam. Confidence built on "I memorized these exact 130+ questions" does not.

## What's in this bank (self-checked totals)

| Section | File | Content | Count |
|---|---|---|---|
| 1 | `01-ai-literacy.md` | MCQs: AI Foundations/GenAI, Prompt Engineering, Advanced AI Systems, Responsible AI | **40 MCQs** |
| 2 | `02-technical-assessment.md` | MCQs: Programming Logic, DSA, Software Engineering Fundamentals, Modern Engineering Awareness | **48 MCQs** |
| 3 | `03-debugging-assessment.md` | Fully worked buggy programs across Trees, Graphs, 2D DP, Advanced DSA in C/C++/Java, each with the confirmed Review→Identify→Fix→Validate method | **8 worked problems** |
| 4 | `04-ai-assisted-coding.md` | Full scaffolded-flow walkthroughs + prompt-quality training against the confirmed 4-criteria rubric | **6 full scenarios + 4 more listed for extra practice** |
| 5 | `05-hr-behavioral-bonus.md` | Common fresher HR/behavioral questions with answer structures (bonus — not from your slides) | **30 Q&A** |

**Total: ~130+ practice items**, every one with a plain-language explanation of *why*, not just an answer key.

## Question format (every MCQ follows this — by design)

1. Options
2. ✅ Correct answer
3. 💡 Plain-language explanation of why it's correct (and briefly why the others aren't)
4. 🎯 A short real-life analogy to anchor the concept in memory

This is slower to read once, but much faster to *recall* under exam pressure, because the student
understands the concept instead of memorizing a letter.

## Assessment structure (confirmed, from the official slides)

| Round | Format | Questions | Time | Topics |
|---|---|---|---|---|
| Technical Module — Sec 1: AI Literacy | MCQ | 20 | ~22.5 min | AI Foundations & GenAI, Prompt Engineering & AI Productivity, Advanced AI Systems, Responsible AI & Evaluation |
| Technical Module — Sec 2: Technical Assessment | MCQ | 20 | ~22.5 min | Programming Logic & Problem Solving, DSA, Software Engineering Fundamentals, Modern Engineering Awareness |
| Debugging Assessment | Code fix | 1 | ~20 min | C, C++, Java. Trees, Graphs, 2D DP, Advanced DSA. Review→Identify→Fix→Validate |
| AI-Assisted Coding Assessment | AI-assisted coding | Scaffolded, step-by-step | — | Evaluated on: AI literacy, prompt quality, problem-solving, review & adapt |

## Repo structure

```
README.md
sections/
  01-ai-literacy.md
  02-technical-assessment.md
  03-debugging-assessment.md
  04-ai-assisted-coding.md
  05-hr-behavioral-bonus.md
images/
  debugging-flow.svg             # 4-step debugging method, visual
  ai-assisted-coding-flow.svg    # 4-step AI-assisted coding flow, visual
```

Each section file links its relevant flowchart image inline — renders automatically on GitHub or
any Markdown viewer.

## How to run a mock session with students

1. **Sections 1 + 2 (MCQs):** 22-23 minutes each, no notes, real exam pressure. Afterward, review
   the ❌ "why wrong" explanations together — that's where the actual learning happens.
2. **Section 3 (Debugging):** Have students attempt each of the 8 problems **blind, on a 15-20 min
   timer**, before reading the explanation — narrating the 4 steps out loud as they work.
3. **Section 4 (AI-Assisted Coding):** Give access to an AI assistant, grade on **how** they
   prompted using the rubric table — not just whether the code worked.
4. **Section 5 (HR/Behavioral):** Run as mock interviews — one student asks, one answers, then swap.
   Push for specific real examples, not memorized scripts.

## Pushing this to GitHub
```
cd capgemini-2027-interview-prep
git init
git add .
git commit -m "Capgemini 2027 batch — full interview & assessment prep bank"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```
