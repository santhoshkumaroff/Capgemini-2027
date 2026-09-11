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

**Format:** Options → ✅ Answer → 💡 Explanation (why correct + why others don't fit) → 🎯 Real-life example.

---

<a id="topic-1"></a>
## Topic 1: AI Foundations & Generative AI (Q1–Q10)

**Q1. What is a "foundation model"?**
A) A small task-specific model  B) A large model pre-trained on broad data, adaptable to many tasks  C) A rule-based expert system  D) A database indexing algorithm

**✅ B** — Foundation models learn broadly first (language, code, reasoning patterns), then get pointed at specific jobs. A describes the opposite (narrow/specialized). C is hand-written rules, not learned patterns. D is unrelated.
🎯 Like a fresh graduate with broad general knowledge who later specializes on the job.

---

**Q2. What does "LLM" stand for?**
A) Large Language Model  B) Linear Learning Machine  C) Logical Language Module  D) Layered Learning Model

**✅ A** — This is the standard, literal term: trained on huge amounts of language data. B, C, D are plausible-sounding distractors with no real meaning in this context.
🎯 ChatGPT, Claude, Gemini — all LLMs.

---

**Q3. Which is a well-known LIMITATION of current LLMs?**
A) Instant processing  B) "Hallucination" — confident but false output  C) Cannot generate text  D) Only work with images

**✅ B** — Models predict plausible-sounding text, not verified fact; they can state wrong info confidently. C contradicts the definition of an LLM. A is a strength, not limitation. D is false.
🎯 Asking for a legal citation and getting a fake one that sounds completely real.

---

**Q4. How does Generative AI differ from traditional predictive ML?**
A) It only classifies data  B) It creates new content instead of just predicting a label  C) It can't use text data  D) Only works with tabular data

**✅ B** — Predictive ML answers "which category?"; generative AI produces brand-new content. A describes classification. C and D are false — text/unstructured data is generative AI's main domain.
🎯 Predictive: "this email is spam." Generative: writes you a whole new email.

---

**Q5. What is "training data" for an LLM?**
A) Debugging test cases  B) The large corpus the model learns patterns from before deployment  C) Only live chat history  D) Only labeled classification data

**✅ B** — The model "reads" huge amounts of text before ever being used. A is a software-testing concept. C is a tiny separate thing after training. D is mostly false — LLM training data is largely unlabeled raw text.
🎯 Like a student who read thousands of books before the exam.

---

**Q6. A genuine capability of modern LLMs is:**
A) Perfect factual accuracy always  B) Few-shot learning from a couple of examples in the prompt  C) Guaranteed live internet access by default  D) Immunity to bias

**✅ B** — Show 2-3 examples, the model often picks up the pattern without retraining. A is false (see Q3). C is false unless connected to search/RAG. D is false — bias comes from training data (Topic 4).
🎯 Show 2 examples of "make this formal," and the 3rd sentence follows the same style automatically.

---

**Q7. What best distinguishes a "base model" from a "fine-tuned model"?**
A) There is no difference  B) A base model is broadly pre-trained; a fine-tuned model is further trained on a narrower, specific dataset/task  C) Fine-tuned models are always smaller  D) Base models can't generate text

**✅ B** — Fine-tuning takes the broad foundation and specializes it further (e.g., for customer support tone, or a coding-only assistant). C and D are false generalizations.
🎯 A general doctor (base model) who later does a specialization in cardiology (fine-tuning).

---

**Q8. What does "context window" refer to in an LLM?**
A) The physical screen size  B) The maximum amount of text (tokens) the model can consider at once when generating a response  C) A UI setting for font  D) The model's training duration

**✅ B** — If a conversation or document exceeds the context window, the model literally cannot "see" the parts that fall outside it. A, C, D are unrelated.
🎯 Like a whiteboard of limited size — once it's full, older notes have to be erased to fit new ones.

---

**Q9. Why do LLMs sometimes give different answers to the same prompt asked twice?**
A) They are broken  B) Many LLMs use some randomness (sampling/"temperature") in generation, so outputs can vary  C) They always give identical answers  D) Only image models vary

**✅ B** — Temperature/sampling settings intentionally introduce controlled randomness so responses aren't robotically identical every time. C is false; this variability is by design, not a malfunction (A is wrong).
🎯 Asking a knowledgeable friend the same question twice — the core facts stay similar, but the exact phrasing varies.

---

**Q10. What is "tokenization" in the context of LLMs?**
A) Creating cryptocurrency tokens  B) Breaking text into smaller units (words/sub-words) the model processes numerically  C) A security login method  D) Compressing an image file

**✅ B** — Before an LLM can process text, it splits it into tokens (which could be whole words or word-pieces) and converts them into numbers it can compute with. A and C are unrelated. D is a different technical concept.
🎯 Like chopping a sentence into puzzle pieces before feeding it into a machine that only understands pieces, not whole sentences.

---

<a id="topic-2"></a>
## Topic 2: Prompt Engineering & AI Productivity (Q11–Q20)

**Q11. Which is the BEST example of a well-structured prompt?**
A) "fix this"  B) "Write code"  C) "Write a Python function that takes a list of integers and returns the second-largest value; return None if the list has fewer than 2 elements."  D) "help me"

**✅ C** — Specifies language, exact task, input/output, and an edge case. A, B, D are all too vague, forcing the AI to guess.
🎯 "This function crashes on empty input, please add a check" vs. just "fix this."

---

**Q12. "Context setting" in prompting means:**
A) Changing font size  B) Giving background info (role, constraints, format) before the actual ask  C) Deleting chat history  D) Using only single-word prompts

**✅ B** — E.g., "You're helping debug Java for a banking app; follow standard naming conventions." This shapes every following answer. C is the opposite of context-setting.
🎯 Telling a new intern "we're in healthcare, avoid casual language" before assigning a task.

---

**Q13. GitHub Copilot is best described as:**
A) A version control system  B) An AI pair-programming tool suggesting code completions based on context  C) A cloud hosting platform  D) A database tool

**✅ B** — Sits inside your editor and suggests next lines based on what you've typed. A is Git (a different, related tool). C and D are unrelated categories.
🎯 You type a function name; Copilot suggests a plausible function body — you accept, edit, or reject.

---

**Q14. Which practice improves prompt quality the most?**
A) Keeping prompts vague and short  B) Giving examples of the desired input/output format (few-shot prompting)  C) Never specifying constraints  D) Repeating the identical failed prompt

**✅ B** — Showing 1-2 worked examples removes guesswork and is the single highest-leverage prompting technique. A and C make output worse. D wastes a turn without fixing the root cause.
🎯 "Format each answer like this: Q: ... A: ..." followed by one example — the AI then follows that format consistently.

---

**Q15. If the AI's output is wrong, the best first move is to:**
A) Ship it to production anyway  B) Review critically, identify the gap, refine the prompt with more specific context  C) Give up  D) Ask something unrelated

**✅ B** — Wrong output is information about what context was missing. A is risky; C and D avoid the actual problem.
🎯 A teammate's first draft has an error — you point out the specific issue and ask for a revision, not scrap the whole project.

---

**Q16. What is "chain-of-thought" prompting?**
A) Asking the AI to skip explaining and just give the final answer  B) Asking the AI to reason step-by-step before giving a final answer, improving accuracy on complex tasks  C) Linking multiple unrelated prompts randomly  D) A type of database chaining

**✅ B** — Explicitly asking for step-by-step reasoning (e.g., "think through this step by step") often improves accuracy on multi-step logic or math problems, because it forces intermediate reasoning instead of a rushed jump to a conclusion.
🎯 Asking a student to "show your working" on a math problem instead of just writing the final number — mistakes become visible and fixable.

---

**Q17. What's a "system prompt" typically used for?**
A) Displaying an error message  B) Setting persistent instructions/behavior/role for the AI throughout a conversation, separate from the user's individual messages  C) A one-time joke prompt  D) Formatting the screen resolution

**✅ B** — It establishes the AI's role, tone, and constraints up front, applying to the whole conversation rather than being repeated every message.
🎯 Like a company handing a new support agent a standing set of guidelines before they start taking calls — those guidelines apply to every call, not just the first one.

---

**Q18. Why might a very long, unstructured prompt actually produce worse output than a shorter, well-organized one?**
A) Length always improves output quality  B) Important instructions can get buried or diluted among irrelevant detail, making the actual ask unclear  C) AI models cannot read long prompts at all  D) There is no difference ever

**✅ B** — Clarity and structure matter more than raw length. Burying the actual task in unrelated detail makes it harder for the model to identify what you actually want.
🎯 A cluttered work email with the real ask buried in paragraph 5 — vs. a clear email with the ask stated up top and details after.

---

**Q19. What does "zero-shot prompting" mean?**
A) Giving the AI many worked examples first  B) Asking the AI to perform a task with no prior examples given, relying only on the instruction itself  C) A failed prompt  D) Only used for image generation

**✅ B** — "Zero" examples given — you just describe the task directly and the model attempts it based on its general training, contrasted with "few-shot" (Q14), which gives examples.
🎯 Asking someone to "translate this sentence to French" with no example translation shown first — they just do it based on general knowledge.

---

**Q20. Which is a red flag of a LOW-quality AI-assisted coding prompt?**
A) Specifying the exact function signature and edge cases  B) Pasting the raw problem statement with zero added structure and accepting the first output without review  C) Asking the AI to explain its approach before coding  D) Requesting test cases alongside the code

**✅ B** — This is the exact anti-pattern Capgemini's AI-Assisted Coding round evaluates against (see Section 4) — no structure, no review. A, C, D are all good practices.
🎯 Copy-pasting a whole assignment into an AI and turning in whatever comes out first, unread.

---

<a id="topic-3"></a>
## Topic 3: Advanced AI Systems (Q21–Q30)

**Q21. What does RAG stand for?**
A) Rapid Application Generation  B) Retrieval-Augmented Generation  C) Random Access Gateway  D) Recursive Algorithm Graph

**✅ B** — Retrieval (fetch real, relevant documents) + Generation (LLM answers using that content) — grounds answers in real data, reducing hallucination. Others are invented distractors.
🎯 Instead of guessing your company's leave policy from memory, the system pulls the actual current HR document first, then answers from it.

---

**Q22. An "AI agent" is best described as:**
A) A static chatbot answering one question with no memory  B) A system that can autonomously plan, use tools, and take multi-step actions toward a goal  C) A type of database index  D) A hardware component

**✅ B** — Agents break a goal into steps, use tools (search, calculators, APIs), check results, and decide the next step — looping until done. A is the opposite behavior.
🎯 "Book me the cheapest flight to Delhi Friday" — an agent searches, compares, checks your calendar, and books — multiple autonomous steps.

---

**Q23. Why does RAG reduce hallucination?**
A) It makes the model bigger  B) It grounds responses in retrieved real documents instead of relying purely on memorized training data  C) It removes the need for any training  D) It deliberately slows responses

**✅ B** — Real source material to reference beats recalling from memory alone. C is false — RAG still needs an underlying trained model.
🎯 Open-book exam (RAG, can check the textbook) vs. closed-book exam from memory alone.

---

**Q24. A "multi-step AI workflow" typically involves:**
A) A single prompt-response with no further steps  B) Breaking a complex task into subtasks, chaining tool use/reasoning steps  C) Only image generation  D) No AI involvement

**✅ B** — Complex tasks rarely get solved in one shot; output of one step feeds the next. A is the opposite (single-step).
🎯 The AI-Assisted Coding round itself: understand → propose approach → generate code → review & fix.

---

**Q25. What is a "vector database" commonly used for in AI systems?**
A) Storing plain text logs only  B) Storing numeric representations (embeddings) of content so similar items can be found via similarity search — key building block for RAG  C) Managing user passwords  D) Compiling source code

**✅ B** — Embeddings capture semantic meaning as numbers; a vector database lets you quickly find content "similar in meaning" to a query — this is how RAG systems retrieve relevant documents.
🎯 Finding songs "similar in vibe" to one you like, based on numeric features of the song, rather than matching exact titles.

---

**Q26. What does "grounding" mean in the context of AI-generated answers?**
A) Powering off the AI  B) Basing the AI's response on verifiable external data/sources rather than pure model memory  C) A hardware safety feature  D) Limiting response length

**✅ B** — Grounding is closely tied to RAG (Q21/Q23) — it means tying answers to something checkable, reducing the risk of confident-but-wrong output.
🎯 A journalist citing an actual document instead of writing from memory alone.

---

**Q27. What's the main risk of giving an AI agent too much autonomy without human checkpoints?**
A) There is no risk  B) It may take incorrect or unintended multi-step actions before a human notices and can correct it  C) It will always refuse to act  D) It becomes slower

**✅ B** — More autonomous steps without review means errors can compound across steps before anyone catches them — this is why human-in-the-loop checkpoints matter for high-stakes agent actions.
🎯 An autopilot flying without any pilot oversight — small early errors can compound before anyone intervenes.

---

**Q28. Which best describes "tool use" by an AI agent?**
A) The AI edits its own source code permanently  B) The AI calls external functions/APIs (like a calculator, search engine, or database) to get information or take an action it can't do purely through text generation  C) The AI only uses tools for image generation  D) Tool use means the AI has no limitations at all

**✅ B** — LLMs can't natively do things like real-time math with perfect precision or fetch live data — "tools" extend their capability by letting them call out to specialized functions.
🎯 A person who doesn't do long division in their head but reaches for a calculator when needed.

---

**Q29. In a multi-step AI workflow, why is it useful to have the AI "show its plan" before executing?**
A) It isn't useful  B) It lets a human review and catch a flawed approach before time/resources are spent executing it  C) It only matters for image generation  D) Plans are always guaranteed correct

**✅ B** — Reviewing the plan first is cheaper than discovering a flawed approach after several steps have already run.
🎯 Approving a project plan before construction begins, rather than after the building is already half-built.

---

**Q30. What differentiates "Agentic AI" from a simple chatbot?**
A) Nothing, they're identical  B) Agentic AI can independently decide on and execute a sequence of actions toward a goal, not just respond to single queries  C) Agentic AI only works offline  D) Chatbots are always more capable

**✅ B** — This directly echoes Q22's definition of an "AI agent" — the "agentic" quality is about autonomous multi-step action, not just single-turn response.
🎯 A chatbot answers "what's the weather" when asked. An agentic system could be told "plan my outdoor trip this weekend" and autonomously check weather, suggest dates, and draft an itinerary.

---

<a id="topic-4"></a>
## Topic 4: Responsible AI & AI Evaluation (Q31–Q40)

**Q31. Why is "output validation" important for AI-generated content/code?**
A) It isn't — AI is always correct  B) AI can produce plausible but incorrect, insecure, or biased output, so a human should verify before use  C) Only matters for images  D) Only relevant for non-technical tasks

**✅ B** — Confident-sounding ≠ correct (Q3). A human check before relying on or shipping output is essential.
🎯 AI-generated code that "looks right" but has a SQL injection vulnerability — only review catches it.

---

**Q32. "Bias" in an AI model typically originates from:**
A) The model's color scheme  B) Patterns (including unfair/skewed ones) present in the training data  C) The user's internet speed  D) The programming language used

**✅ B** — Models learn from what they're shown; skewed data produces skewed output. A, C, D are unrelated technical factors.
🎯 A resume-screening model trained mostly on one demographic's past hires may favor that pattern going forward.

---

**Q33. Which is a responsible AI practice?**
A) Blindly trusting AI in high-stakes decisions without human review  B) Disclosing AI-generated content where relevant, and reviewing output for accuracy/fairness  C) Never testing AI output  D) Ignoring data privacy when prompting

**✅ B** — Transparency + human oversight + active fairness/accuracy checks define responsible use. A, C, D each skip a necessary safeguard.
🎯 A doctor using AI to draft notes still personally reviews and signs off on the final decision.

---

**Q34. What's a practical way to evaluate AI-generated code before use?**
A) Assume correctness because it compiles  B) Read it, test against edge cases, check for security/logic issues  C) Never look at it  D) Only check it "looks professional"

**✅ B** — Compiling only proves valid syntax, not correct or safe logic. A confuses "compiles" with "correct" — a common fresher mistake.
🎯 Code that compiles fine but crashes on an empty list input — only testing the edge case catches it.

---

**Q35. Why shouldn't sensitive/confidential data be pasted into a public AI chat tool?**
A) It slows the AI down  B) It may be logged, used for training, or exposed — a real privacy/security risk  C) AI tools can't process sensitive data at all  D) It's completely safe

**✅ B** — Depending on the tool's settings, typed data can be stored or reviewed — a genuine compliance risk for confidential data. C and D are false.
🎯 Pasting a real customer's ID number into a public AI chatbot "to summarize" — a data leak risk companies explicitly guard against.

---

**Q36. What is "AI explainability" (or interpretability)?**
A) Making an AI model talk louder  B) The degree to which humans can understand WHY a model produced a particular output or decision  C) A model's marketing description  D) The model's file size

**✅ B** — Especially important in high-stakes domains (finance, healthcare, hiring) where a black-box decision without any reasoning trail is hard to trust or audit.
🎯 A loan rejection that comes with a reason ("insufficient credit history") is more trustworthy and actionable than a bare "no" with zero explanation.

---

**Q37. What does "human-in-the-loop" mean in an AI system design?**
A) A human physically sits inside a server room  B) A human reviews, approves, or can override AI decisions/outputs at key points, rather than the AI acting fully autonomously  C) It means no AI is used at all  D) It's a hardware specification

**✅ B** — This is the standard safeguard against fully autonomous AI errors going unchecked, especially for consequential decisions.
🎯 An AI drafts a customer refund decision, but a support agent reviews and approves it before it's processed — not fully automatic.

---

**Q38. Which scenario best illustrates a responsible-AI FAILURE?**
A) A team tests AI-generated code against edge cases before deploying  B) A team ships AI-written financial advice directly to customers with no human review or disclosure that it's AI-generated  C) A team discloses AI involvement in a report  D) A team double-checks AI facts before publishing

**✅ B** — No human review + no disclosure + a high-stakes domain (financial advice) — this combination is exactly the kind of failure Responsible AI practices exist to prevent.
🎯 An unreviewed AI chatbot telling a customer to make a specific investment decision with no advisor oversight.

---

**Q39. Why is it risky to assume an AI model's confidence (how certain it "sounds") reflects its actual accuracy?**
A) It's not risky, confidence always equals accuracy  B) LLMs can state incorrect information with the same fluent, confident tone as correct information — tone is not a reliability signal  C) AI models never sound confident  D) This only applies to voice assistants

**✅ B** — This directly connects to hallucination (Q3): a wrong answer and a right answer can both be phrased with identical, fluent confidence — so confidence of tone should never be mistaken for a correctness guarantee.
🎯 A person who speaks very assertively isn't necessarily more correct than someone who hedges — same logic applies to AI output.

---

**Q40. What is a reasonable organizational policy response to the risk of AI hallucination in customer-facing content?**
A) Ban AI use entirely with no exceptions  B) Require human review/fact-checking of AI-generated content before it reaches customers, especially for factual claims  C) Publish all AI output instantly with no checks  D) Only check AI output once a year

**✅ B** — A balanced, practical response: keep the productivity benefit of AI assistance while adding a review step proportional to the risk of the content (factual/high-stakes content gets more scrutiny).
🎯 A marketing team using AI to draft blog posts, but always having a human fact-check any statistic or claim before publishing.

---

## Visual summary
See `../images/debugging-flow.svg` and `../images/ai-assisted-coding-flow.svg` for the other two rounds' flowcharts.


---

<a id="-continue-reading"></a>
## Continue reading

[🏠 Home](../README.md) · [Next: Technical Assessment ➡](./02-technical-assessment.md)
