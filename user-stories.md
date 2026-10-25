# 2. User Stories and Tasks: RDM IT Portal

[Back to contents](index.html)

> **Edit these stories so they match what you actually built.** I kept them generic on purpose, so no confidential details are exposed.

---

## Part A: Evidence

### How I write stories

Every story follows the format:

> **As a** [type of user], **I want** [a feature], **so that** [benefit].

Each story has acceptance criteria (how we know it works), a story-point estimate (1, 2, 3, 5, 8) and a list of tasks. Stories are small enough to finish within a one-week sprint.

### Users (personas)

| User | Description |
|---|---|
| **Employee** | Any RDM staff member, including new starters, who uses the portal to learn and find resources |
| **Content administrator** | A staff member responsible for keeping documents and links up to date |
| **Mentor / Product Owner** | Reviews progress and signs off the system |

---

### US-01: Access induction documents

**As a** new employee, **I want** to find and open the induction documents in one place, **so that** I can settle into the company without asking colleagues for files.

**Acceptance criteria**
- Induction documents are listed under a clear section.
- Selecting a document opens or downloads it.
- A document that is missing shows a friendly message, not an error page.

**Estimate:** 5 points

| Task | Description | Est. hours |
|---|---|---|
| T-01.1 | Design the page layout (HTML/CSS) | 3 |
| T-01.2 | Create SQL Server table for documents | 2 |
| T-01.3 | Build Flask route to read documents | 3 |
| T-01.4 | Display documents in the page | 3 |
| T-01.5 | Test open/download and missing-file case | 2 |

---

### US-02: Access training documents

**As an** employee, **I want** to browse training material by category, **so that** I can find the right training for my job.

**Acceptance criteria**
- Training documents are grouped by category.
- Categories can be selected to filter the list.
- The list loads from the database.

**Estimate:** 5 points

| Task | Description | Est. hours |
|---|---|---|
| T-02.1 | Add category field/table in SQL Server | 2 |
| T-02.2 | Build Flask route with category filter | 3 |
| T-02.3 | Build category navigation (HTML/CSS) | 3 |
| T-02.4 | Add JavaScript for smooth filtering | 2 |
| T-02.5 | Test each category | 2 |

---

### US-03: Quick links to company-connected sites

**As an** employee, **I want** a directory of external sites connected to the company, **so that** I can open them from one place instead of searching for each address.

**Acceptance criteria**
- Links are displayed with a clear name and short description.
- Links open the correct site (in a new tab).
- Links are grouped logically.

**Estimate:** 3 points

| Task | Description | Est. hours |
|---|---|---|
| T-03.1 | Create links table in SQL Server | 1 |
| T-03.2 | Build Flask route to retrieve links | 2 |
| T-03.3 | Design link cards (HTML/CSS) | 3 |
| T-03.4 | Test every link opens correctly | 1 |

---

### US-04: Search for content

**As an** employee, **I want** to search by keyword, **so that** I can find a document or site quickly.

**Acceptance criteria**
- A search box is available on the main pages.
- Results show matching documents and links.
- "No results" shows a helpful message.

**Estimate:** 5 points

| Task | Description | Est. hours |
|---|---|---|
| T-04.1 | Add search input to the interface | 2 |
| T-04.2 | Write parameterised SQL search query | 3 |
| T-04.3 | Display results page | 3 |
| T-04.4 | Handle empty results | 1 |
| T-04.5 | Test with different search terms | 2 |

---

### US-05: Secure access [CONFIRM how login works in your system]

**As the** company, **we want** only authorised staff to use the portal, **so that** internal information stays protected.

**Acceptance criteria**
- Users must be authenticated before seeing portal content.
- Passwords or credentials are never stored in plain text.
- Unauthorised users receive a clear message and are redirected.

**Estimate:** 8 points

| Task | Description | Est. hours |
|---|---|---|
| T-05.1 | Design the authentication approach with mentor | 2 |
| T-05.2 | Implement login/logout in Flask | 6 |
| T-05.3 | Protect routes | 3 |
| T-05.4 | Secure database access (parameterised queries) | 2 |
| T-05.5 | Test valid/invalid access | 3 |

---

### US-06: Manage documents and links

**As a** content administrator, **I want** to add, edit and remove documents and links, **so that** the portal always shows current information.

**Acceptance criteria**
- An administrator can add a new item.
- An administrator can edit and remove items.
- Normal employees cannot see the admin functions.
- Removing an item asks for confirmation.

**Estimate:** 8 points

| Task | Description | Est. hours |
|---|---|---|
| T-06.1 | Build admin forms (HTML/CSS) | 4 |
| T-06.2 | Flask create/update/delete routes | 6 |
| T-06.3 | Validate form input | 2 |
| T-06.4 | Restrict by role | 3 |
| T-06.5 | Test add/edit/delete | 3 |

---

### US-07: Consistent navigation and layout

**As an** employee, **I want** a clear menu and consistent layout on every page, **so that** I always know where I am and how to get back.

**Acceptance criteria**
- A consistent header and menu appear on all pages.
- Layout works on common screen sizes.
- The company look and feel is applied.

**Estimate:** 3 points

| Task | Description | Est. hours |
|---|---|---|
| T-07.1 | Create a shared base template (Jinja) | 2 |
| T-07.2 | Style navigation (CSS) | 3 |
| T-07.3 | Responsive tweaks | 2 |
| T-07.4 | Cross-browser check | 1 |

---

### US-08: Act on demo feedback and prepare for sign-off

**As the** mentor, **I want** feedback from each demo to be fixed and re-shown, **so that** I can approve the portal for go-live.

**Acceptance criteria**
- Feedback is recorded after every demo.
- Each item becomes a backlog item or is rejected with a reason.
- Fixes are shown in the following demo.

**Estimate:** Ongoing (about 2 points per sprint)

| Task | Description | Est. hours |
|---|---|---|
| T-08.1 | Record feedback after each demo | 0.5 |
| T-08.2 | Convert feedback into backlog items | 1 |
| T-08.3 | Fix and retest | varies |
| T-08.4 | Prepare final handover notes | 3 |

---

## Part B: Reflection

**What I did.** I broke the portal into user stories from the viewpoint of the people who would use it (employees, administrators and my mentor), and then split each story into tasks small enough to finish in a day or less.

**What I learned.** Writing "so that..." forced me to explain *why* a feature exists. Several times, when I could not write a clear benefit, I realised the feature was not needed yet. Acceptance criteria were the most useful part: they gave me and my mentor a shared checklist for the demo, and they stopped features from growing in size. Estimating in hours per task and points per story also taught me that my first guesses were usually too optimistic, especially for security and testing work.

**What was difficult.** Stories involving login and admin permissions were the hardest to size, because they touch every other part of the system. I had to split them into smaller tasks to make them manageable.

**What I would do differently.** I would write the acceptance criteria *with* my mentor in the planning meeting instead of alone, and I would track real hours against estimates so my later estimates improve.

**Link to my studies.** This applies what I learned about requirements gathering and systems analysis and design, and shows the difference between a requirement written in a document and one that is testable.
