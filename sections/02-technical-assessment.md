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

**How every question is laid out below (same structure, every single time):**
Options → ✅ Correct Answer → 💡 Why it's correct → ❌ Why each other option is wrong → 🎯 Real-life example.

---

<a id="topic-1"></a>
## Topic 1: Programming Logic & Problem Solving (Q1–Q12)

### Q1. What will this print?
```
x = 5; y = 2
print(x % y)
```
- **A.** 2.5
- **B.** 1
- **C.** 2
- **D.** 0

**✅ Correct Answer: B**

**💡 Why:** `%` is the modulus operator — it gives the remainder after division. 5 ÷ 2 = 2 remainder 1.

**❌ Why not the others:**
- **A** is what true division (`x / y`) gives, not `%`.
- **C** is the whole-number quotient, not the remainder.
- **D** would only be correct if 5 were evenly divisible by 2.

**🎯 Example:** 5 candies split among 2 friends — 2 each, 1 leftover. That leftover is `%`.

---

### Q2. Which data type stores `3.14`?

- **A.** int
- **B.** char
- **C.** float/double
- **D.** boolean

**✅ Correct Answer: C**

**💡 Why:** `3.14` has a decimal point, so it needs a type built for fractional numbers.

**❌ Why not the others:**
- **A** stores whole numbers only.
- **B** stores a single character like `'A'`.
- **D** stores only `true`/`false`.

**🎯 Example:** Height `5.8` ft needs float; age `24` uses int.

---

### Q3. What is the output of this?
```
a = 10; b = a; a = a + 5
print(b)
```
- **A.** 15
- **B.** 10
- **C.** 5
- **D.** Error

**✅ Correct Answer: B**

**💡 Why:** `b = a` copies the current value of `a` (10) at that moment. Changing `a` afterward doesn't retroactively change `b`.

**❌ Why not the others:**
- **A** would be `a`'s new value, not `b`'s.
- **C** and **D** don't logically follow from any step here.

**🎯 Example:** Photocopying a document, then scribbling on the original — the copy stays as it was.

---

### Q4. Which of the following is an example of implicit type conversion?

- **A.** `int x = (int) 5.9;`
- **B.** `int x = 5; float y = x;` (int automatically becomes float)
- **C.** `String s = String.valueOf(5);`
- **D.** Manually casting a string to an integer

**✅ Correct Answer: B**

**💡 Why:** "Implicit" means the language converts automatically without an explicit cast. Assigning
an int to a float is safe (no data lost), so the compiler does it silently.

**❌ Why not the others:**
- **A** and **D** both use explicit casting syntax — the programmer is telling the compiler what to do.
- **C** uses a method call, also explicit.

**🎯 Example:** Pouring a smaller cup of water into a bigger jug — it just fits, no special handling needed.

---

### Q5. What does this loop print?
```
for i in range(1, 4): print(i)
```
- **A.** 1 2 3 4
- **B.** 1 2 3
- **C.** 0 1 2 3
- **D.** 2 3 4

**✅ Correct Answer: B**

**💡 Why:** `range(1, 4)` starts at 1 and stops before 4 — the upper bound is excluded.

**❌ Why not the others:**
- **A** wrongly includes 4.
- **C** wrongly starts at 0 (that's `range(4)` alone, not `range(1,4)`).
- **D** wrongly skips 1.

**🎯 Example:** A counter that stops just before reaching 4, never touching it.

---

### Q6. A variable declared but never initialized before use will most likely cause:

- **A.** Always a syntax error at compile time in every language
- **B.** Undefined behavior or a runtime/logical error, depending on the language
- **C.** Automatic initialization to the correct business value
- **D.** No effect at all in any language

**✅ Correct Answer: B**

**💡 Why:** Behavior differs by language — some give a default value, some throw a compile error,
some (like C) leave garbage memory data. The safe, general answer is: it depends, and it's risky.

**❌ Why not the others:**
- **A** and **D** are absolute claims ("always," "no effect...in any language") — usually wrong since behavior varies by language.
- **C** is simply false — there's no such thing as automatic initialization to a "correct business value."

**🎯 Example:** An empty box that might have leftover "garbage" in it until you deliberately fill it.

---

### Q7. Find the bug:
```java
int[] arr = {1,2,3};
for (int i = 0; i <= arr.length; i++) {
    System.out.println(arr[i]);
}
```
- **A.** No bug
- **B.** Off-by-one: `i <= arr.length` causes ArrayIndexOutOfBoundsException; should be `i < arr.length`
- **C.** Array syntax is wrong
- **D.** Loop never executes

**✅ Correct Answer: B**

**💡 Why:** An array of length 3 has valid indexes 0, 1, 2. `i <= arr.length` lets `i` reach 3 — one past the last valid index.

**❌ Why not the others:**
- **A** is false — there clearly is a bug.
- **C** is false — the array declaration syntax is correct.
- **D** is false — the loop does execute, it just crashes partway through.

**🎯 Example:** A parking lot has spots 0–2 (3 spots). Trying to park in "spot 3," which doesn't exist.

---

### Q8. What is the output?
```
x = "5"; y = 3
print(x + str(y))
```
- **A.** 8
- **B.** "53"
- **C.** Error
- **D.** "35"

**✅ Correct Answer: B**

**💡 Why:** `x` is already a string `"5"`. `str(y)` converts `3` to `"3"`. Adding two strings with `+` concatenates them as text.

**❌ Why not the others:**
- **A** would only be correct for numeric addition, but `x` is a string.
- **C** is wrong because `str(y)` correctly converts the type first.
- **D** has the digits in the wrong order — that would need `str(y) + x`.

**🎯 Example:** Sticky notes "5" then "3" placed side by side read as "53," not summed to 8.

---

### Q9. What does this pseudocode compute?
```
total = 0
for i from 1 to n:
    total = total + i
```
- **A.** n factorial
- **B.** Sum of 1 to n
- **C.** n squared
- **D.** Product of 1 to n

**✅ Correct Answer: B**

**💡 Why:** Each iteration adds the next integer — this is the classic running-sum pattern
(equivalent to n(n+1)/2).

**❌ Why not the others:**
- **A** and **D** describe multiplying values together (factorial), not adding them.
- **C** would require multiplying n by itself, not summing a sequence.

**🎯 Example:** Adding up daily savings: ₹1 day 1, ₹2 day 2, etc. — the total is the cumulative sum.

---

### Q10. Which best describes a "logical error" vs a "syntax error"?

- **A.** They're the same thing
- **B.** A syntax error breaks compilation; a logical error compiles fine but produces wrong results
- **C.** Logical errors always crash the program
- **D.** Syntax errors never stop compilation

**✅ Correct Answer: B**

**💡 Why:** Syntax errors are caught by the compiler/interpreter before running. Logical errors run
without crashing but give incorrect output — often harder to catch.

**❌ Why not the others:**
- **A** is false — they are distinct and behave very differently.
- **C** is false — logical errors often DON'T crash; that's what makes them hard to notice.
- **D** is false — syntax errors specifically DO stop compilation.

**🎯 Example:** A recipe with a missing ingredient in the list (syntax error, won't even start) vs. a recipe that runs fine but uses the wrong amount of salt (logical error, tastes wrong).

---

### Q11. In pseudocode interpretation, what does this represent?
```
if (age >= 18):
    print("Eligible")
else:
    print("Not Eligible")
```
- **A.** A loop
- **B.** A conditional/decision structure
- **C.** A function definition
- **D.** A data type declaration

**✅ Correct Answer: B**

**💡 Why:** `if/else` is a branching structure — the program takes one of two paths based on a condition.

**❌ Why not the others:**
- **A** would require repetition, which this doesn't do.
- **C** and **D** describe different code constructs entirely.

**🎯 Example:** A bouncer checking ID at a club entrance — one path (in) if the condition is met, another (denied) if not.

---

### Q12. What is the output?
```
count = 0
while count < 3:
    print(count)
    count += 1
```
- **A.** 0 1 2
- **B.** 1 2 3
- **C.** 0 1 2 3
- **D.** Infinite loop

**✅ Correct Answer: A**

**💡 Why:** Starts at 0, prints while `count < 3` (so 0, 1, 2), then stops once count reaches 3.

**❌ Why not the others:**
- **B** wrongly starts at 1.
- **C** wrongly includes 3, which fails the loop condition.
- **D** is false — `count` increments every iteration, so the loop does terminate.

**🎯 Example:** A countdown-style check-in — you stop admitting people once you hit the capacity limit, right before crossing it.

---

<a id="topic-2"></a>
## Topic 2: Data Structures & Algorithms (Q13–Q24)

### Q13. Average time complexity of binary search on a sorted array of size n?

- **A.** O(n)
- **B.** O(n log n)
- **C.** O(log n)
- **D.** O(1)

**✅ Correct Answer: C**

**💡 Why:** Each step halves the search space (because the array is sorted). Repeated halving to reach 1 element takes about log₂(n) steps.

**❌ Why not the others:**
- **A** would be a plain linear scan, much slower.
- **B** is typical of good sorting algorithms, not searching.
- **D** would mean instant lookup regardless of size, which binary search doesn't achieve.

**🎯 Example:** Finding a word in a dictionary by repeatedly opening to the middle of the remaining pages.

---

### Q14. Worst-case time complexity of Quicksort?

- **A.** O(n log n)
- **B.** O(n²)
- **C.** O(log n)
- **D.** O(n)

**✅ Correct Answer: B**

**💡 Why:** Poor pivot choices (e.g., always the smallest/largest element) create unbalanced
partitions, degrading performance.

**❌ Why not the others:**
- **A** is Quicksort's average/best case, not worst case — a common mix-up trap.
- **C** and **D** are far too fast for a worst-case sorting bound.

**🎯 Example:** Sorting people by height by always picking the shortest person as pivot — splits off just one person per round.

---

### Q15. Which data structure gives near O(1) average lookup via hashing?

- **A.** Linked List
- **B.** Hash Map / Hash Table
- **C.** Binary Search Tree
- **D.** Stack

**✅ Correct Answer: B**

**💡 Why:** A hash function computes almost directly where a key is stored — lookup doesn't depend on how many items are stored.

**❌ Why not the others:**
- **A** requires walking node-by-node from the start (O(n)).
- **C** gives O(log n) on average — better than linear, but not O(1).
- **D** is designed for last-in-first-out access, not key-based lookup.

**🎯 Example:** A library where a book's shelf location is computed directly from its ISBN — no shelf-by-shelf scanning.

---

### Q16. Space complexity of an algorithm using a fixed number of extra variables, regardless of input size?

- **A.** O(n)
- **B.** O(n²)
- **C.** O(1)
- **D.** O(log n)

**✅ Correct Answer: C**

**💡 Why:** "Fixed number of extra variables" means the extra memory doesn't grow with input size — the definition of constant space.

**❌ Why not the others:**
- **A** and **B** both describe memory usage that grows with input size.
- **D** also grows, just more slowly.

**🎯 Example:** A calculator using 2-3 memory slots whether adding 2 numbers or 2 million.

---

### Q17. Which sorting algorithm is stable AND has O(n log n) worst-case complexity?

- **A.** Quicksort
- **B.** Merge Sort
- **C.** Selection Sort
- **D.** Bubble Sort

**✅ Correct Answer: B**

**💡 Why:** Merge Sort always splits the array evenly, guaranteeing O(n log n) even worst-case, and
preserves the relative order of equal elements (stable).

**❌ Why not the others:**
- **A** can degrade to O(n²) worst case (see Q14).
- **C** and **D** are both O(n²) even in typical cases.

**🎯 Example:** Repeatedly splitting a card deck in half, sorting each half, then merging back in order — consistent regardless of starting order.

---

### Q18. Time complexity of reversing a string via two pointers (swap, move inward)?

- **A.** O(n²)
- **B.** O(n)
- **C.** O(log n)
- **D.** O(1)

**✅ Correct Answer: B**

**💡 Why:** Each pointer traverses roughly half the string once — total work scales linearly with length.

**❌ Why not the others:**
- **A** would mean nested loops, which the two-pointer approach avoids by design.
- **C** and **D** are far too fast — every character has to be touched at least once.

**🎯 Example:** Two people at opposite ends of a line, swapping pairs and stepping inward, meeting in the middle.

---

### Q19. What's the key idea behind "problem decomposition"?

- **A.** Solving the whole problem in one giant function with no structure
- **B.** Breaking a large problem into smaller, independent sub-problems that are easier to solve and combine
- **C.** Avoiding functions altogether
- **D.** Only applicable to sorting problems

**✅ Correct Answer: B**

**💡 Why:** Big, complex problems become manageable when split into smaller pieces solved one at a time, then combined.

**❌ Why not the others:**
- **A** is the opposite approach.
- **C** removes the very tool that enables decomposition.
- **D** wrongly limits the idea to one narrow use case.

**🎯 Example:** Planning a wedding by breaking it into venue, catering, guest list, etc., rather than one giant undivided task.

---

### Q20. What is the time complexity of accessing an element by index in an array?

- **A.** O(n)
- **B.** O(log n)
- **C.** O(1)
- **D.** O(n²)

**✅ Correct Answer: C**

**💡 Why:** Arrays store elements in contiguous memory; the index directly computes the memory location — no searching needed.

**❌ Why not the others:**
- **A, B, D** all imply some form of searching or scanning, which direct indexing doesn't require.

**🎯 Example:** Knowing a house's exact street number lets you go straight there, no need to check every house on the street.

---

### Q21. Which data structure is best suited for Last-In-First-Out (LIFO) operations?

- **A.** Queue
- **B.** Stack
- **C.** Array (unordered)
- **D.** Hash Map

**✅ Correct Answer: B**

**💡 Why:** A Stack's defining behavior is that the most recently added item is the first one removed.

**❌ Why not the others:**
- **A** is First-In-First-Out (FIFO), the opposite behavior.
- **C** and **D** aren't defined by an access-order rule at all.

**🎯 Example:** A stack of plates — you take the top plate off first, the one placed most recently.

---

### Q22. Which data structure is best suited for First-In-First-Out (FIFO) operations?

- **A.** Stack
- **B.** Queue
- **C.** Binary Tree
- **D.** Hash Set

**✅ Correct Answer: B**

**💡 Why:** A Queue processes items in the order they arrived — the first one in is the first one out.

**❌ Why not the others:**
- **A** is LIFO, the opposite behavior (see Q21).
- **C** and **D** aren't defined by arrival-order access at all.

**🎯 Example:** A line at a ticket counter — the first person to join is served first.

---

### Q23. Time complexity of Breadth-First Search (BFS) on a graph with V vertices and E edges?

- **A.** O(V)
- **B.** O(E)
- **C.** O(V + E)
- **D.** O(V × E)

**✅ Correct Answer: C**

**💡 Why:** BFS visits every vertex once and examines every edge once (using an adjacency list), giving combined linear complexity in vertices + edges.

**❌ Why not the others:**
- **A** and **B** each account for only part of the work BFS actually does.
- **D** wildly overestimates — BFS doesn't compare every vertex against every edge.

**🎯 Example:** Visiting every room in a building (vertices) and walking through every doorway connecting them (edges) exactly once.

---

### Q24. In dynamic programming, "memoization" refers to:

- **A.** Deleting old computed results to save memory
- **B.** Storing (caching) results of expensive function calls and reusing them when the same inputs occur again
- **C.** A sorting technique
- **D.** A type of syntax error

**✅ Correct Answer: B**

**💡 Why:** Instead of recomputing the same sub-problem repeatedly (as in naive recursion),
memoization stores the result once and reuses it — turning exponential-time solutions into polynomial-time ones.

**❌ Why not the others:**
- **A** is the opposite of what memoization does.
- **C** and **D** are unrelated concepts.

**🎯 Example:** Writing down the answer to a repeated math sub-problem on scratch paper instead of recalculating it every time it comes up.

---

<a id="topic-3"></a>
## Topic 3: Software Engineering Fundamentals (Q25–Q36)

### Q25. Which OOP principle allows a subclass to redefine a parent's method?

- **A.** Encapsulation
- **B.** Polymorphism (method overriding)
- **C.** Abstraction
- **D.** Composition

**✅ Correct Answer: B**

**💡 Why:** A child class giving its own behavior to an inherited method name is method overriding — a form of polymorphism.

**❌ Why not the others:**
- **A** is about bundling data and methods together with access control.
- **C** is about hiding complex implementation details behind a simple interface.
- **D** is about building objects by combining other objects, not redefining behavior.

**🎯 Example:** `Animal.makeSound()` — `Dog` overrides it to bark, `Cat` overrides it to meow.

---

### Q26. Which SQL clause filters GROUPED results (after GROUP BY)?

- **A.** WHERE
- **B.** HAVING
- **C.** ORDER BY
- **D.** FILTER

**✅ Correct Answer: B**

**💡 Why:** `WHERE` filters individual rows before grouping happens. `HAVING` filters groups after aggregation has already been calculated.

**❌ Why not the others:**
- **A** runs too early to filter on aggregated values.
- **C** only controls sort order, not filtering.
- **D** isn't standard SQL syntax for this purpose.

**🎯 Example:** `WHERE` = checking individual marks before grouping by class. `HAVING` = "which classes average above 80%" — only makes sense after grouping.

---

### Q27. Which HTTP method updates an existing resource entirely?

- **A.** GET
- **B.** POST
- **C.** PUT
- **D.** DELETE

**✅ Correct Answer: C**

**💡 Why:** `PUT` conventionally replaces a resource's full data. (`PATCH` handles partial updates.)

**❌ Why not the others:**
- **A** only retrieves data, without changing anything.
- **B** is typically used to create a new resource.
- **D** removes a resource entirely, not update it.

**🎯 Example:** GET = read a profile. POST = create a new user. PUT = replace the whole profile. DELETE = remove the account.

---

### Q28. What does `git commit` do?

- **A.** Uploads code to a remote repository
- **B.** Saves a snapshot of staged changes to local repository history
- **C.** Deletes the current branch
- **D.** Merges two branches automatically

**✅ Correct Answer: B**

**💡 Why:** It saves a local checkpoint with a message — it does NOT send anything anywhere yet.

**❌ Why not the others:**
- **A** describes `git push`, a separate command.
- **C** and **D** are unrelated Git actions (`git branch -d`, `git merge`).

**🎯 Example:** Saving a checkpoint locally in a video game vs. uploading that save to the cloud (push).

---

### Q29. Which SQL keyword combines rows from two tables based on a related column?

- **A.** UNION
- **B.** JOIN
- **C.** GROUP BY
- **D.** DISTINCT

**✅ Correct Answer: B**

**💡 Why:** `JOIN` links tables via a shared column (e.g., `customer_id` appearing in both tables).

**❌ Why not the others:**
- **A** stacks results from two queries on top of each other, not linking by column.
- **C** groups rows within one result set for aggregation.
- **D** removes duplicate rows — unrelated to combining tables.

**🎯 Example:** Matching a student's ID across a "Students" table and a "Marks" table to see name next to marks.

---

### Q30. What is "encapsulation" in OOP?

- **A.** Making all variables public
- **B.** Bundling data and methods together and restricting direct access to internal state
- **C.** Deleting unused classes
- **D.** A database indexing technique

**✅ Correct Answer: B**

**💡 Why:** Encapsulation protects an object's internal state from being changed arbitrarily from outside, exposing only controlled access via methods.

**❌ Why not the others:**
- **A** is the opposite — encapsulation typically restricts direct access, doesn't open everything up.
- **C** and **D** are unrelated concepts.

**🎯 Example:** A car's engine internals are hidden under the hood; you interact with it only through the accelerator/brake.

---

### Q31. What is a "primary key" in a database table?

- **A.** Any random column
- **B.** A column (or set of columns) that uniquely identifies each row in a table
- **C.** A column that can have duplicate values
- **D.** A column used only for sorting

**✅ Correct Answer: B**

**💡 Why:** Every row must have a unique primary key value — it's how the database guarantees each record can be uniquely identified.

**❌ Why not the others:**
- **A** wrongly implies any column would work.
- **C** directly contradicts the uniqueness requirement.
- **D** describes an unrelated, secondary use case.

**🎯 Example:** A student's unique roll number — no two students in the same class share one.

---

### Q32. What is the purpose of a "foreign key" in a relational database?

- **A.** To encrypt a table
- **B.** To create a link between two tables by referencing another table's primary key, enforcing referential integrity
- **C.** To speed up all queries automatically
- **D.** To rename a column

**✅ Correct Answer: B**

**💡 Why:** A foreign key in one table points to a primary key in another, keeping relationships
valid and consistent (e.g., an `Orders` table's `customer_id` must point to a real `Customers` row).

**❌ Why not the others:**
- **A, C, D** describe unrelated database operations.

**🎯 Example:** A library card referencing a specific member ID — you can't issue a card for a member who doesn't exist in the members list.

---

### Q33. What does REST stand for, and what's one core REST principle?

- **A.** Random External State Transfer; no defined principles
- **B.** Representational State Transfer; it's typically stateless — each request from client to server contains all information needed
- **C.** Rapid Execution State Tool; requires a database
- **D.** Not a real acronym

**✅ Correct Answer: B**

**💡 Why:** REST APIs typically don't store client session state on the server between requests —
each request is self-contained, which improves scalability.

**❌ Why not the others:**
- **A, C, D** are all invented-sounding expansions or false claims.

**🎯 Example:** Each time you call a restaurant to place an order, you re-state your full order and address — the restaurant doesn't need to "remember" your previous call.

---

### Q34. What's the difference between `git merge` and `git rebase`, at a basic level?

- **A.** They are identical
- **B.** `merge` combines branch histories with a merge commit, preserving both histories as-is; `rebase` re-applies commits on top of another branch, creating a linear history
- **C.** `rebase` deletes all commit history
- **D.** `merge` only works on the main branch

**✅ Correct Answer: B**

**💡 Why:** Both integrate changes from one branch into another, but produce different resulting commit histories — merge keeps a branching structure, rebase creates a clean, linear sequence.

**❌ Why not the others:**
- **A** is false — they behave and result differently.
- **C** and **D** are false claims about how these commands work.

**🎯 Example:** Merge is like stapling two documents together as-is; rebase is like retyping one document's changes onto the end of the other, producing one continuous document.

---

### Q35. What is "abstraction" in OOP, and how does it differ from encapsulation?

- **A.** They're the same thing
- **B.** Abstraction hides complex implementation details behind a simple interface; encapsulation controls access to internal data
- **C.** Abstraction is only used in databases
- **D.** Encapsulation always requires inheritance

**✅ Correct Answer: B**

**💡 Why:** Abstraction is about simplifying what's exposed to the user; encapsulation is about
protecting and controlling access to internal data. Related, but distinct.

**❌ Why not the others:**
- **A** is a common fresher confusion — they're related but not identical.
- **C** and **D** are false, unrelated claims.

**🎯 Example:** A car's steering wheel and pedals are the abstraction (simple interface); the engine wiring being inaccessible under the hood is the encapsulation.

---

### Q36. What does "idempotent" mean for an HTTP method like PUT or DELETE?

- **A.** It means the request always fails the second time
- **B.** Calling it multiple times with the same input produces the same result/state as calling it once
- **C.** It means the method requires authentication
- **D.** It means the method is faster than others

**✅ Correct Answer: B**

**💡 Why:** `PUT`ting the same data twice, or `DELETE`ing the same resource twice, leaves the system
in the same end state as doing it once — important for reliable retries over unreliable networks.

**❌ Why not the others:**
- **A, C, D** are unrelated or false claims about what idempotency actually means.

**🎯 Example:** Pressing an elevator's "floor 5" button multiple times doesn't send the elevator to a different floor each time.

---

<a id="topic-4"></a>
## Topic 4: Modern Engineering Awareness (Q37–Q48)

### Q37. In client-server architecture, the "client" typically:

- **A.** Stores and serves data/resources
- **B.** Requests resources or services from a server
- **C.** Is always a physical server rack
- **D.** Is a database index

**✅ Correct Answer: B**

**💡 Why:** The client asks (requests); the server provides.

**❌ Why not the others:**
- **A** describes the server's role, the opposite.
- **C** and **D** are unrelated hardware/database concepts.

**🎯 Example:** You (client) order food at a restaurant; the kitchen (server) prepares and sends it.

---

### Q38. Main difference between an API key and an OAuth token?

- **A.** They're identical
- **B.** API keys are typically static, long-lived identifiers for a project/app; OAuth tokens are often short-lived, scoped credentials tied to a user session
- **C.** Tokens never expire
- **D.** API keys are only for databases

**✅ Correct Answer: B**

**💡 Why:** Tokens commonly expire (a security feature, not a flaw); API keys identify the calling app/project and often persist longer.

**❌ Why not the others:**
- **A** is false — the whole point here is that they behave differently.
- **C** is false — expiry is a deliberate security feature of many tokens.
- **D** is false — API keys are used across many kinds of APIs.

**🎯 Example:** API key = a permanent staff ID card. Token = a visitor's day-pass that expires and only opens certain floors.

---

### Q39. What does Docker primarily provide?

- **A.** Version control
- **B.** Containerization — packaging an app with dependencies to run consistently across environments
- **C.** A programming language
- **D.** A database engine

**✅ Correct Answer: B**

**💡 Why:** Solves "it works on my machine" by bundling everything the app needs into a portable container.

**❌ Why not the others:**
- **A** describes Git, a different tool.
- **C** and **D** are also unrelated categories.

**🎯 Example:** Shipping a fully-packed lunch box with everything included, instead of hoping the destination has matching plates and forks.

---

### Q40. In Agile, a "sprint" refers to:

- **A.** A single line of code
- **B.** A fixed, short time-boxed period (commonly 1-4 weeks) to complete a set of work
- **C.** A database query type
- **D.** A cybersecurity protocol

**✅ Correct Answer: B**

**💡 Why:** Short iterative cycles with review and replanning are core to Agile's incremental approach.

**❌ Why not the others:**
- **A, C, D** are all unrelated technical terms borrowed from other domains.

**🎯 Example:** Reviewing study goals every 2 weeks instead of planning an entire semester in one go.

---

### Q41. Which is a basic cybersecurity best practice?

- **A.** Hardcoding credentials directly in source code in a public repo
- **B.** Using environment variables/secret managers, never committing secrets to version control
- **C.** Reusing the same password everywhere
- **D.** Disabling HTTPS for "speed"

**✅ Correct Answer: B**

**💡 Why:** Keeps credentials out of the codebase entirely, so they're never exposed if code is shared or leaked.

**❌ Why not the others:**
- **A** is one of the most common real-world security mistakes.
- **C** means one leaked password compromises every system you used it on.
- **D** removes encryption in transit for a tiny speed gain not worth the risk.

**🎯 Example:** Keeping your house key with trusted people only, not posting its location on a public noticeboard.

---

### Q42. What is the main purpose of a load balancer in a client-server system?

- **A.** To encrypt all traffic
- **B.** To distribute incoming requests across multiple servers, improving reliability and handling higher traffic
- **C.** To store user passwords
- **D.** To compile code faster

**✅ Correct Answer: B**

**💡 Why:** Prevents any single server from being overwhelmed by spreading requests across a pool of
servers — improves both performance and fault tolerance.

**❌ Why not the others:**
- **A, C, D** describe unrelated functions.

**🎯 Example:** A supermarket opening multiple checkout counters and directing customers to whichever is free.

---

### Q43. What does "CI/CD" stand for in DevOps, and what's its core benefit?

- **A.** Code Isolation / Code Deployment; no real benefit
- **B.** Continuous Integration / Continuous Deployment (or Delivery) — automatically building, testing, and deploying code changes frequently and reliably
- **C.** Central Index / Central Directory; a database term
- **D.** It's unrelated to software

**✅ Correct Answer: B**

**💡 Why:** CI automatically builds and tests code on every change; CD automates getting tested changes into production — reducing manual error and speeding up delivery.

**❌ Why not the others:**
- **A, C, D** are invented-sounding expansions or false claims.

**🎯 Example:** An assembly line that automatically checks quality at every stage and ships the finished product, instead of manually inspecting each item by hand.

---

### Q44. What is the main advantage of cloud computing over traditional on-premise servers?

- **A.** It's always completely free
- **B.** On-demand, scalable computing resources without owning/maintaining physical hardware
- **C.** It requires no internet connection
- **D.** It eliminates the need for any security practices

**✅ Correct Answer: B**

**💡 Why:** You can scale resources up or down as needed and pay for what you use, without buying and maintaining physical servers yourself.

**❌ Why not the others:**
- **A** is false — cloud computing is typically pay-as-you-go, not free.
- **C** is false — cloud computing fundamentally requires network/internet connectivity.
- **D** is false and dangerous thinking — security practices remain essential in the cloud.

**🎯 Example:** Renting a car when you need one instead of buying and maintaining one you rarely use.

---

### Q45. What is the purpose of an "environment variable" in software configuration?

- **A.** To change the color scheme of an IDE
- **B.** To store configuration values (like API keys, database URLs) outside the source code, so they can differ per environment without code changes
- **C.** To slow down execution intentionally
- **D.** To define a new programming language

**✅ Correct Answer: B**

**💡 Why:** Keeps configuration and secrets separate from code, so the same code can run against
different databases/settings in dev, test, and production just by changing the environment variables.

**❌ Why not the others:**
- **A, C, D** are unrelated or false claims about what environment variables do.

**🎯 Example:** Using a different delivery address depending on whether you're testing an order process or placing a real order — same process, different configuration.

---

### Q46. What is a basic definition of "networking latency"?

- **A.** The amount of storage a server has
- **B.** The time delay between sending a request and receiving a response over a network
- **C.** The number of users on a website
- **D.** A type of encryption

**✅ Correct Answer: B**

**💡 Why:** Latency measures delay, not data volume, user count, or throughput.

**❌ Why not the others:**
- **A, C, D** describe unrelated metrics or concepts.

**🎯 Example:** The pause between asking someone a question over a long-distance phone call and actually hearing their answer.

---

### Q47. What does "version control" (like Git) fundamentally provide?

- **A.** A way to compile code faster
- **B.** A system for tracking changes to files over time, enabling collaboration, history, and rollback to previous states
- **C.** A cloud hosting service
- **D.** An encryption algorithm

**✅ Correct Answer: B**

**💡 Why:** Every commit is a tracked snapshot, letting teams collaborate, see who changed what, and revert to earlier working versions if something breaks.

**❌ Why not the others:**
- **A, C, D** describe unrelated tools or functions.

**🎯 Example:** Track-changes in a shared document, but far more powerful — with a full history of every version and the ability to jump back to any point.

---

### Q48. What is the difference between a Docker "image" and a Docker "container"?

- **A.** They are identical terms
- **B.** An image is a static, packaged blueprint (app + dependencies); a container is a running instance of that image
- **C.** A container is used only for databases
- **D.** An image can only be used once

**✅ Correct Answer: B**

**💡 Why:** The image is the recipe/template; the container is the actual running process created from that template — you can start multiple containers from the same single image.

**❌ Why not the others:**
- **A** is false — they're related but distinct concepts.
- **C** and **D** are false claims about their usage.

**🎯 Example:** A cake recipe (image) vs. an actual baked cake (container) — you can bake multiple cakes from the same recipe.


---

<a id="-continue-reading"></a>
## Continue reading

[🏠 Home](../README.md) · [⬅ Previous: AI Literacy](./01-ai-literacy.md) · [Next: Debugging Assessment ➡](./03-debugging-assessment.md)
