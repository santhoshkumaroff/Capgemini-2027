[🏠 Home](../README.md) · [Next: Technical Assessment ➡](./02-technical-assessment.md)

---

# 🤖 Chapter 1 — AI Literacy

**📑 In this chapter:**

1. [Topic 1: AI Foundations & Generative AI (Q1–Q10)](#topic-1)
2. [Topic 2: Prompt Engineering & AI Productivity (Q11–Q20)](#topic-2)
3. [Topic 3: Advanced AI Systems (Q21–Q30)](#topic-3)
4. [Topic 4: Responsible AI & AI Evaluation (Q31–Q40)](#topic-4)

[🔝 Jump to navigation ⬇](#-continue-reading) (bottom of page)

---

🔮 **Source note:** Practice questions matched to Capgemini's confirmed topic list. Not leaked real
exam questions — built for volume + understanding, not memorization.

**How every question is laid out below (same structure, every single time):**
Options → ✅ Correct Answer → 💡 Why it's correct → ❌ Why each other option is wrong → 🎯 Real-life example.

---

<a id="topic-1"></a>
## Topic 1: AI Foundations & Generative AI (Q1–Q10)

### Q1. What is a "foundation model"?

- **A.** A small model trained for one narrow task
- **B.** A large model pre-trained on broad data that can be adapted to many downstream tasks
- **C.** A rule-based expert system
- **D.** A database indexing algorithm

**✅ Correct Answer: B**

**💡 Why:** Foundation models learn broadly first — from a massive, diverse dataset covering
language, code, and reasoning patterns — and are only afterward adapted to specific jobs. That
broad-then-specific structure is exactly what makes it a "foundation."

**❌ Why not the others:**
- **A** describes a narrow, task-specific model — the opposite of "foundation."
- **C** describes hand-written if-then rules, not patterns learned from data.
- **D** is an unrelated database concept.

**🎯 Example:** A fresh engineering graduate with broad general knowledge (the foundation model),
who later specializes in one domain during their first job (fine-tuning).

---

### Q2. What does "LLM" stand for?

- **A.** Large Language Model
- **B.** Linear Learning Machine
- **C.** Logical Language Module
- **D.** Layered Learning Model

**✅ Correct Answer: A**

**💡 Why:** It's literal — "Large" (trained on huge amounts of data), "Language" (works with human
language/code), "Model" (a system that learned patterns from that data).

**❌ Why not the others:**
- **B, C, D** are invented-sounding expansions with no real meaning here — a classic distractor
  pattern. If you don't recognize the acronym, don't guess based on "sounds technical."

**🎯 Example:** ChatGPT, Claude, and Gemini are all LLMs — that's the category name for what kind of AI they are.

---

### Q3. Which of these is a well-known LIMITATION of current LLMs?

- **A.** They can process text instantly
- **B.** They can "hallucinate" — generate plausible-sounding but false information
- **C.** They cannot be used for text generation
- **D.** They only work with images

**✅ Correct Answer: B**

**💡 Why:** Hallucination means the model states something confidently and fluently — a fact, a
citation, a function name — that is simply wrong or doesn't exist. It happens because the model
predicts "what sounds plausible next," not because it checks a verified fact database.

**❌ Why not the others:**
- **A** describes speed, a strength, not a limitation — and isn't what this question is testing.
- **C** directly contradicts the definition of an LLM, which is built for text generation.
- **D** is false; LLMs primarily work with text (some are also multimodal).

**🎯 Example:** Asking an LLM for a legal case citation and getting a completely fake case name that sounds 100% real.

---

### Q4. Generative AI primarily differs from traditional predictive AI/ML because it:

- **A.** Only classifies existing data into categories
- **B.** Creates new content (text, images, code, audio) rather than just predicting a label
- **C.** Cannot be trained on text data
- **D.** Only works with structured/tabular data

**✅ Correct Answer: B**

**💡 Why:** Traditional ML usually answers "which category does this belong to?" Generative AI
instead produces brand-new output — a paragraph, an image, a snippet of code — that didn't exist before you asked for it.

**❌ Why not the others:**
- **A** describes classification — a predictive ML task, not generative AI.
- **C** is false; LLMs are commonly trained on huge amounts of text.
- **D** is false; generative AI works mainly with unstructured data (text, images, audio).

**🎯 Example:** A predictive model tells you "this email is spam" (a label). A generative model writes you a whole new email from scratch.

---

### Q5. What is "training data" in the context of an LLM?

- **A.** The test cases used to debug the model's code
- **B.** The large corpus of text/data the model learns patterns from before deployment
- **C.** The user's live chat history only
- **D.** A database of only labeled classification data

**✅ Correct Answer: B**

**💡 Why:** Before an LLM is ever released, it "reads" an enormous amount of text (books, websites,
code, articles) and learns statistical patterns of language from it — that's what shapes everything it later produces.

**❌ Why not the others:**
- **A** is a software-testing concept, unrelated to how a model learns.
- **C** is a small, separate thing that happens after training, during actual use.
- **D** is mostly false — LLM training data is largely unlabeled raw text.

**🎯 Example:** A student who has read thousands of books before the exam — that reading is the training data; the exam is the model being used afterward.

---

### Q6. A key capability of modern LLMs is:

- **A.** Perfect factual accuracy on all topics, all the time
- **B.** Few-shot learning — adapting to a new task from just a few examples in the prompt
- **C.** Guaranteed real-time internet access by default
- **D.** Immunity to biased outputs

**✅ Correct Answer: B**

**💡 Why:** Show the model 2-3 examples of the input/output pattern you want, and it can often pick
up the pattern and apply it to something new — without being retrained.

**❌ Why not the others:**
- **A** is false — see Q3, hallucination proves LLMs aren't perfectly accurate.
- **C** is false unless the model is specifically connected to a search/RAG tool.
- **D** is false — bias comes from training data (see Topic 4) and models aren't immune to it.

**🎯 Example:** Show the AI 2 examples of "convert this sentence to formal English," and the 3rd sentence follows the same style automatically.

---

### Q7. What best distinguishes a "base model" from a "fine-tuned model"?

- **A.** There is no difference
- **B.** A base model is broadly pre-trained; a fine-tuned model is further trained on a narrower, specific dataset/task
- **C.** Fine-tuned models are always smaller
- **D.** Base models can't generate text

**✅ Correct Answer: B**

**💡 Why:** Fine-tuning takes the broad foundation model and specializes it further — for example,
for a particular tone, domain, or task like coding-only assistance.

**❌ Why not the others:**
- **A** is false — this question exists precisely because there is a meaningful difference.
- **C** is a false generalization — fine-tuning doesn't inherently shrink a model.
- **D** is false — base models can generate text; that's their core function.

**🎯 Example:** A general doctor (base model) who later specializes in cardiology (fine-tuning).

---

### Q8. What does "context window" refer to in an LLM?

- **A.** The physical screen size
- **B.** The maximum amount of text (tokens) the model can consider at once when generating a response
- **C.** A UI setting for font
- **D.** The model's training duration

**✅ Correct Answer: B**

**💡 Why:** If a conversation or document exceeds this limit, the model literally cannot "see" the
parts that fall outside it — older content gets pushed out to make room for new content.

**❌ Why not the others:**
- **A, C, D** are all unrelated concepts — screen size, UI settings, and training time have nothing to do with how much text a model can process at once.

**🎯 Example:** A whiteboard of limited size — once it's full, older notes have to be erased to fit new ones.

---

### Q9. Why do LLMs sometimes give different answers to the same prompt asked twice?

- **A.** They are broken
- **B.** Many LLMs use some randomness (sampling/"temperature") in generation, so outputs can vary
- **C.** They always give identical answers
- **D.** Only image models vary

**✅ Correct Answer: B**

**💡 Why:** Temperature/sampling settings intentionally introduce controlled randomness so
responses aren't robotically identical every time — this is by design, not a malfunction.

**❌ Why not the others:**
- **A** wrongly treats intended behavior as a malfunction.
- **C** is simply false, and contradicts what the question is asking about.
- **D** is false — this variability applies broadly, not only to image models.

**🎯 Example:** Asking a knowledgeable friend the same question twice — the core facts stay similar, but the exact phrasing varies.

---

### Q10. What is "tokenization" in the context of LLMs?

- **A.** Creating cryptocurrency tokens
- **B.** Breaking text into smaller units (words/sub-words) the model processes numerically
- **C.** A security login method
- **D.** Compressing an image file

**✅ Correct Answer: B**

**💡 Why:** Before an LLM can process text, it splits it into tokens (whole words or word-pieces)
and converts them into numbers it can compute with.

**❌ Why not the others:**
- **A** and **C** are unrelated concepts borrowed from other domains (finance, security).
- **D** is a different technical concept (image compression, not text processing).

**🎯 Example:** Chopping a sentence into puzzle pieces before feeding it into a machine that only understands pieces, not whole sentences.

---

<a id="topic-2"></a>
## Topic 2: Prompt Engineering & AI Productivity (Q11–Q20)

### Q11. Which of the following is the BEST example of a well-structured prompt?

- **A.** "fix this"
- **B.** "Write code"
- **C.** "Write a Python function that takes a list of integers and returns the second-largest value; handle the case where the list has fewer than 2 elements by returning None."
- **D.** "help me"

**✅ Correct Answer: C**

**💡 Why:** It specifies the language, the exact task, the input type, the expected output, and
what to do in a tricky edge case — all five elements of a genuinely usable prompt.

**❌ Why not the others:**
- **A, B, D** are all vague — none of them say what language, what the input/output is, or what
  "this" even refers to, forcing the AI to guess.

**🎯 Example:** Asking a colleague "this function crashes on empty input, please add a check" gets a correct fix faster than just saying "fix this."

---

### Q12. "Context setting" in prompt engineering refers to:

- **A.** Changing the font size in the prompt
- **B.** Giving the AI relevant background information (role, constraints, format) before asking the actual question
- **C.** Deleting the chat history
- **D.** Using only single-word prompts

**✅ Correct Answer: B**

**💡 Why:** Before asking the real question, you set the stage — role, domain, tone constraints —
and that context shapes every answer that follows.

**❌ Why not the others:**
- **A** and **D** are surface-level and unrelated to meaning.
- **C** is the literal opposite of context-setting — it removes context instead of adding it.

**🎯 Example:** Telling a new intern "we're a healthcare company, avoid casual language" before assigning a writing task.

---

### Q13. GitHub Copilot is best described as:

- **A.** A version control system
- **B.** An AI pair-programming tool that suggests code completions based on context
- **C.** A cloud hosting platform
- **D.** A database management tool

**✅ Correct Answer: B**

**💡 Why:** Copilot sits inside your code editor and suggests the next lines of code as you type,
based on what you've already written and the surrounding context.

**❌ Why not the others:**
- **A** describes Git — a different (related) tool Copilot works alongside.
- **C** describes something like AWS/Azure — unrelated to Copilot's function.
- **D** describes tools like MySQL Workbench — also unrelated.

**🎯 Example:** You type `def calculate_tax(` and Copilot suggests a plausible function body — you accept, edit, or reject it.

---

### Q14. Which practice IMPROVES prompt quality the most?

- **A.** Keeping prompts as short and ambiguous as possible
- **B.** Giving examples of desired input/output format (few-shot prompting)
- **C.** Never specifying constraints
- **D.** Repeating the exact same prompt if the first output is wrong, without any changes

**✅ Correct Answer: B**

**💡 Why:** Showing the AI 1-2 examples of exactly what "good" looks like removes guesswork — it's
the single highest-leverage prompting technique for consistent, correctly-formatted output.

**❌ Why not the others:**
- **A** and **C** make the prompt vaguer, producing worse output.
- **D** wastes a turn — if output was wrong, the prompt needs to change (add detail, fix a
  misunderstanding), not repeat identically.

**🎯 Example:** "Format each answer like this: Q: ... A: ..." plus one worked example — the AI then follows that format consistently.

---

### Q15. In AI-assisted problem solving, what should you do FIRST if the AI's output is wrong?

- **A.** Immediately copy-paste it into production
- **B.** Review the output critically, identify what's wrong, and refine the prompt with more specific context
- **C.** Give up on the task
- **D.** Ask an unrelated question

**✅ Correct Answer: B**

**💡 Why:** Wrong output tells you the AI was missing context or misunderstood something — the
productive move is to diagnose the gap and fix the prompt.

**❌ Why not the others:**
- **A** is dangerous — shipping known-wrong code.
- **C** and **D** both avoid solving the actual problem instead of addressing it.

**🎯 Example:** If a teammate's first draft has an error, you point out the specific issue and ask for a revision — you don't publish it as-is or scrap the whole project.

---

### Q16. What is "chain-of-thought" prompting?

- **A.** Asking the AI to skip explaining and just give the final answer
- **B.** Asking the AI to reason step-by-step before giving a final answer, improving accuracy on complex tasks
- **C.** Linking multiple unrelated prompts randomly
- **D.** A type of database chaining

**✅ Correct Answer: B**

**💡 Why:** Explicitly asking for step-by-step reasoning forces intermediate reasoning instead of a
rushed jump to a conclusion — this often improves accuracy on multi-step logic or math problems.

**❌ Why not the others:**
- **A** is the opposite approach — skipping reasoning tends to hurt accuracy on complex tasks.
- **C** and **D** are unrelated, made-up-sounding distractors.

**🎯 Example:** Asking a student to "show your working" on a math problem instead of just writing the final number — mistakes become visible and fixable.

---

### Q17. What's a "system prompt" typically used for?

- **A.** Displaying an error message
- **B.** Setting persistent instructions/behavior/role for the AI throughout a conversation, separate from the user's individual messages
- **C.** A one-time joke prompt
- **D.** Formatting the screen resolution

**✅ Correct Answer: B**

**💡 Why:** It establishes the AI's role, tone, and constraints up front, applying to the whole conversation rather than being repeated every message.

**❌ Why not the others:**
- **A, C, D** are unrelated to how AI instructions actually persist across a conversation.

**🎯 Example:** A company handing a new support agent a standing set of guidelines before they start taking calls — those guidelines apply to every call, not just the first.

---

### Q18. Why might a very long, unstructured prompt actually produce worse output than a shorter, well-organized one?

- **A.** Length always improves output quality
- **B.** Important instructions can get buried or diluted among irrelevant detail, making the actual ask unclear
- **C.** AI models cannot read long prompts at all
- **D.** There is no difference ever

**✅ Correct Answer: B**

**💡 Why:** Clarity and structure matter more than raw length — burying the actual task in unrelated detail makes it harder for the model to identify what you actually want.

**❌ Why not the others:**
- **A** and **D** are absolute claims that don't hold up — structure matters, not just length.
- **C** is factually false — models can process long prompts, just not infinitely long ones (see Q8).

**🎯 Example:** A cluttered work email with the real ask buried in paragraph 5, versus a clear email stating the ask up top.

---

### Q19. What does "zero-shot prompting" mean?

- **A.** Giving the AI many worked examples first
- **B.** Asking the AI to perform a task with no prior examples given, relying only on the instruction itself
- **C.** A failed prompt
- **D.** Only used for image generation

**✅ Correct Answer: B**

**💡 Why:** "Zero" examples given — you describe the task directly and the model attempts it based
on general training, contrasted with "few-shot" (Q14), which gives examples.

**❌ Why not the others:**
- **A** describes few-shot prompting, the opposite concept.
- **C** and **D** are incorrect — zero-shot isn't a failure state, and it applies broadly, not just to images.

**🎯 Example:** Asking someone to "translate this sentence to French" with no example translation shown first.

---

### Q20. Which is a red flag of a LOW-quality AI-assisted coding prompt?

- **A.** Specifying the exact function signature and edge cases
- **B.** Pasting the raw problem statement with zero added structure and accepting the first output without review
- **C.** Asking the AI to explain its approach before coding
- **D.** Requesting test cases alongside the code

**✅ Correct Answer: B**

**💡 Why:** No structure, no review — this is exactly the anti-pattern Capgemini's AI-Assisted
Coding round evaluates against (see Chapter 4).

**❌ Why not the others:**
- **A, C, D** are all good practices, not red flags.

**🎯 Example:** Copy-pasting a whole assignment into an AI and turning in whatever comes out first, unread.

---

<a id="topic-3"></a>
## Topic 3: Advanced AI Systems (Q21–Q30)

### Q21. What does RAG stand for?

- **A.** Rapid Application Generation
- **B.** Retrieval-Augmented Generation
- **C.** Random Access Gateway
- **D.** Recursive Algorithm Graph

**✅ Correct Answer: B**

**💡 Why:** RAG has two parts — **Retrieval** (fetch real, relevant documents) and **Generation**
(the LLM answers using that content) — grounding answers in real data instead of relying purely on memorized training data.

**❌ Why not the others:**
- **A, C, D** are invented-sounding expansions with no real meaning in this context.

**🎯 Example:** Instead of guessing your company's leave policy from memory, the system pulls the actual current HR document first, then answers from it.

---

### Q22. An "AI agent" is best described as:

- **A.** A static chatbot that only answers one question at a time with no memory
- **B.** A system that can autonomously plan, use tools, and take multi-step actions to achieve a goal
- **C.** A type of database index
- **D.** A hardware component

**✅ Correct Answer: B**

**💡 Why:** Agents break a goal into steps, decide to use tools (search, calculators, APIs), check
results, and decide the next step — looping until the goal is done.

**❌ Why not the others:**
- **A** describes a basic chatbot — the opposite of agentic behavior.
- **C** and **D** are unrelated technical terms borrowed from other domains.

**🎯 Example:** "Book me the cheapest flight to Delhi Friday" — an agent searches, compares, checks your calendar, and books — multiple autonomous steps.

---

### Q23. Why is RAG useful for reducing hallucination?

- **A.** It makes the model bigger
- **B.** It grounds the model's response in retrieved, real documents instead of relying purely on memorized training data
- **C.** It removes the need for any training data
- **D.** It slows down responses on purpose

**✅ Correct Answer: B**

**💡 Why:** Hallucination (Q3) happens because the model relies on its "memory" of training data,
which can be outdated or blended incorrectly. RAG hands the model real source text to work from instead.

**❌ Why not the others:**
- **A** and **D** are irrelevant side-effects, not the actual reason.
- **C** is false — RAG systems still need a trained LLM underneath; retrieval supplements it.

**🎯 Example:** An open-book exam (RAG — you can check the textbook) vs. a closed-book exam from memory alone.

---

### Q24. A "multi-step AI workflow" typically involves:

- **A.** A single prompt-response with no further steps
- **B.** Breaking a complex task into subtasks, where the AI (or agent) may use tools, call APIs, or chain reasoning steps
- **C.** Only image generation
- **D.** Manual-only processing with no AI involvement

**✅ Correct Answer: B**

**💡 Why:** Complex real-world tasks rarely get solved in one shot — a multi-step workflow chains
smaller steps together, where the output of one feeds into the next.

**❌ Why not the others:**
- **A** is the opposite (single-step, not multi-step).
- **C** narrows the concept to one specific use case incorrectly.
- **D** removes AI entirely, contradicting the term.

**🎯 Example:** The AI-Assisted Coding round itself is a multi-step workflow: understand → propose approach → generate code → review & fix.

---

### Q25. What is a "vector database" commonly used for in AI systems?

- **A.** Storing plain text logs only
- **B.** Storing numeric representations (embeddings) of content so similar items can be found via similarity search
- **C.** Managing user passwords
- **D.** Compiling source code

**✅ Correct Answer: B**

**💡 Why:** Embeddings capture semantic meaning as numbers; a vector database lets you quickly find
content "similar in meaning" to a query — this is how RAG systems retrieve relevant documents.

**❌ Why not the others:**
- **A, C, D** describe unrelated storage/functionality concepts.

**🎯 Example:** Finding songs "similar in vibe" to one you like, based on numeric features of the song, rather than matching exact titles.

---

### Q26. What does "grounding" mean in the context of AI-generated answers?

- **A.** Powering off the AI
- **B.** Basing the AI's response on verifiable external data/sources rather than pure model memory
- **C.** A hardware safety feature
- **D.** Limiting response length

**✅ Correct Answer: B**

**💡 Why:** Grounding is closely tied to RAG (Q21/Q23) — tying answers to something checkable
reduces the risk of confident-but-wrong output.

**❌ Why not the others:**
- **A, C, D** are all unrelated concepts with no connection to answer verifiability.

**🎯 Example:** A journalist citing an actual document instead of writing purely from memory.

---

### Q27. What's the main risk of giving an AI agent too much autonomy without human checkpoints?

- **A.** There is no risk
- **B.** It may take incorrect or unintended multi-step actions before a human notices and can correct it
- **C.** It will always refuse to act
- **D.** It becomes slower

**✅ Correct Answer: B**

**💡 Why:** More autonomous steps without review means errors can compound across steps before
anyone catches them — this is exactly why human-in-the-loop checkpoints matter for high-stakes agent actions.

**❌ Why not the others:**
- **A** dismisses a real, well-documented risk.
- **C** and **D** are unrelated/false claims about agent behavior.

**🎯 Example:** An autopilot flying without any pilot oversight — small early errors can compound before anyone intervenes.

---

### Q28. Which best describes "tool use" by an AI agent?

- **A.** The AI edits its own source code permanently
- **B.** The AI calls external functions/APIs (like a calculator, search engine, or database) to get information or take an action it can't do purely through text generation
- **C.** The AI only uses tools for image generation
- **D.** Tool use means the AI has no limitations at all

**✅ Correct Answer: B**

**💡 Why:** LLMs can't natively do things like perfectly precise real-time math or fetch live data —
tools extend capability by letting the AI call specialized functions.

**❌ Why not the others:**
- **A** describes something LLMs don't do (self-modifying source code).
- **C** wrongly narrows the concept to one use case.
- **D** is false — tool use doesn't remove limitations, it works around specific ones.

**🎯 Example:** A person who doesn't do long division in their head but reaches for a calculator when needed.

---

### Q29. In a multi-step AI workflow, why is it useful to have the AI "show its plan" before executing?

- **A.** It isn't useful
- **B.** It lets a human review and catch a flawed approach before time/resources are spent executing it
- **C.** It only matters for image generation
- **D.** Plans are always guaranteed correct

**✅ Correct Answer: B**

**💡 Why:** Reviewing the plan first is cheaper than discovering a flawed approach after several steps have already run.

**❌ Why not the others:**
- **A** and **C** dismiss or wrongly narrow a genuinely useful, broadly-applicable practice.
- **D** is false — plans can absolutely be flawed, which is exactly why review matters.

**🎯 Example:** Approving a project plan before construction begins, rather than after the building is already half-built.

---

### Q30. What differentiates "Agentic AI" from a simple chatbot?

- **A.** Nothing, they're identical
- **B.** Agentic AI can independently decide on and execute a sequence of actions toward a goal, not just respond to single queries
- **C.** Agentic AI only works offline
- **D.** Chatbots are always more capable

**✅ Correct Answer: B**

**💡 Why:** This echoes Q22's definition — the "agentic" quality is about autonomous multi-step action, not just single-turn response.

**❌ Why not the others:**
- **A** and **D** are false — there is a meaningful, well-defined difference, and agentic systems typically extend rather than reduce capability.
- **C** is an unrelated, made-up claim.

**🎯 Example:** A chatbot answers "what's the weather" when asked. An agentic system told "plan my outdoor trip this weekend" could autonomously check weather, suggest dates, and draft an itinerary.

---

<a id="topic-4"></a>
## Topic 4: Responsible AI & AI Evaluation (Q31–Q40)

### Q31. Why is "output validation" important when using AI-generated content/code?

- **A.** It isn't — AI output is always correct
- **B.** AI can produce plausible but incorrect, insecure, or biased output, so a human should verify it before use
- **C.** It only matters for image generation
- **D.** It's only relevant for non-technical tasks

**✅ Correct Answer: B**

**💡 Why:** Confident-sounding output isn't the same as correct output (see Q3). A human should
check that the output actually works, is secure, and is fair before relying on it.

**❌ Why not the others:**
- **A** directly contradicts a well-established limitation of AI models.
- **C** and **D** arbitrarily narrow the scope — validation matters across text, code, and images alike.

**🎯 Example:** AI-generated code that "looks right" but has a SQL injection vulnerability — only review catches it.

---

### Q32. "Bias" in an AI model typically originates from:

- **A.** The model's color scheme
- **B.** Patterns (including unfair or skewed patterns) present in the training data
- **C.** The user's internet speed
- **D.** The programming language used to build the model

**✅ Correct Answer: B**

**💡 Why:** Models learn from the data they're shown — if that data has historical imbalances, the
model can pick up and repeat those same imbalances in its output.

**❌ Why not the others:**
- **A, C, D** are technical or unrelated factors with no real connection to how bias forms.

**🎯 Example:** A resume-screening model trained mostly on past hires from one group may unintentionally favor that group's resume patterns going forward.

---

### Q33. Which is a responsible AI practice?

- **A.** Blindly trusting AI output in high-stakes decisions (medical, legal, financial) without human review
- **B.** Disclosing when content is AI-generated where relevant, and reviewing output for accuracy and fairness
- **C.** Never testing AI output
- **D.** Ignoring data privacy when feeding prompts

**✅ Correct Answer: B**

**💡 Why:** Responsible AI use means staying transparent about AI involvement, keeping a human in
the loop for important decisions, and actively checking for accuracy/fairness issues.

**❌ Why not the others:**
- **A, C, D** each skip a necessary safeguard — these are exactly the irresponsible practices this topic tests you to recognize.

**🎯 Example:** A doctor using AI to draft notes still reviews and signs off on the final medical decision.

---

### Q34. What is a practical way to evaluate an AI-generated code snippet before using it?

- **A.** Assume it's correct since it compiles
- **B.** Read it, test it against edge cases, and check it doesn't introduce security/logic issues
- **C.** Never look at it
- **D.** Only check that it "looks professional"

**✅ Correct Answer: B**

**💡 Why:** Compiling only proves the syntax is valid — it says nothing about whether the logic is correct or safe.

**❌ Why not the others:**
- **A** confuses "compiles" with "correct" — a very common fresher mistake.
- **C** and **D** skip actual verification entirely.

**🎯 Example:** Code that compiles fine but crashes the moment you pass it an empty list — only testing the edge case catches it.

---

### Q35. Why should sensitive/confidential data generally NOT be pasted into a public AI chat tool?

- **A.** It makes the AI slower
- **B.** It may be logged, used for training, or exposed — creating a data privacy/security risk
- **C.** AI tools cannot process sensitive data at all
- **D.** There's no reason, it's completely safe

**✅ Correct Answer: B**

**💡 Why:** Depending on the tool's settings, data you type in can be stored or reviewed —
a real privacy/compliance risk for confidential company or personal data.

**❌ Why not the others:**
- **A** is a made-up, irrelevant consequence.
- **C** and **D** are both false — AI tools CAN process sensitive data, which is exactly why the risk in B is real.

**🎯 Example:** Pasting a real customer's ID number into a public AI chatbot "to summarize" — a data leak risk most companies explicitly guard against.

---

### Q36. What is "AI explainability" (or interpretability)?

- **A.** Making an AI model talk louder
- **B.** The degree to which humans can understand WHY a model produced a particular output or decision
- **C.** A model's marketing description
- **D.** The model's file size

**✅ Correct Answer: B**

**💡 Why:** Especially important in high-stakes domains (finance, healthcare, hiring), where a
black-box decision without any reasoning trail is hard to trust or audit.

**❌ Why not the others:**
- **A, C, D** are unrelated concepts with no connection to understanding model decisions.

**🎯 Example:** A loan rejection with a reason ("insufficient credit history") is more trustworthy than a bare "no" with zero explanation.

---

### Q37. What does "human-in-the-loop" mean in an AI system design?

- **A.** A human physically sits inside a server room
- **B.** A human reviews, approves, or can override AI decisions/outputs at key points, rather than the AI acting fully autonomously
- **C.** It means no AI is used at all
- **D.** It's a hardware specification

**✅ Correct Answer: B**

**💡 Why:** This is the standard safeguard against fully autonomous AI errors going unchecked, especially for consequential decisions.

**❌ Why not the others:**
- **A** and **D** take the phrase literally instead of as the design principle it is.
- **C** is false — human-in-the-loop specifically means AI IS used, alongside human oversight.

**🎯 Example:** An AI drafts a customer refund decision, but a support agent reviews and approves it before it's processed.

---

### Q38. Which scenario best illustrates a responsible-AI FAILURE?

- **A.** A team tests AI-generated code against edge cases before deploying
- **B.** A team ships AI-written financial advice directly to customers with no human review or disclosure that it's AI-generated
- **C.** A team discloses AI involvement in a report
- **D.** A team double-checks AI facts before publishing

**✅ Correct Answer: B**

**💡 Why:** No human review + no disclosure + a high-stakes domain (financial advice) — this
combination is exactly what Responsible AI practices exist to prevent.

**❌ Why not the others:**
- **A, C, D** all describe GOOD responsible-AI practices, not failures.

**🎯 Example:** An unreviewed AI chatbot telling a customer to make a specific investment decision with no advisor oversight.

---

### Q39. Why is it risky to assume an AI model's confidence (how certain it "sounds") reflects its actual accuracy?

- **A.** It's not risky, confidence always equals accuracy
- **B.** LLMs can state incorrect information with the same fluent, confident tone as correct information — tone is not a reliability signal
- **C.** AI models never sound confident
- **D.** This only applies to voice assistants

**✅ Correct Answer: B**

**💡 Why:** This connects directly to hallucination (Q3) — a wrong answer and a right answer can
both be phrased with identical, fluent confidence, so tone should never be mistaken for a correctness guarantee.

**❌ Why not the others:**
- **A** is false and is exactly the risky assumption this question warns against.
- **C** and **D** are factually incorrect and don't address the actual concept.

**🎯 Example:** A person who speaks very assertively isn't necessarily more correct than someone who hedges — the same logic applies to AI output.

---

### Q40. What is a reasonable organizational policy response to the risk of AI hallucination in customer-facing content?

- **A.** Ban AI use entirely with no exceptions
- **B.** Require human review/fact-checking of AI-generated content before it reaches customers, especially for factual claims
- **C.** Publish all AI output instantly with no checks
- **D.** Only check AI output once a year

**✅ Correct Answer: B**

**💡 Why:** A balanced response keeps the productivity benefit of AI assistance while adding a
review step proportional to the risk of the content.

**❌ Why not the others:**
- **A** overcorrects and discards genuine productivity benefits unnecessarily.
- **C** and **D** both ignore the risk entirely, in different ways.

**🎯 Example:** A marketing team using AI to draft blog posts, but always having a human fact-check any statistic before publishing.


---

<a id="-continue-reading"></a>
## Continue reading

[🏠 Home](../README.md) · [Next: Technical Assessment ➡](./02-technical-assessment.md)
