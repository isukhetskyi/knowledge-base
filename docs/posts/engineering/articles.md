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


###[Mistakes I see engineers making in their code reviews](https://www.seangoedecke.com/good-code-reviews/) by [Sean Goedecke.](https://www.seangoedecke.com/)

***

Here is a summary of the post, formatted in Markdown and under 250 words.

***

The author argues that with the rise of AI-generated code, effective code review is more important than ever. However, many engineers make key mistakes.

The biggest error is **reviewing only the diff**. The most valuable comments come from a holistic understanding of the system, such as pointing out existing code or ensuring the change maintains long-term consistency.

The author outlines five key principles for better reviews:

1.  **Don't leave too many comments:** A good review has 5-6 high-impact comments. A hundred comments obscure the important feedback.
2.  **Avoid the "how would I write it?" filter:** Reviewers should approve acceptable solutions, even if they differ from their personal "taste," to avoid needless conflict and churn.
3.  **Use blocking reviews clearly:** If a change *must not* be merged, use a formal blocking review. Don't leave ambiguous, critical comments on a non-blocking review.
4.  **Bias towards approval:** In a standard SaaS codebase, most reviews should be approvals. A high rate of blocking reviews often signals a structural problem, like gatekeeping or misaligned team incentives.
5.  **Review AI code differently:** These rules apply to AI-generated code, *except* for the bias to approve. The author states you "can and should gatekeep AI-generated PRs as much as you want."