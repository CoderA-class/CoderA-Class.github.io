# 3. Product Backlog: RDM IT Portal

[Back to contents](index.html)


## Part A: Evidence

### What the product backlog is

The product backlog is the single, ordered list of everything the portal needs: features, improvements, technical work and bug fixes. My mentor (as Product Owner) decides the priority, and I estimate and refine items. It is a living list. It changed after nearly every weekly demo.

### How items are prioritised

| Label | Meaning |
|---|---|
| **Must** | Portal cannot go live without it |
| **Should** | Important, but a workaround exists |
| **Could** | Nice to have if time allows |
| **Won't (now)** | Agreed for a later release |

### Backlog (ordered by priority)

| ID | Item | Type | Story | Priority | Points | Status | Sprint |
|---|---|---|---|---|---|---|---|
| PB-01 | Set up Flask project structure and SQL Server connection | Technical | n/a | Must | 5 | Done | Early sprints |
| PB-02 | Design database tables for documents, categories and links | Technical | n/a | Must | 3 | Done | Early sprints |
| PB-03 | Base layout and navigation | Feature | US-07 | Must | 3 | Done | Early sprints |
| PB-04 | Induction documents page | Feature | US-01 | Must | 5 | Done | Early sprints |
| PB-05 | Training documents page with categories | Feature | US-02 | Must | 5 | Done | Mid sprints |
| PB-06 | Company-connected sites directory | Feature | US-03 | Must | 3 | Done | Mid sprints |
| PB-07 | Secure access (login) [CONFIRM] | Feature | US-05 | Must | 8 | Done | Mid sprints |
| PB-08 | Admin: add, edit and remove content | Feature | US-06 | Must | 8 | Done | Mid sprints |
| PB-09 | Search | Feature | US-04 | Should | 5 | Done | Later sprints |
| PB-10 | Apply feedback from demos (layout and wording fixes) | Improvement | US-08 | Should | 3 | Done | Continuous |
| PB-11 | Input validation and friendly error messages | Technical | US-05/06 | Should | 3 | Done | Later sprints |
| PB-12 | Responsive design and cross-browser testing | Improvement | US-07 | Should | 3 | Done | Later sprints |
| PB-13 | Bug fixes found during testing | Bug | n/a | Must | 5 | Done / ongoing | Continuous |
| PB-14 | Final testing and handover documentation | Technical | US-08 | Must | 3 | In progress | Current |
| PB-15 | Sign-off by mentor and stakeholders | Milestone | US-08 | Must | n/a | **Waiting** | Pending |
| PB-16 | Deploy to the live environment (with IT) | Technical | n/a | Must | 5 | Blocked until sign-off | Pending |
| PB-17 | Usage analytics (which content is opened most) | Feature | n/a | Could | 5 | Not started | Future |
| PB-18 | Notifications when new training is added | Feature | n/a | Could | 8 | Not started | Future |
| PB-19 | Favourites / personalised view for each employee | Feature | n/a | Won't (now) | 8 | Not started | Future |



### Refinement notes

- After each weekly demo I added feedback to the backlog and re-ordered it with my mentor.
- Items too large for one week were split into smaller stories.
- Ideas outside the agreed scope were parked rather than built, to protect the release date.

**Board:** [Trello board](trello.html) 

---

## Part B: Reflection

**What I did.** I created and maintained a prioritised list of everything the portal needed, and I updated it after each demo as my mentor gave feedback and as I learned more.

**What I learned.** The backlog is not a to-do list. It is a *conversation* between the developer and the Product Owner about value. Using  labels made it easy to explain why one item came before another, and it let me say "not now" without a disagreement. I also learned that keeping future ideas (analytics, notifications) visible but unbuilt stops scope creep and still shows I listened to the user needs.

**What was difficult.** The hardest part was balancing new feedback against the work I had already planned. Some feedback was small but touched many pages, so it was larger than it looked, and I had to estimate it honestly.

**What I would do differently.** I would record the *reason* for each priority change in the backlog, and I would track velocity (points completed per sprint) so I could forecast when work will finish rather than guessing.

**Link to my studies.** This links to project management concepts such as scope management and prioritisation, and to the idea of delivering value early and often.
