[🏠 Home](../README.md) · [⬅ Previous: AI Literacy](./01-ai-literacy.md) · [Next: Debugging Assessment ➡](./03-debugging-assessment.md)

---

# 🧮 Chapter 2 — Technical Assessment

**📑 In this chapter:**

1. [Topic 1: Programming Logic & Problem Solving (Q1–Q12)](#topic-1)
2. [Topic 2: Data Structures & Algorithms (Q13–Q24)](#topic-2)
3. [Topic 3: Software Engineering Fundamentals (Q25–Q36)](#topic-3)
4. [Topic 4: Modern Engineering Awareness (Q37–Q48)](#topic-4)

[🔝 Jump to navigation ⬇](#-continue-reading) (bottom of page)

---

🔮 **Source note:** Practice questions matched to Capgemini's confirmed topic list. Not leaked real
exam questions — built for volume + understanding.

**Format:** Options → ✅ Answer → 💡 Explanation → 🎯 Real-life example.

---

<a id="topic-1"></a>
## Topic 1: Programming Logic & Problem Solving (Q1–Q12)

**Q1. What will this print?**
```
x = 5; y = 2
print(x % y)
```
A) 2.5  B) 1  C) 2  D) 0
**✅ B** — `%` gives the remainder. 5 ÷ 2 = 2 remainder 1.
🎯 5 candies split among 2 friends: 2 each, 1 leftover — that leftover is `%`.

---

**Q2. Which data type stores `3.14`?**
A) int  B) char  C) float/double  D) boolean
**✅ C** — Decimal values need `float`/`double`; `int` is whole numbers only.
🎯 Height `5.8` ft needs float; age `24` uses int.

---

**Q3. Output of:**
```
a = 10; b = a; a = a + 5
print(b)
```
A) 15  B) 10  C) 5  D) Error
**✅ B** — `b = a` copies the value (10) at that moment; later changes to `a` don't affect `b`.
🎯 Photocopying a document, then scribbling on the original — the copy stays as it was.

---

**Q4. Which is implicit type conversion?**
A) `int x = (int) 5.9;`  B) `int x = 5; float y = x;`  C) `String s = String.valueOf(5);`  D) Manual string-to-int cast
**✅ B** — The compiler converts int→float automatically (safe, no data loss). A, C, D are all explicit/manual.
🎯 Pouring a small cup of water into a bigger jug — fits automatically, no special handling needed.

---

**Q5. What does this loop print?**
```
for i in range(1, 4): print(i)
```
A) 1 2 3 4  B) 1 2 3  C) 0 1 2 3  D) 2 3 4
**✅ B** — `range(1,4)` excludes the upper bound: 1, 2, 3.
🎯 A counter that stops just before reaching 4, never touching it.

---

**Q6. A variable used before being initialized will most likely cause:**
A) Always a compile error in every language  B) Undefined behavior or a runtime/logical error, depending on the language  C) Automatic correct initialization  D) No effect ever
**✅ B** — Behavior varies by language; absolute claims (A, D) are usually wrong in MCQs. C is simply false.
🎯 An empty box that might have leftover "garbage" in it until you deliberately fill it.

---

**Q7. Find the bug:**
```java
int[] arr = {1,2,3};
for (int i = 0; i <= arr.length; i++) { System.out.println(arr[i]); }
```
A) No bug  B) Off-by-one: should be `i < arr.length`  C) Array syntax wrong  D) Loop never runs
**✅ B** — Valid indexes for a length-3 array are 0,1,2. `i <= arr.length` lets i reach 3 → ArrayIndexOutOfBoundsException.
🎯 A parking lot with spots 0–2 (3 total); trying to park in "spot 3" which doesn't exist.

---

**Q8. Output of:**
```
x = "5"; y = 3
print(x + str(y))
```
A) 8  B) "53"  C) Error  D) "35"
**✅ B** — String concatenation joins "5" and "3" as text → "53", not numeric addition.
🎯 Sticky notes "5" then "3" placed side by side read as "53", not summed to 8.

---

**Q9. What does this pseudocode compute?**
```
total = 0
for i from 1 to n:
    total = total + i
```
A) n factorial  B) Sum of 1 to n  C) n squared  D) Product of 1 to n
**✅ B** — Each iteration adds the next integer; this is the classic running-sum pattern (equivalent to n(n+1)/2).
🎯 Adding up daily savings: ₹1 day 1, ₹2 day 2, etc. — total is the cumulative sum.

---

**Q10. Which best describes a "logical error" vs a "syntax error"?**
A) They're the same thing  B) A syntax error breaks compilation; a logical error compiles fine but produces wrong results  C) Logical errors always crash the program  D) Syntax errors never stop compilation
**✅ B** — Syntax errors are caught by the compiler/interpreter before running. Logical errors run without crashing but give incorrect output — often harder to catch.
🎯 A recipe with a missing ingredient in the list (syntax error, won't even start) vs. a recipe that runs fine but uses the wrong amount of salt (logical error, tastes wrong).

---

**Q11. In pseudocode interpretation, what does this represent?**
```
if (age >= 18):
    print("Eligible")
else:
    print("Not Eligible")
```
A) A loop  B) A conditional/decision structure  C) A function definition  D) A data type declaration
**✅ B** — `if/else` is a branching/decision structure — the program takes one of two paths based on a condition.
🎯 A bouncer checking ID at a club entrance — one path (in) if the condition is met, another (denied) if not.

---

**Q12. What is the output?**
```
count = 0
while count < 3:
    print(count)
    count += 1
```
A) 0 1 2  B) 1 2 3  C) 0 1 2 3  D) Infinite loop
**✅ A** — Starts at 0, prints while `count < 3` (0,1,2), then stops once count becomes 3.
🎯 A countdown-style check-in: you stop admitting people once you hit the capacity limit, right before crossing it.

---

<a id="topic-2"></a>
## Topic 2: Data Structures & Algorithms (Q13–Q24)

**Q13. Average time complexity of binary search on a sorted array of size n?**
A) O(n)  B) O(n log n)  C) O(log n)  D) O(1)
**✅ C** — Each step halves the search space; repeated halving to reach 1 element takes ~log₂(n) steps.
🎯 Finding a word in a dictionary by repeatedly opening to the middle of the remaining pages.

---

**Q14. Worst-case time complexity of Quicksort?**
A) O(n log n)  B) O(n²)  C) O(log n)  D) O(n)
**✅ B** — Poor pivot choices (e.g., always smallest/largest) create unbalanced partitions, degrading to O(n²). O(n log n) is the average/best case, not worst — a classic mix-up trap.
🎯 Sorting people by height by always picking the shortest person as pivot — splits off just one person per round.

---

**Q15. Which structure gives near O(1) average lookup via hashing?**
A) Linked List  B) Hash Map / Hash Table  C) Binary Search Tree  D) Stack
**✅ B** — A hash function computes almost directly where a key is stored. Linked List is O(n), BST is O(log n) average, Stack isn't for key lookup at all.
🎯 A library where a book's shelf is computed directly from its ISBN — no shelf-by-shelf scanning.

---

**Q16. Space complexity of an algorithm using a fixed number of extra variables regardless of input size?**
A) O(n)  B) O(n²)  C) O(1)  D) O(log n)
**✅ C** — Memory used doesn't grow with input — the definition of constant space.
🎯 A calculator using 2-3 memory slots whether adding 2 numbers or 2 million.

---

**Q17. Which sort is stable AND O(n log n) worst-case?**
A) Quicksort  B) Merge Sort  C) Selection Sort  D) Bubble Sort
**✅ B** — Merge Sort always splits evenly, guaranteeing O(n log n) even worst-case, and preserves order of equal elements (stable). Quicksort can degrade (Q14); Selection/Bubble are O(n²).
🎯 Repeatedly splitting a card deck in half, sorting each half, then merging back in order — consistent no matter the starting order.

---

**Q18. Time complexity of reversing a string via two pointers (swap, move inward)?**
A) O(n²)  B) O(n)  C) O(log n)  D) O(1)
**✅ B** — Each pointer traverses roughly half the string once; total work scales linearly.
🎯 Two people at opposite ends of a line swapping pairs and stepping inward, meeting in the middle.

---

**Q19. Which best describes "problem decomposition"?**
A) Solving everything in one giant undivided function  B) Breaking a large problem into smaller, independent sub-problems  C) Avoiding functions altogether  D) Only applies to sorting
**✅ B** — Splitting complex problems into manageable pieces solved separately, then combined.
🎯 Planning a wedding by breaking it into venue, catering, guest list, etc., rather than one giant undivided task.

---

**Q20. What is the time complexity of accessing an element by index in an array?**
A) O(n)  B) O(log n)  C) O(1)  D) O(n²)
**✅ C** — Arrays store elements in contiguous memory; the index directly computes the memory location — no searching needed.
🎯 Knowing a house's exact street number lets you go straight there, no need to check every house on the street.

---

**Q21. What data structure is best suited for Last-In-First-Out (LIFO) operations?**
A) Queue  B) Stack  C) Array (unordered)  D) Hash Map
**✅ B** — A Stack's defining behavior is: the most recently added item is the first one removed.
🎯 A stack of plates — you take the top plate off first, the one placed most recently.

---

**Q22. What data structure is best suited for First-In-First-Out (FIFO) operations?**
A) Stack  B) Queue  C) Binary Tree  D) Hash Set
**✅ B** — A Queue processes items in the order they arrived — the first one in is the first one out.
🎯 A line at a ticket counter — the first person to join the line is served first.

---

**Q23. What's the time complexity of Breadth-First Search (BFS) on a graph with V vertices and E edges?**
A) O(V)  B) O(E)  C) O(V + E)  D) O(V × E)
**✅ C** — BFS visits every vertex once and examines every edge once (in an adjacency list representation), giving combined linear complexity in vertices + edges.
🎯 Visiting every room in a building (vertices) and walking through every doorway connecting them (edges) exactly once.

---

**Q24. In dynamic programming, "memoization" refers to:**
A) Deleting old computed results to save memory  B) Storing (caching) results of expensive function calls and reusing them when the same inputs occur again  C) A sorting technique  D) A type of syntax error

**✅ B** — Instead of recomputing the same sub-problem repeatedly (as in naive recursion), memoization stores the result once and reuses it — turning exponential-time recursive solutions into polynomial-time ones.
🎯 Writing down the answer to a repeated math sub-problem on scratch paper instead of recalculating it every single time it comes up again.

---

<a id="topic-3"></a>
## Topic 3: Software Engineering Fundamentals (Q25–Q36)

**Q25. Which OOP principle allows a subclass to redefine a parent's method?**
A) Encapsulation  B) Polymorphism (method overriding)  C) Abstraction  D) Composition
**✅ B** — A child class giving its own behavior to an inherited method name is method overriding, a form of polymorphism.
🎯 `Animal.makeSound()` — `Dog` overrides it to bark, `Cat` overrides it to meow.

---

**Q26. Which SQL clause filters GROUPED results (after GROUP BY)?**
A) WHERE  B) HAVING  C) ORDER BY  D) FILTER
**✅ B** — `WHERE` filters rows before grouping; `HAVING` filters after aggregation is calculated.
🎯 `WHERE` = checking individual marks before grouping by class. `HAVING` = "which classes average above 80%," which only makes sense after grouping.

---

**Q27. Which HTTP method updates an existing resource entirely?**
A) GET  B) POST  C) PUT  D) DELETE
**✅ C** — `PUT` replaces a resource fully. (`PATCH` is for partial updates.) GET reads, POST creates, DELETE removes.
🎯 GET = read a profile. POST = create a new user. PUT = replace the whole profile. DELETE = remove the account.

---

**Q28. What does `git commit` do?**
A) Uploads code to a remote repo  B) Saves a snapshot of staged changes to local repo history  C) Deletes the current branch  D) Auto-merges two branches
**✅ B** — Saves a local checkpoint with a message. `git push` (not commit) is what sends it to a remote server.
🎯 Saving a checkpoint locally in a video game vs. uploading that save to the cloud (push).

---

**Q29. Which SQL keyword combines rows from two tables based on a related column?**
A) UNION  B) JOIN  C) GROUP BY  D) DISTINCT
**✅ B** — `JOIN` links tables via a shared column (e.g., `customer_id`). `UNION` stacks result sets, doesn't link by column.
🎯 Matching a student's ID across a "Students" table and a "Marks" table to see name next to marks.

---

**Q30. What is "encapsulation" in OOP?**
A) Making all variables public  B) Bundling data and methods together and restricting direct access to internal state (e.g., via private fields + public methods)  C) Deleting unused classes  D) A database indexing technique
**✅ B** — Encapsulation protects an object's internal state from being changed arbitrarily from outside, exposing only controlled access via methods.
🎯 A car's engine internals are hidden under the hood; you interact with it only through the accelerator/brake — controlled access, not direct wiring access.

---

**Q31. What is a "primary key" in a database table?**
A) Any random column  B) A column (or set of columns) that uniquely identifies each row in a table  C) A column that can have duplicate values  D) A column used only for sorting
**✅ B** — Every row must have a unique primary key value — it's how the database guarantees each record can be uniquely identified and referenced.
🎯 A student's unique roll number — no two students in the same class share one.

---

**Q32. What is the purpose of a "foreign key" in a relational database?**
A) To encrypt a table  B) To create a link between two tables by referencing another table's primary key, enforcing referential integrity  C) To speed up all queries automatically  D) To rename a column
**✅ B** — A foreign key in one table points to a primary key in another, maintaining valid, consistent relationships (e.g., an `Orders` table's `customer_id` pointing to a valid `Customers` row).
🎯 A library card referencing a specific member ID — you can't issue a card for a member who doesn't exist in the members list.

---

**Q33. What does REST stand for, and what's one core REST principle?**
A) Random External State Transfer; no defined principles  B) Representational State Transfer; it's typically stateless — each request from client to server contains all information needed  C) Rapid Execution State Tool; requires a database  D) Not a real acronym

**✅ B** — REST APIs typically don't store client session state on the server between requests — each request is self-contained (includes any needed auth/data), which improves scalability.
🎯 Each time you call a restaurant to place an order, you re-state your full order and address — the restaurant doesn't need to "remember" your previous call.

---

**Q34. What's the difference between `git merge` and `git rebase`, at a basic level?**
A) They are identical  B) `merge` combines branch histories with a merge commit, preserving both histories as-is; `rebase` re-applies commits on top of another branch, creating a linear history  C) `rebase` deletes all commit history  D) `merge` only works on the main branch

**✅ B** — Both integrate changes from one branch into another, but they produce different resulting commit histories — merge keeps a branching structure with an extra merge commit, rebase creates a cleaner, linear sequence.
🎯 Merge is like stapling two separate documents together as-is; rebase is like retyping one document's changes onto the end of the other, producing one continuous document.

---

**Q35. What is "abstraction" in OOP, and how does it differ from encapsulation?**
A) They're the same thing  B) Abstraction hides complex implementation details behind a simple interface (what it does); encapsulation controls access to internal data (how it's protected)  C) Abstraction is only used in databases  D) Encapsulation always requires inheritance

**✅ B** — Abstraction is about simplifying what's exposed to the user (a simple `startCar()` method hiding complex engine logic); encapsulation is about protecting and controlling access to internal data. They're related but distinct concepts, a common point of confusion for freshers.
🎯 A car's steering wheel and pedals are the abstraction (simple interface); the actual engine wiring being inaccessible under the hood is the encapsulation.

---

**Q36. What does "idempotent" mean for an HTTP method like PUT or DELETE?**
A) It means the request always fails the second time  B) Calling it multiple times with the same input produces the same result/state as calling it once  C) It means the method requires authentication  D) It means the method is faster than others

**✅ B** — `PUT`ting the same data twice, or `DELETE`ing the same resource twice, leaves the system in the same end state as doing it once — an important property for reliable retries over unreliable networks.
🎯 Pressing an elevator's "floor 5" button multiple times doesn't send the elevator to a different floor each time — the end result (arriving at floor 5) stays the same.

---

<a id="topic-4"></a>
## Topic 4: Modern Engineering Awareness (Q37–Q48)

**Q37. In client-server architecture, the "client" typically:**
A) Stores and serves data/resources  B) Requests resources or services from a server  C) Is always a physical server rack  D) Is a database index
**✅ B** — The client asks (requests); the server provides. A describes the server's role.
🎯 You (client) order food at a restaurant; the kitchen (server) prepares and sends it.

---

**Q38. Main difference between an API key and an OAuth token?**
A) They're identical  B) API keys are typically static, long-lived identifiers for a project/app; OAuth tokens are often short-lived, scoped credentials tied to a user session  C) Tokens never expire  D) API keys are only for databases
**✅ B** — Tokens commonly expire (a security feature, not a flaw); API keys identify the calling app/project and often persist longer.
🎯 API key = a permanent staff ID card. Token = a visitor's day-pass that expires and only opens certain floors.

---

**Q39. What does Docker primarily provide?**
A) Version control  B) Containerization — packaging an app with dependencies to run consistently across environments  C) A programming language  D) A database engine
**✅ B** — Solves "it works on my machine" by bundling everything the app needs into a portable container.
🎯 Shipping a fully-packed lunch box with everything included, instead of hoping the destination has matching plates and forks.

---

**Q40. In Agile, a "sprint" refers to:**
A) A single line of code  B) A fixed, short time-boxed period (commonly 1-4 weeks) to complete a set of work  C) A database query type  D) A cybersecurity protocol
**✅ B** — Short iterative cycles with review and replanning, core to Agile's incremental approach.
🎯 Reviewing study goals every 2 weeks instead of planning an entire semester in one go.

---

**Q41. Which is a basic cybersecurity best practice?**
A) Hardcoding credentials directly in source code in a public repo  B) Using environment variables/secret managers, never committing secrets to version control  C) Reusing the same password everywhere  D) Disabling HTTPS for "speed"
**✅ B** — Keeps credentials out of the codebase entirely, so they're never exposed if code is shared or leaked.
🎯 Keeping your house key with trusted people only, not posting its location on a public noticeboard.

---

**Q42. What is the main purpose of a load balancer in a client-server system?**
A) To encrypt all traffic  B) To distribute incoming requests across multiple servers, improving reliability and handling higher traffic  C) To store user passwords  D) To compile code faster
**✅ B** — Prevents any single server from being overwhelmed by spreading requests across a pool of servers — improves both performance and fault tolerance (if one server fails, others keep serving).
🎯 A supermarket opening multiple checkout counters and directing customers to whichever is free, instead of forcing everyone into one line.

---

**Q43. What does "CI/CD" stand for in DevOps, and what's its core benefit?**
A) Code Isolation / Code Deployment; no real benefit  B) Continuous Integration / Continuous Deployment (or Delivery) — automatically building, testing, and deploying code changes frequently and reliably  C) Central Index / Central Directory; a database term  D) It's unrelated to software

**✅ B** — CI automatically builds and tests code every time changes are pushed; CD automates getting tested changes into production (or ready for release) — reducing manual error and speeding up delivery.
🎯 An assembly line that automatically checks quality at every stage and ships the finished product, instead of manually inspecting and shipping each item by hand.

---

**Q44. What is the main advantage of cloud computing (e.g., AWS, Azure, GCP) over traditional on-premise servers?**
A) It's always completely free  B) On-demand, scalable computing resources without owning/maintaining physical hardware  C) It requires no internet connection  D) It eliminates the need for any security practices

**✅ B** — You can scale resources up or down as needed and pay for what you use, without buying and maintaining physical servers yourself.
🎯 Renting a car when you need one instead of buying and maintaining one you rarely use.

---

**Q45. What is the purpose of an "environment variable" in software configuration?**
A) To change the color scheme of an IDE  B) To store configuration values (like API keys, database URLs) outside the source code, so they can differ per environment (dev/test/prod) without code changes  C) To slow down execution intentionally  D) To define a new programming language

**✅ B** — Keeps configuration (and secrets — see Q41) separate from code, so the same code can run against a test database in development and a real database in production just by changing the environment variables.
🎯 Using a different delivery address depending on whether you're testing an order process or placing a real order — same process, different configuration.

---

**Q46. What is a basic definition of "networking latency"?**
A) The amount of storage a server has  B) The time delay between sending a request and receiving a response over a network  C) The number of users on a website  D) A type of encryption

**✅ B** — Latency measures delay, not data volume or throughput — a highly relevant distinction in performance-focused technical questions.
🎯 The pause between asking someone a question over a long-distance phone call and actually hearing their answer.

---

**Q47. What does "version control" (like Git) fundamentally provide?**
A) A way to compile code faster  B) A system for tracking changes to files over time, enabling collaboration, history, and rollback to previous states  C) A cloud hosting service  D) An encryption algorithm

**✅ B** — Every commit is a tracked snapshot, letting teams collaborate, see who changed what, and revert to earlier working versions if something breaks.
🎯 Track-changes in a shared document, but far more powerful — with a full history of every version and the ability to jump back to any point.

---

**Q48. Basic Docker awareness: what is the difference between a Docker "image" and a Docker "container"?**
A) They are identical terms  B) An image is a static, packaged blueprint (app + dependencies); a container is a running instance of that image  C) A container is used only for databases  D) An image can only be used once

**✅ B** — The image is the recipe/template; the container is the actual running process created from that template — you can start multiple containers from the same single image.
🎯 A cake recipe (image) vs. an actual baked cake (container) — you can bake multiple cakes from the same recipe.

---

## Visual summary
See `../images/debugging-flow.svg` for the Debugging round's process and `../images/ai-assisted-coding-flow.svg` for the AI-Assisted Coding round's flow.


---

<a id="-continue-reading"></a>
## Continue reading

[🏠 Home](../README.md) · [⬅ Previous: AI Literacy](./01-ai-literacy.md) · [Next: Debugging Assessment ➡](./03-debugging-assessment.md)
