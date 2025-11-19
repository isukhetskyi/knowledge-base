### [System Design Interview Questions & Prep (from FAANG experts)](https://igotanoffer.com/blogs/tech/system-design-interviews) - by [Max Serrano.](https://igotanoffer.com/en/author/max-serrano)

***

System design interviews are 45-60 minute, open-ended sessions where candidates are given a broad prompt, such as "Design Instagram," to assess their ability to create scalable, reliable, and maintainable systems.

Interview expectations vary significantly by level. 

**Entry-level** candidates face basic questions (e.g., "Design TinyURL") and are judged on foundational reasoning and clear communication, not a production-ready design. 

**Mid-level** engineers must drive the conversation, discussing scaling, data flow, and fault tolerance for systems like a newsfeed. 

**Senior/Staff** engineers tackle complex distributed systems (e.g., collaborative docs), must own the entire design process, and deeply analyze trade-offs and edge cases.

Interviews cover High-Level Design (HLD)—the overall architecture, components, and data flows—and Low-Level Design (LLD)—the implementation details like classes, APIs, and data models. Seniors focus on HLD, while mid-level candidates typically cover both.

The article provides common "Design X" questions (e.g., messaging apps, file-sharing systems) and foundational knowledge questions for juniors (e.g., "What is a CDN?," "SQL vs. NoSQL?").

A successful preparation strategy involves learning core concepts (caching, sharding, load balancing) and applying a 4-step framework:
1.  **Ask clarifying questions** to define scope.
2.  **Create a high-level design.**
3.  **Drill down** on key components.
4.  **Bring it all together,** discussing trade-offs.

Experts stress that practicing mock interviews out loud is critical for mastering communication and problem-scoping.


### [Mistakes I see engineers making in their code reviews](https://www.seangoedecke.com/good-code-reviews/) by [Sean Goedecke.](https://www.seangoedecke.com/)

***

The author argues that with the rise of AI-generated code, effective code review is more important than ever. However, many engineers make key mistakes.

The biggest error is **reviewing only the diff**. The most valuable comments come from a holistic understanding of the system, such as pointing out existing code or ensuring the change maintains long-term consistency.

The author outlines five key principles for better reviews:

1.  **Don't leave too many comments:** A good review has 5-6 high-impact comments. A hundred comments obscure the important feedback.
2.  **Avoid the "how would I write it?" filter:** Reviewers should approve acceptable solutions, even if they differ from their personal "taste," to avoid needless conflict and churn.
3.  **Use blocking reviews clearly:** If a change *must not* be merged, use a formal blocking review. Don't leave ambiguous, critical comments on a non-blocking review.
4.  **Bias towards approval:** In a standard SaaS codebase, most reviews should be approvals. A high rate of blocking reviews often signals a structural problem, like gatekeeping or misaligned team incentives.
5.  **Review AI code differently:** These rules apply to AI-generated code, *except* for the bias to approve. The author states you "can and should gatekeep AI-generated PRs as much as you want."


### [Good software development habits](https://zarar.dev/good-software-development-habits/) by [Zarar's blog](https://zarar.dev/me/)


***

The author outlines ten personal habits adopted to increase speed and maintain quality in software development. The core philosophy emphasizes pragmatism, continuous improvement, and ease of change.

**Key habits include:**

* **Micro-Commits:** Keep commits extremely small to simplify reverts and avoid merge conflicts.
* **Continuous Refactoring:** Follow Kent Beck’s advice: "Make the change easy, then make the easy change." Small, frequent refactors are superior to massive overhauls.
* **Deploy Frequently:** Treat undeployed code as a liability. Frequent deploys prove progress, while tests provide confidence.
* **Pragmatic Testing:** Avoid testing framework capabilities. Use TDD to design APIs from a consumer perspective, but avoid dogma. If code is hard to test, it usually indicates poor design.
* **The Rule of Three:** Copy-pasting is acceptable once. If code is duplicated a third time, it must be abstracted to prevent divergence.
* **Modularization:** If a function doesn't fit an existing module, create a new one rather than forcing it where it doesn't belong.
* **Prioritize Technical Debt:** Focus only on debt that blocks current work or will definitely block future work. Ignore hypothetical future problems.
* **Embrace Design Decay:** Accept that designs inevitably go stale. Success is defined by how well you manage change, not by creating a perfect, static design.


### [Stop postponing things by embracing the mess](https://www.deprocrastination.co/blog/stop-postponing-things-by-embracing-the-mess) by [deprocrastination blog.](https://www.deprocrastination.co/)

***

The article argues that we procrastinate because we view "today" as messy and imperfect, while holding onto a false, simplified belief that "tomorrow will be better" and more productive. When today inevitably deviates from our perfect expectations (e.g., a meeting is canceled, we wake up late), we feel justified in getting distracted and putting off work.

The solution is to **"Embrace the mess."** This means accepting that the perfect, motivated moment is not coming. When interruptions happen, the correct response is to simply **"Reset"** and make the best of the current situation.

To cultivate this mindset, the author suggests:

* **Don't be "precious" about routines:** They make us fragile and give us an excuse to procrastinate when broken.
* **View work in small chunks (15-30 minutes):** Don't build tasks up into 8-hour-long behemoths.
* **Accept imperfect focus:** Our concentration naturally wanes; what matters is not getting sidetracked during the lulls.
* **Aim for "good enough" productivity:** Treat productivity as a spectrum (aiming for 50%) rather than an all-or-nothing (100% or 0%) switch.

Ultimately, the core principle is that **imperfect action is always better than perfect inaction**. We discover the "right" way to do something *by* starting, not by waiting.


### [Falsehoods Junior Developers believe about becoming Senior](https://vadimkravcenko.com/shorts/falsehoods-junior-developers-believe-about-becoming-senior) by [Vadim Kravcenko.](https://vadimkravcenko.com/)

***

Many junior developers romanticize the senior role, believing it grants ultimate knowledge and an escape from "boring" work. This essay debunks common "falsehoods" juniors believe about seniority, revealing a more complex and nuanced reality.

The author explains that career advancement is less about technical magic (like mastering terminal shortcuts) and more about embracing new responsibilities. The complexity of the problems a developer faces simply grows with their skill.

Here are the key myths and their corresponding realities:

* **Having All the Answers**
    * **Myth:** Seniors can solve any bug in minutes.
    * **Reality:** Seniority is not about possessing all knowledge but about effectively working with uncertainty. The job is to find solutions, which often means being comfortable saying, "I don't know" and then asking the right questions to figure it out.

* **Working with Latest Tech**
    * **Myth:** Seniors get to build exciting new projects.
    * **Reality:** A significant part of the role involves maintaining, debugging, and patching legacy systems that house years of critical business logic.

* **No More Boring Tasks**
    * **Myth:** Seniority means avoiding mundane work.
    * **Reality:** The role is filled with meetings, documentation, and code reviews. While often tedious, these tasks are essential for team alignment, maintainability, and mentoring, which seniors eventually find rewarding.

* **Making Big Changes**
    * **Myth:** Seniors can immediately implement their million-dollar ideas.
    * **Reality:** Real change requires building a business case, getting management approval, and aligning with budgets and organizational goals.

* **Time to Relax**
    * **Myth:** Seniors have a perfect work-life balance.
    * **Reality:** The workload evolves. With more responsibility for mentoring, planning, and project delivery, work often extends into personal time.

* **Deciding What to Do**
    * **Myth:** Seniors just tell others what to do.
    * **Reality:** Seniors are expected *to know* what needs to be done, transitioning from well-defined tasks to ambiguous, high-level problems (e.g., "Integrate AI into HR"). This autonomy comes with pressure and anxiety.

* **Becoming Irreplaceable**
    * **Myth:** Seniority equals job security.
    * **Reality:** No one is irreplaceable. Economic shifts, strategy changes, or project cancellations can lead to layoffs at all levels. True security comes from being a lifelong learner and staying adaptable.


### [Conscious Debugging: 10 Effective Strategies That Actually Work 🐛](https://thetshaped.dev/p/conscious-debugging-10-effective-debugging-strategies-debug-like-pro) - by [Petar Ivanov.](https://thetshaped.dev/)

***

Debugging is a skill that can be mastered with the right mindset and strategies. This article outlines ten practical techniques to find and fix bugs efficiently, saving time and frustration.

**Part 1: Set Yourself Up For Success**
*   **Reproduce Consistently:** Create step-by-step instructions to trigger the bug every time. Understand the full flow, especially in microservices.
*   **Reproduce Quickly:** Optimize your environment to jump straight to the problematic state, saving time on every iteration.
*   **Capture Full Context:** Gather all available information (logs, user actions, system state) before diving in. Tools like session replays can be invaluable here.

**Part 2: Active Debugging Techniques**
*   **Isolate the Problem:** Use a "binary search" approach—comment out half the code or use breakpoints to narrow down the scope quickly.
*   **Use Your Debugger:** Don't just guess. Use breakpoints, inspect variables, and step through code to see the actual execution flow.
*   **Rubber Duck It:** Explain your code line-by-line to an inanimate object (or colleague). Speaking aloud often reveals assumptions you didn't know you had.
*   **Form & Test Hypotheses:** Apply the scientific method: Form a hypothesis -> Experiment (log/break) -> Observe -> Fix -> Verify. Avoid random changes.

**Part 3: When You’re Stuck**
*   **Document Progress:** Keep a log of what you've tried to avoid repeating failed experiments and to make asking for help easier.
*   **Take Strategic Breaks:** Step away (walk, rest) to let your subconscious process the problem. Solutions often appear when you disengage.
*   **Leverage AI Smartly:** Use AI tools as debugging partners. Provide them with full context (logs, code, recordings) to generate hypotheses you might have missed.