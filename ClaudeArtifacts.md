# Claude Artifacts — Complete Guide (Telugu-English Mix)

> **Idi enti?** Claude Artifacts = Claude chat lo directly create chesina **interactive, live-rendered files**.
> Code block kadu — ivi live run avutay, meeru interact cheyyadam possible, share cheyyadam possible.

---

## Architecture Diagram

```
[User Prompt in Claude.ai Chat]
          |
          v
[Claude generates code/content]
          |
          v
+-----------------------------+
|      Artifacts Panel        |
|   (right side of chat)      |
|   Live Preview (rendered)   |  <- directly interact cheyyadam
+-----------------------------+
          |
          +---> Download  (as .html/.jsx/.md file)
          +---> Publish   (public shareable link)
          +---> Remix     (others can fork)
          +---> Embed     (website lo iframe)
          +---> Iterate   (chat lo refine)
```

## Deep Architecture Notes

- **Step 1:** Chat lo describe chestam — "HTML artifact create cheyyi for X"
- **Step 2:** Claude code generate chesi Artifacts panel lo live render chestundi
- **Step 3:** Preview lo interact cheyyachu, errors telustunayi
- **Step 4:** Chat lo feedback isthe Claude update chestundi (versioning)
- **Step 5:** Publish → public URL → anyone access cheyyachu
- **Step 6:** Remix → others fork chesi modify cheyyachu
- **Step 7:** Storage API → artifact data persist cheyyachu

---

# PART 1: Artifacts Ante Enti?

**Artifact** = Claude chat lo produce chesina **self-contained, interactive output**.

```
Normal code block:
  Claude code text istundi -> meeru copy chesi run cheyyali

Artifact:
  Claude generates HTML/React/SVG
  -> RIGHT SIDE PANEL lo LIVE render avutundi
  -> Meeru ikkade directly interact cheyyachu
  -> Separate standalone file -- chat kadu
```

**Analogy:**
```
Code block = Recipe card (instructions raasindi)
Artifact   = Ready dish on plate (directly eat cheyyochu)
```

## Artifacts vs Regular Code

| Feature | Code Block | Artifact |
|---|---|---|
| Display | Plain text | Live rendered |
| Interaction | None | Click, type, drag |
| Running | Copy then run | Runs inside Claude |
| Sharing | Share code text | Share live link |
| Versioning | No | Yes |

---

# PART 2: Artifact Types — 6 Types

## Type 1: HTML Artifact

Complete HTML page — CSS, JavaScript anni inline.

```
Use cases:
  Calculators, games (Tetris, Wordle, Snake),
  dashboards, forms, landing pages, data visualizers

Supported via CDN:
  Tailwind CSS, Chart.js, D3.js, Bootstrap, Alpine.js
```

**Prompt example:**
```
"Create an HTML artifact: BMI calculator with height/weight
 sliders, color-coded result (green/yellow/red), Tailwind CSS"
```

---

## Type 2: React (JSX) Artifact

React components — hooks, state management. Most powerful type.

```
Use cases:
  Kanban boards, todo apps, data dashboards,
  multi-step forms, games with complex state

Pre-loaded (no import needed):
  react, react-dom, recharts, lucide-react,
  shadcn/ui, Tailwind CSS

Babel in-browser transpile chestundi — no build step!
```

**Prompt example:**
```
"Build a React artifact: Kanban board with draggable cards across
 Todo/In Progress/Done, useState, Tailwind styling, add/delete cards"
```

---

## Type 3: SVG Artifact

Vector graphics — diagrams, icons, architecture illustrations.

```
Use cases:
  System architecture diagrams, org charts,
  flowcharts, infographics, custom icons
```

---

## Type 4: Mermaid Diagram

Text-based diagrams — code raasthe diagram render avutundi.

```
Types:
  flowchart       -- process flows, decisions
  sequenceDiagram -- API calls, system interactions
  classDiagram    -- OOP relationships
  gantt           -- project timelines
  erDiagram       -- database schemas
  stateDiagram    -- state machines
  gitGraph        -- git branches
```

**Example Mermaid code:**
```
sequenceDiagram
  Browser->>API: POST /login
  API->>Auth: validate()
  Auth-->>Browser: JWT token
```

---

## Type 5: Markdown Artifact

Formatted documents — reports, docs, README files.

```
Use cases:
  Technical docs, API specs, meeting notes,
  project proposals, blog drafts
```

---

## Type 6: PDF Artifact

Formal printable documents.

```
Use cases:
  Business reports, invoices, contracts,
  executive summaries, academic papers
```

---

## Types Summary

| Type | File | Best For | Interactive? |
|---|---|---|---|
| **HTML** | `.html` | Apps, games, dashboards | Yes |
| **React JSX** | `.jsx` | Complex stateful apps | Yes — full |
| **SVG** | `.svg` | Diagrams, illustrations | Optional |
| **Mermaid** | `.mmd` | Technical diagrams | No |
| **Markdown** | `.md` | Documents, reports | No |
| **PDF** | `.pdf` | Print, formal docs | No |

---

# PART 3: Create Cheyyadam — Step by Step

## Step 1: Enable

```
Claude.ai -> Settings (gear) -> Features -> Artifacts -> Enable
OR: automatically shows when Claude creates renderable content
```

## Step 2: Prompt Formula

```
"Create a [TYPE] artifact: [WHAT], [FEATURES], [STYLING], [BEHAVIOR]"

HTML:
  "Create an HTML artifact: expense tracker with add/delete,
   category filter, total, dark theme, Tailwind CSS"

React:
  "Build a React artifact: quiz app, 10 questions, progress bar,
   score tracking, useState, reveal correct/wrong on submit"

Mermaid:
  "Create a Mermaid sequence diagram: RAG pipeline --
   query -> embed -> vector search -> LLM -> response"
```

## Step 3: Iterate

```
Artifact create ayyaka chat lo continue:
  "Change color scheme to dark blue"
  "Add a download button"
  "Fix the delete bug"
  "Make it mobile responsive"
  "Convert HTML to React with hooks"

Prathi message = new version. Version history navigate cheyyachu.
```

## Step 4: Download or Publish

```
Download -> .html/.jsx/.md file -> own server lo host cheyyachu

Publish  -> Public URL generate avutundi
            Anyone (no Claude account) access cheyyachu
            Embed code kuda istundi
```

---

# PART 4: Hosting Options

## Option 1: Claude Cloud (Built-in, Free)

```
Publish button -> Anthropic cloud lo host avutundi
URL: claude.ai/artifacts/[id]
Zero cost, zero setup

Features: shareable link, embed code, remix allowed
Limits:   custom domain ledu, Anthropic infra dependent
```

## Option 2: Netlify (Fastest, 2 min)

```
1. Artifact -> Download -> index.html
2. netlify.com/drop -> drag the file
3. Instant live URL!

Custom domain optional. Free tier sufficient.
```

## Option 3: Vercel / GitHub Pages

```
React artifacts:
  Download .jsx -> Vite project lo integrate -> build -> deploy

Static HTML:
  GitHub: push to repo -> Settings -> Pages -> instant URL
```

## Option 4: Embed

```html
<iframe
  src="https://claude.ai/artifacts/[your-id]"
  width="100%"
  height="600"
  frameborder="0">
</iframe>
```

## Option 5: Internal (Teams/Enterprise)

```
Internal link -- only org members access
Claude Cowork lo live artifacts share
Admin controls external sharing
```

## Hosting Comparison

| Option | Cost | Setup | Custom Domain | Best For |
|---|---|---|---|---|
| Claude cloud | Free | Zero | No | Quick demos |
| Netlify | Free tier | 2 min | Yes | Public HTML |
| Vercel | Free tier | 2 min | Yes | React apps |
| GitHub Pages | Free | 5 min | Yes | Open source |
| Replit | Free tier | 1 min | Yes | Experiments |

---

# PART 5: Remix

```
Published artifact -> Remix button ->
  Copy of artifact meeru account lo create avutundi
  Meeru modify -> republish cheyyadam possible
  GitHub Fork concept artifact lo

Who can remix: Free, Pro, Max -- anyone public artifact ni

Use cases:
  "Expense tracker remix chesi Indian Rupee add chestanu"
  "Quiz template remix chesi Python questions add"
  "Dashboard template remix chesi our branding"
```

---

# PART 6: Storage API — Persistent Data

```
Default: artifact stateless -- reload aite data pothundi
Storage API tho: data persist cheyyachu

Use cases: todos save, game scores, user preferences
```

```javascript
const storage = window.claude?.storage;

// Save cheyyadam
await storage.setItem('todos', JSON.stringify(todos));

// Read cheyyadam
const saved = await storage.getItem('todos');
const todos = JSON.parse(saved || '[]');

// Delete cheyyadam
await storage.removeItem('todos');
```

> **WARNING:** Artifact unpublish chestunte storage **PERMANENTLY DELETED**.

---

# PART 7: Supported Libraries

## HTML — CDN via script tag

```html
<!-- Tailwind CSS -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- Chart.js -->
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<!-- D3.js -->
<script src="https://d3js.org/d3.v7.min.js"></script>

<!-- Alpine.js -->
<script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>

<!-- Bootstrap 5 -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5/dist/css/bootstrap.min.css" rel="stylesheet">
```

## React — Pre-loaded

```javascript
import { useState, useEffect, useRef } from "react";
import { BarChart, Bar, XAxis, YAxis, Tooltip } from "recharts";
import { PlusCircle, Trash2 } from "lucide-react";
// shadcn/ui, Tailwind -- no install needed
```

## Sandbox Limits

```
NOT allowed:
  fetch() to external URLs
  Node.js modules (fs, path)
  npm packages (CDN only)

Why? Security, isolation, reproducibility
```

---

# PART 8: Real-World Examples

## Sales Dashboard (HTML + Chart.js)

```
"Create an HTML artifact: sales dashboard with monthly revenue
 bar chart, pie chart for top products, KPI cards (total/orders/avg),
 dark theme, Tailwind + Chart.js, 12 months sample data"
```

## RAG Pipeline Diagram (Mermaid)

```
"Create Mermaid sequence diagram: RAG pipeline --
 PDF -> chunk -> embed -> vector store,
 then query -> embed -> similarity search -> LLM -> answer"

Output:
  sequenceDiagram
    User->>Embedder: Upload PDF
    Embedder->>VectorDB: Store embeddings
    User->>Embedder: Ask question
    Embedder->>VectorDB: Similarity search
    VectorDB-->>LLM: chunks + question
    LLM-->>User: Final answer
```

## React Expense Tracker

```
"Build a React artifact: expense tracker --
 add/delete expenses, category filter, monthly bar chart,
 Tailwind + shadcn styling, persist to localStorage"
```

## LangChain tho Artifact-quality HTML Generate

```python
from langchain_anthropic import ChatAnthropic
from langchain_core.messages import HumanMessage

llm = ChatAnthropic(model="claude-sonnet-5")

response = llm.invoke([HumanMessage(content="""
Create a complete self-contained HTML page: BMI calculator.
Features: height cm + weight kg inputs, calculate button,
color-coded result (green=normal, yellow=overweight, red=obese),
Tailwind CSS. Return ONLY the HTML code.
""")])

with open("bmi_calculator.html", "w") as f:
    f.write(response.content)

print("Open bmi_calculator.html in browser!")
```

---

# PART 9: Best Practices

## Prompt Tips

```
1. Specify type:   "Create an HTML artifact" / "Build a React artifact"
2. List features:  "Include: feature1, feature2, feature3"
3. Styling:        "Tailwind CSS" / "dark theme" / "Material Design"
4. Data:           "use sample data" / provide actual values
5. Behavior:       "responsive for mobile" / "smooth animations"
6. Constraints:    "single file" / "no external API calls"
```

## Iteration Pattern

```
Step 1: Broad  -- "Create basic expense tracker"
Step 2: Bugs   -- "Delete button doesn't work, fix it"
Step 3: Add    -- "Add category filter dropdown"
Step 4: Polish -- "More padding, rounded corners, shadows"
Step 5: Edge   -- "Show empty state if no data"
```

## Common Patterns

```
Calculator:  "HTML artifact: currency converter INR-USD-EUR with flags"
Game:        "HTML artifact: Wordle clone, 5-letter, 6 attempts"
Data viz:    "React artifact: dashboard for this JSON [...], charts"
Docs:        "Mermaid artifact: our microservices architecture"
Report:      "Markdown artifact: quarterly review template with KPIs"
```

---

# PART 10: Plans and Access

```
Free Plan:
  All 6 artifact types
  Live preview, download, publish, remix
  Limited daily generations
  Storage API limited

Pro ($20/mo):
  More generations, full Storage API, version history

Teams/Enterprise:
  Internal sharing (org-only links)
  Live artifacts in Cowork
  Admin controls, audit logs
  Private artifact marketplace
```

---

# PART 11: Quick Reference

```
TYPES:
  HTML     -> apps, games, dashboards        (interactive)
  React    -> stateful complex UIs           (most powerful)
  SVG      -> diagrams, illustrations        (optional interactive)
  Mermaid  -> technical diagrams             (static)
  Markdown -> documents, reports             (static)
  PDF      -> formal, printable              (static)

CREATE:
  "Create a [type] artifact: [description + features + styling]"
  Chat lo iterate cheyyadam

HOSTING:
  Claude cloud -> Publish -> instant URL (free, zero setup)
  Netlify      -> drag .html -> instant URL (2 min)
  Vercel       -> git push -> React apps
  GitHub Pages -> free static

SHARING:
  Public   -> Publish -> anyone (no account needed)
  Internal -> Teams/Enterprise only
  Embed    -> iframe in any website
  Remix    -> others fork + modify

LIBRARIES:
  HTML:  Tailwind, Chart.js, D3.js, Bootstrap, Alpine.js
  React: hooks, Recharts, shadcn/ui, Lucide, Tailwind

STORAGE:
  window.claude.storage -- setItem / getItem / removeItem
  Unpublish = DATA PERMANENTLY DELETED

SANDBOX LIMITS:
  No external fetch(), no npm, no Node.js modules

BEST PROMPT:
  "Create a [HTML/React] artifact:
   [feature 1], [feature 2], [feature 3],
   styled with Tailwind, [behavior], [data]"
```

---

---

# PART 12: Publishing Artifacts — Complete Deep Dive

> Publishing = artifact ni public ga internet lo accessible cheyyadam.
> Oka button click tho — meeru raasina HTML/React/SVG app world ki available avutundi.

---

## What Happens When You Publish?

```
Before Publish:
  Artifact only meeru Claude chat lo chudagalaru
  Share cheyyatam possible kadu
  Private, only your session lo

After Publish:
  Anthropic cloud lo host avutundi
  Unique public URL generate avutundi: claude.ai/artifacts/[unique-id]
  Anyone (even without Claude account) browser lo open cheyyachu
  Interact cheyyachu — buttons click, inputs type, everything works
  Share cheyyachu — WhatsApp, email, slack, anywhere
```

---

## How to Publish — Step by Step

```
Step 1: Artifact create cheyyadam (or open existing)
        Chat panel lo artifact right side lo kanipistundi

Step 2: Artifact panel top-right lo options button (three dots ...)
        OR direct "Publish" button click

Step 3: Publish dialog opens:
        +--------------------------------+
        |  Publish Artifact              |
        |                                |
        |  Visibility:                   |
        |    ( ) Public  — anyone        |
        |    ( ) Internal — org only*    |
        |                                |
        |  [ Publish ]  [ Cancel ]       |
        +--------------------------------+
        * Internal only for Teams/Enterprise

Step 4: "Publish" click cheyyadam

Step 5: URL copy cheyyadam + share options:
        +--------------------------------+
        |  Published!                    |
        |                                |
        |  URL: claude.ai/artifacts/xyz  |
        |  [Copy Link]  [Open]           |
        |                                |
        |  Embed code:                   |
        |  <iframe src="..."></iframe>   |
        |  [Copy Embed]                  |
        +--------------------------------+
```

---

## Public vs Internal Publishing

### Public (Free, Pro, Max, Teams, Enterprise)

```
Who can access: Anyone with the link — no Claude account needed
What they can do:
  Open the artifact in browser
  Interact with it fully (click, type, use)
  Remix it (create their own copy)
  Share the link further

What they CANNOT do:
  Edit the original (only meeru cheyyadam possible)
  See your chat conversation
  Access your account

Use cases:
  Demo to client — "Idi chudandi meeru build chesina tool"
  Share calculator with team
  Embed interactive chart on blog
  Prototype show to investor
  Public portfolio piece
```

### Internal (Teams/Enterprise only)

```
Who can access: Only logged-in members of your organization
What they can do:
  Open, interact, remix
  View within org context

What they CANNOT do:
  Share externally (link won't work outside org)

Use cases:
  Internal dashboard — only team can see
  Company-specific tool — sensitive data
  Draft report — internal review first
  Training material — org members only
```

---

## Published Artifact URL — Structure

```
Format: https://claude.ai/artifacts/[artifact-id]

Example: https://claude.ai/artifacts/art_01234567890abcdef

artifact-id:
  Unique, random string
  Permanent (doesn't change when you update)
  Tied to your account

URL characteristics:
  Short and shareable
  Works on mobile browsers
  No login required for public artifacts
  HTTPS always (secure)
```

---

## Embed Code — Website lo Add Cheyyadam

Publish chesaka embed code vastundi. Idi website lo artifact embed cheyyataniki:

```html
<!-- Basic embed -->
<iframe
  src="https://claude.ai/artifacts/[your-artifact-id]"
  width="100%"
  height="600"
  frameborder="0"
  allow="clipboard-write">
</iframe>
```

**Responsive embed (CSS tho):**
```html
<div style="position: relative; width: 100%; padding-bottom: 56.25%;">
  <iframe
    src="https://claude.ai/artifacts/[your-artifact-id]"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="clipboard-write">
  </iframe>
</div>
```

**Use cases for embed:**
```
Blog post lo interactive calculator embed
Portfolio site lo project demo embed
Documentation site lo live code example
Company website lo tool embed
Notion page lo artifact embed (Notion supports iframes)
```

---

## Updating a Published Artifact

```
Published artifact update cheyyadam:
  Chat lo continue — "Add a new feature" or "Fix this bug"
  Claude updates artifact
  SAME URL lo automatically update avutundi — no republish needed!

Version history:
  Artifact panel lo version arrows (< >) click
  Previous versions chudachu
  Specific version ki revert cheyyachu

Note:
  URL changes kaadu — same link share chesina people ki
  automatic ga new version vastundi
```

---

## Unpublish — Undo Cheyyadam

```
Artifact panel -> ... (options) -> Unpublish

After Unpublish:
  URL work cheyyadu (404 error)
  Storage data PERMANENTLY DELETED (recover cheyyatam impossible!)
  Re-publish chesthe — NEW URL vastundi (old link dead)

Before Unpublish checklist:
  [ ] Important data backup chesukunnara? (storage API data)
  [ ] Shared link anyone ki ippudu use avutundaa?
  [ ] Old URL ni new URL tho replace chesukunnara?

WARNING: Unpublish IRREVERSIBLE for storage data!
```

---

## Published Artifact — What Visitor Sees

```
Visitor experience (no Claude account):

1. Link open chestadu — browser lo directly artifact load avutundi
   (No login page, no Claude chat)

2. Full interactive experience:
   Buttons work, inputs accept text, charts animate
   Game playable, calculator usable, dashboard interactive

3. Remix option visible:
   "Remix" button — visitor click chesthe
   Claude.ai account kaavali (create cheyyadam free)
   Their own copy create avutundi

4. What they DON'T see:
   Your chat conversation
   Your account info
   Other artifacts
   The code (unless you include it in the UI)

5. Mobile experience:
   Works on mobile browsers
   Responsive design (if you made it responsive)
   Touch events work
```

---

## Sharing Published Artifact — Platforms

```
Direct link share:
  Copy URL -> WhatsApp, Telegram, Email, Slack, Teams
  Anyone clicks -> opens in browser

Social media:
  LinkedIn: "Built this calculator with Claude — [URL]"
  Twitter/X: "Try my interactive RAG diagram — [URL]"
  Reddit: Share in relevant tech subreddits

Developer platforms:
  GitHub: README.md lo link add cheyyadam
  Dev.to, Medium: Article lo embed or link
  Stack Overflow: Answer lo reference

Business:
  Email to client — "Demo ready: [URL]"
  Presentation lo QR code — link to URL
  Documentation site lo embed

Note: URL clicked avutundi — preview image generate avutundi
      (Twitter/LinkedIn lo nice preview vastundi)
```

---

## Publishing Permissions — Plan wise

```
Free Plan:
  Public publish: YES (unlimited)
  Internal publish: NO
  Remix: YES (can remix others)
  Storage in published: limited

Pro Plan ($20/mo):
  Public publish: YES (unlimited)
  Internal publish: NO (Teams needed)
  Remix: YES
  Storage in published: full

Teams Plan:
  Public publish: YES
  Internal publish: YES (org-only links)
  Remix: YES
  Admin can restrict publishing
  Live artifacts in Cowork: YES

Enterprise:
  All Teams features
  Private marketplace for artifacts
  Admin control: whitelist approved artifacts only
  Audit logs: who published what, when
  Custom domain for artifacts (some cases)
```

---

## Common Publishing Mistakes — Avoid These

```
Mistake 1: Sensitive data artifact lo publish cheyyadam
  Problem: Anyone can see the data
  Fix: Sensitive info remove chesaka publish
        Sample/anonymized data use cheyyadam

Mistake 2: Unpublish chesaka storage data lost
  Problem: Irreversible data loss
  Fix: Important data download cheyyadam first
        localStorage/export feature add cheyyadam

Mistake 3: URL share chesaka update chestunte visitors affected
  Actually NOT a mistake — URL same, updates automatic
  (This is a feature, not a bug!)

Mistake 4: Mobile responsive ga cheyyakunda publish cheyyadam
  Problem: Mobile users lo broken layout
  Fix: Artifact lo mobile test cheyyadam
        "Make it mobile responsive" prompt add cheyyadam

Mistake 5: No error handling published artifact lo
  Problem: Users see JavaScript errors
  Fix: try-catch add cheyyadam
        "Add proper error handling" prompt cheyyadam
```

---

## Publish Workflow — Recommended

```
Step 1: Create
  Prompt chesaka artifact create avutundi

Step 2: Test locally (in Claude panel)
  All features test cheyyadam
  Mobile view check (browser developer tools lo)
  Edge cases check (empty state, invalid input)

Step 3: Polish
  "Improve the UI polish"
  "Fix mobile layout"
  "Add loading states"

Step 4: Publish (Public or Internal)
  Publish button click
  URL copy chesukoddam

Step 5: Share
  Relevant people ki URL share cheyyadam
  Embed if needed

Step 6: Iterate based on feedback
  Chat lo continue with improvements
  URL auto-update avutundi — no republish
```

---

## Quick Reference — Publishing

```
PUBLISH:
  Artifact panel -> Publish -> Public/Internal -> URL get

UPDATE:
  Chat lo refine -> same URL auto-updates (no republish)

UNPUBLISH:
  Artifact panel -> ... -> Unpublish
  WARNING: Storage data permanently deleted!

URL FORMAT:
  https://claude.ai/artifacts/[unique-id]
  Permanent, HTTPS, shareable

EMBED:
  <iframe src="https://claude.ai/artifacts/[id]"
          width="100%" height="600" frameborder="0">

ACCESS:
  Public  -> anyone with link (no account needed)
  Internal -> org members only (Teams/Enterprise)

VISITOR CAN:
  Open, interact, remix
  Cannot: edit original, see your chat

PLANS:
  Free/Pro   -> Public publish
  Teams/Ent  -> Internal publish + admin controls
```
