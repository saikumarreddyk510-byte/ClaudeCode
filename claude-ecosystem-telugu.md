# Claude Ecosystem — Complete Guide (Telugu-English Mix)
ArtifactsLink-https://claude.ai/code/artifact/20dc656b-8aa8-4b71-b3c2-f7a55a822aa4
> **Idi enti?** — Ee document lo Claude ecosystem lo unna anni topics ni Telugu-English mix lo,
> step-by-step detailed ga explain chesam. Beginner nunchi advanced varaku — prathi concept clear avutundi.
> Image lo chupincha danni kuda ikkade detailed ga cover chesam.

---

## Architecture Diagram

```
[Anthropic Company]
       |
       | trains & serves
       v
[Claude Models: Haiku / Sonnet / Opus / Fable]
       |
  _____|_____________________________________
 |              |                           |
 v              v                           v
[Claude Chat]  [Claude Code]          [Claude Cowork]
(Brain)        (Engineer)             (Operator)
Conversation   Writes/reads code      Files, browser,
Q&A, Writing   Runs commands          tools, workflows
Responds text  Developer agent        Work agent
       |              |                    |
       |______________|____________________|
                      |
              [Skills & Plugins]
              [MCP Connectors]
                      |
              [External World]
         Databases, Slack, Drive, GitHub...
```

## Deep Architecture Notes

- **Step 1:** Claude models Anthropic train chestundi — Haiku (fast), Sonnet (balanced), Opus (powerful), Fable (hardest)
- **Step 2:** Aa models 3 different surfaces lo serve avutay — Chat (conversation), Code (agentic coding), Cowork (file + tool workflows)
- **Step 3:** Skills = reusable instruction modules; Plugins = department-level workflow bundles
- **Step 4:** MCP (Model Context Protocol) = Claude ni real databases, SaaS tools, external systems tho connect chese layer
- **Step 5:** Permission modes = Claude Code lo Claude emi touch cheyyagalado decide chese settings

---

# PART 1: Claude Ecosystem — 3 Layers (Image Explanation)

## Image lo Chupinchindi — Claude Ecosystem 3 Layers

Image lo Anthropic Claude ecosystem ni **3 layers** ga explain chesaru.
Prathi layer oka different role play chestundi — Brain, Engineer, Operator.

```
Claude Chat    Claude Code     Claude Cowork
(Brain)    -->  (Engineer)  -->  (Operator)

AI evolution toward action — simple chat nunchi full automation varaku
```

---

## Layer 1: Claude Chat — Brain (Conversational AI)

**Claude Chat ante enti?**

Claude.ai lo unna normal chat interface — meeru question adugutaru, Claude answer chestundi.
Idi most basic ga, most people daily use cheyye layer. "Prompt in, Answer out" simple flow.

**Image lo chupinchina features:**
- **Conversational AI** — back-and-forth conversation, oka turn lo answer chestundi
- **Q&A** — questions ki direct answers
- **Writing** — essays, emails, reports, code explanations raayadam
- **Brainstorming** — ideas generate cheyyadam, options suggest cheyyadam
- **Responds in text** — output always text (+ code, tables, lists)

**Flow — image lo:**

```
Prompt (in) --> [Claude Chat] --> Answer (out)
Meeru question type chestam --> Claude process chesi --> Text response istundi
```

**Real examples:**

```
"Python lo for loop explain cheyyandi"     --> Claude text lo explain chestundi
"Cover letter raayu"                       --> Draft ready ga istundi
"Ee code lo bug enti?"                     --> Bug explain + fix suggest chestundi
"Startup idea ki pros and cons cheppandi"  --> Brainstorm chestundi
```

**Available lo:**
- Claude.ai website (web browser) — free lo kuda work avutundi
- Claude desktop app (Windows/Mac)
- Claude mobile app (iOS/Android)
- Free plan lo basic access; Pro/Max/Teams lo full access

---

## Layer 2: Claude Code — Engineer (Developer Agent)

**Claude Code ante enti?**

Idi terminal (command line) lo run ayye agentic coding tool.
Normal chat kadu — Claude mana actual codebase lo **real changes** cheyyadam possible.
"Tab input, Build/Execute output" — idi image lo chupinchadu.

**Image lo chupinchina features:**
- **Writes code** — function raayadam, module create cheyyadam, entire feature implement cheyyadam
- **Reads code** — existing codebase understand chesi context lo work cheyyadam
- **Runs commands** — tests run cheyyadam, builds trigger cheyyadam, git operations cheyyadam
- **Builds apps** — complete applications scaffold cheyyadam end-to-end

**Developer agent ante enti?**

Claude ikkade just suggest cheyyadu — actual ga files edit chestundi, terminal lo commands run chestundi.
Idi **agentic** behavior — multi-step autonomous tasks.
Human approval optional ga set cheyyaocchu (permission modes tho).

**Flow:**

```
Meeru task cheppitam
     |
     v
Claude Code: codebase read chestundi
     |
     v
Plan chestundi (plan mode lo)
     |
     v
Files edit, code write, tests run
     |
     v
Result report chestundi
```

**Real examples:**

```bash
$ claude "Add authentication to this FastAPI app"
# Claude: existing files read, auth code raasi, tests run chesi report

$ claude "Fix failing tests"
# Claude: error analyze chesi, fix implement chesi, tests pass ayyintaka continue

$ claude --permission-mode plan "Refactor database layer"
# Claude: read-only plan chestundi, emi change cheyyali explain chestundi
```

**Enduku powerful:**

```
Normal developer: oka file open, code raasi, save, test run, error fix, repeat
Claude Code:      "Add feature X" -- Claude anni steps autonomous ga chestundi
Time saved:       Hours --> Minutes
```

---

## Layer 3: Claude Cowork — Operator (Work Agent)

**Claude Cowork ante enti?**

Claude.ai lo Cowork tab — idi full workflow automation workspace.
Claude ikkade real files read/write chestundi, browser use cheyyadam possible, external tools connect cheyyadam.
Image lo "Aa" connectors symbol tho show chesaru.

**Image lo chupinchina features:**
- **Access files** — Google Drive, local folders nunchi real files read/write
- **Use browser** — web pages browse, data scrape, forms fill
- **Connect tools** — Slack, Salesforce, GitHub, DocuSign — live integrations
- **Run workflows** — multi-step automated tasks end-to-end complete cheyyadam

**Work agent ante enti?**

Department-level automation. Sales team, Legal team, Finance team — each ki full workflow.
Chat tab lo snapshot attach cheyyadam, Cowork lo real files work cheyyadam.

**Real examples:**

```
/research-prospect "TechCorp"
--> Claude: web search, CRM data pull, call notes prepare, email draft — all automatic

/review-contract "vendor_agreement.pdf"
--> Claude: contract read, risky clauses flag, redline suggestions — complete review

/monthly-report
--> Claude: accounting data pull, trends calculate, charts create, report draft
```

---

## 3 Layers Summary — Brain, Engineer, Operator

```
Layer         | Role      | Where       | What it does          | Output
--------------+-----------+-------------+-----------------------+------------------
Claude Chat   | Brain     | claude.ai   | Conversation, Q&A     | Text responses
              |           | web/mobile  | Writing, Brainstorm   |
--------------+-----------+-------------+-----------------------+------------------
Claude Code   | Engineer  | Terminal    | Writes/reads code     | Real file changes
              |           | CLI         | Runs commands         | Working software
              |           |             | Builds apps           |
--------------+-----------+-------------+-----------------------+------------------
Claude Cowork | Operator  | claude.ai   | Files, browser        | Deliverables
              |           | Cowork tab  | Tools, workflows      | Documents, reports
```

**Image lo tagline:** "Brain --> Engineer --> Operator = AI evolution toward action"

Idi real insight — Claude sirf chat cheyyatledu, action taasukuntundi, work complete chestundi.

---

## Image lo Second Diagram — Why AI Assistants Are Becoming Essential

### Traditional Work vs AI-Assisted Work

**Image explain chestundi:** Before AI assistants, people anni pani cheyyadam manually chesevaru —
time waste, boring, solo work. AI vastha same work minutes lo complete avutundi.

**Before AI Assistants — Traditional Work (image left side):**

```
Oka person anni chestadu (sad face, overloaded):
  - Emails write cheyyadam (manual)
  - Documents create cheyyadam (manual)
  - Research cheyyadam (manual)
  - Planning cheyyadam (manual)

Result:
  "Takes hours" -- time expensive
  "Doing everything alone" -- single person ki overload
  Repetitive, boring, slow
```

**AI Assistant ela work chestundi (image center):**

```
AI Assistant 3 things chestundi:
  1. Understands requests   --> meeru emi adigaro understand chestundi (NLP)
  2. Processes information  --> relevant data gather, analyze chestundi
  3. Generates solutions    --> answer, document, code, plan ready chestundi

Simple flow:
  Question --> [AI Assistant] --> Solution
  Ask      --> Process        --> Output
```

**With AI Assistant — Working With AI (image right side):**

```
Same work, AI tho:
  - Automated help available aanika
  - Research: AI immediately finds, summarizes
  - Documents: AI drafts, meeru review
  - Emails: AI writes, meeru send
  - Planning: AI suggests, meeru approve

Result:
  "Minutes instead of hours" -- massive time saving
  Meeru strategy + creativity, AI handles repetitive
  Energy saved for high-value work
```

**Market lo unna AI Assistants (image lo list chesaru):**

| AI Tool | Company | Best At |
|---|---|---|
| **ChatGPT** | OpenAI | General purpose, most popular, plugins |
| **Gemini** | Google | Search integration, Google Workspace |
| **Claude** | Anthropic | Safety, long-context, coding, writing |
| **Deepseek** | High-Flyer (China) | Math, reasoning, cheap API |
| **Grok** | xAI (Elon Musk) | Real-time Twitter/X data |

**Claude ni unique ga chesedi:**

```
Other AI tools:  Chat cheyyochu, answer istay, text return
Claude Code:     Actual files touch chestundi, commands run chestundi
Claude Cowork:   Real files write, external tools connect, workflows automate

-- Idi oka level above simple chat assistants --
```

---

# PART 2: Claude Code Permission Modes — Detailed

## Permission Modes ante Enti?

**Permission mode** = Claude Code session lo oka important setting.
"Claude machine ni touch cheyyadaniki mundu, emi jarigipotundi?" ani answer chestundi.

**Enduku important?**

Claude Code cheyye work — files edit cheyyadam, shell commands run cheyyadam, git push cheyyadam.
Ivi anni irreversible (undo chesukotam hard). Mode decide chestundi — Claude auto chestuundaa, adigitonundaa.

**Simple analogy:**

```
Mode = key lo unna security gate

manual mode:      Gate daggara security guard — every car ki ID check
acceptEdits mode: Cars (edits) auto lo pass, trucks (commands) ID check
plan mode:        Gate closed, chudadam matrame ok, emi enter cheyyaraddu
auto mode:        Smart AI security — risk chusi decide
bypass mode:      Gate ledu — emi check cheyyadu (most dangerous)
dontAsk mode:     Pre-approved list only auto, others silently turn away
```

**Available modes (Claude Code v2.1.237):**

```bash
$ claude --help
  --permission-mode <mode>
    choices: "acceptEdits", "auto", "bypassPermissions",
             "manual", "dontAsk", "plan"
```

---

## Mode 1: manual — Default, Safest

**Manual mode ante enti?**

Prathi tool call ki — file edit, shell command, URL fetch — Claude meeru ki ask chestundi.
Meeru "y" chepaaka matrame proceed avutundi. Idi default mode — most people ki yidi best.

**Built-in description:**
> "default — asks before making edits or running commands"

**Ela pani chestundi:**

```
Claude: "functions.py lo 15 lines add cheyyalani undi. Ok aa?"
Meeru:  y (yes) press cheyyam
Claude: edit chestundi

Next action:
Claude: "npm test run cheyyalani undi. Ok aa?"
Meeru:  y or n
```

**Enduku use cheyyali:**

```
Production systems tho pani chestunapudu
Databases, infrastructure changes chestunapudu
Irreversible operations: delete, deploy, migrate
Unfamiliar codebase — emi chestundaa telusu koadanu
Risk high ga feel aite
```

**Best practice:**

```bash
git add -A
git commit -m "checkpoint before claude session"
claude                    # tarvata work start cheyyadam
```

Undo option kaavali — git commit chesaka Claude ki pass cheyyadam safe.

---

## Mode 2: acceptEdits — File Edits Auto-Approve

**acceptEdits mode ante enti?**

File edits (write, create, modify) ki auto-approve avutundi — ask cheyyadu.
Shell commands ki maatramu still ask chestundi.

**Built-in description:**
> "auto-accepts file edits; still asks before running shell commands"

**Ela pani chestundi:**

```
File write   --> Auto approve (ask cheyyadu) -- fast!
File edit    --> Auto approve
Shell command (npm test, git push, pip install) --> Still asks
```

**Enduku use cheyyali:**

```
Feature development lo — bohot files edit avutay, prathi ki ask boring
Committed repo lo — git undo option undi
Shell commands ki control kavalante — file edits ok aithe
Large refactoring — 50 files change chestunapudu manual boring avutundi
```

**Analogy:**

```
Manual mode:       Oka oka brick pettakamudu permission
acceptEdits mode:  Bricks auto pettukuntam, cement (commands) ki permission
```

---

## Mode 3: plan — Read-Only, Safe Exploration

**plan mode ante enti?**

Claude read-only mode lo work chestundi.
File write, commands run — blocked. Chudadam, thinking matrame ok.

**Built-in description:**
> "read-only mode — claude can read files and think through problems but cannot make changes"

**Ela pani chestundi:**

```
File read   --> OK (cat, grep, ls work avutay)
File write  --> BLOCKED
Shell commands --> Read-only only (ls, cat — ok; npm install, git push — blocked)
API calls   --> Blocked (external state change possible)
```

**Enduku use cheyyali:**

```
New codebase explore cheyyadaniki — emi break cheyyadam ledu
Task begin cheyyadaniki mundu — approach plan cheyyadaniki
"Idi ela work avutundo?" ani understand cheyyadaniki
Code review, architecture understanding
Interview lo "explain this codebase" type questions
```

**Recommended workflow:**

```
Step 1: plan mode lo Claude start cheyyadam
        "ee authentication module ela work avutundi?"
        Claude: chusi, explain chestundi, plan chestundi

Step 2: Meeru plan approve chestam
        "Yes, proceed with approach 2"

Step 3: acceptEdits mode switch cheyyadam (Shift+Tab)
        Claude: actual implementation chestundi
```

---

## Mode 4: auto — AI Decides

**auto mode ante enti?**

Claude ki oka built-in AI classifier undi — each action "safe" a "risky" a classify chestundi.
Safe aithe auto chestundi, risky aithe meeru ki ask chestundi.

**Built-in description:**
> "claude's judgment on when to ask for permission based on risk assessment"

**Ela pani chestundi:**

```
Action --> AI classifier analyze chestundi
       --> Safe ga teelintundi   --> Auto approve, chestundi
       --> Risky ga teelintundi  --> User ki ask chestundi

Examples:
Safe (auto):  unit tests run, doc strings add, README update, local file edit
Risky (ask):  database delete, external API call, git push, npm publish
```

**Enduku use cheyyali:**

```
Long autonomous runs — Claude hours work chestundi, hourly check intolerance
Mixed tasks — mostly safe, occasional risky steps
Productivity + safety balance kavalante
Background jobs while meeru inka work chestunnapudu
```

**Risk — prompt injection:**

```
Untrusted content process chestunte (external repos, user data, web pages)
--> Malicious content "delete all files" trigger cheyyaocchu
--> auto mode lo careful ga use cheyyadam
--> Trusted codebases lo only recommended
```

---

## Mode 5: bypassPermissions — Never Asks

**bypassPermissions mode ante enti?**

Claude emi ask cheyyadu. Anni tool calls auto-approve. Most risky mode.
Production lo never use cheyyaraddu.

**Built-in description:**
> "skips all permission checks — CAUTION: claude will make changes without asking"

**Ela pani chestundi:**

```
File write   --> Auto (no ask)
Shell cmd    --> Auto (no ask)
Database ops --> Auto (no ask)
Git push     --> Auto (no ask)
Delete files --> Auto (no ask)
```

**ONLY use chesedi:**

```
1. Throwaway VM / disposable container
   -- Docker container, cloud sandbox, emi break ainaaa restart cheyyadam easy
   -- Production kadu

2. Isolated test environment
   -- Real data ledu, real consequences ledu

3. Meeru deliberately enable chestunapudu — every session
   -- Settings lo default set cheyyadam impossible (intentional design)
```

**Enable cheyyadam:**

```bash
claude --dangerously-skip-permissions
# OR
claude --allow-dangerously-skip-permissions
```

**Why impossible to set as default?**

Anthropic intentionally made this — every session lo consciously choose cheyyali.
"I want bypass today" ana awareness kaavali. Accidental permanent bypass prevent.

---

## Mode 6: dontAsk — Allowlist Only, Headless Mode

**dontAsk mode ante enti?**

Specific allowlisted operations auto-approve avutay.
Allowlist lo lekapothe silently skip — error cheyyadu, ask cheyyadu — just skip.

**Built-in description:**
> "never asks for permission, but skips operations that aren't in the allowlist"

**Ela pani chestundi:**

```
Allowlisted operation  --> Auto approve, chestundi
Non-allowlisted        --> Silently skip (no error, no ask, no output)
```

**Enduku use cheyyali:**

```
CI/CD pipelines:  GitHub Actions lo claude run cheyyataniki
Scheduled jobs:   Cron lo nightly analysis
Scripted mode:    claude -p "task" --output-format json
Headless runs:    Human available ledu, non-interactive mode
```

**Real CI/CD example:**

```yaml
# GitHub Actions workflow
- name: Claude code review
  run: |
    claude --permission-mode dontAsk \
           -p "Review this PR for bugs" \
           --output-format json > review.json
```

---

## Modes Switch — 3 Ways

**Way 1: Shift+Tab (mid-session cycle)**

```
default --> acceptEdits --> plan --> bypassPermissions --> auto --> default
(loop continues)

Note:
- bypassPermissions: only if enabled at launch
- auto: only if opted-in
- dontAsk: cycle lo ledu, back to default avutundi
```

**Way 2: Launch time lo**

```bash
claude --permission-mode plan
claude --permission-mode acceptEdits
claude --permission-mode dontAsk
claude --dangerously-skip-permissions     # bypassPermissions
```

**Way 3: Settings.json lo (persistent)**

```json
{
  "permissions": {
    "defaultMode": "acceptEdits"
  }
}
```

Note: bypassPermissions + auto — settings lo set cheyyaraddu. Always session lo deliberately choose cheyyali.

---

## Permission Modes Quick Reference

| Mode | File Edits | Shell Commands | Risk | Use When |
|---|---|---|---|---|
| **manual** | Ask every time | Ask every time | Lowest | Production, irreversible ops |
| **acceptEdits** | Auto-approved | Ask every time | Low | Normal feature dev, committed repo |
| **plan** | BLOCKED | Read-only only | Zero | New codebase, planning phase |
| **auto** | AI decides | AI decides | Medium | Long autonomous trusted runs |
| **bypassPermissions** | Never asks | Never asks | HIGHEST | Throwaway VM only |
| **dontAsk** | Allowlist only | Allowlist only | Low (silent skips) | CI/CD, scripted |

---

## Permission Rules — Fine-grained Control

Mode tho batunga, specific rules set cheyyadam possible:

```bash
/permissions                          # current rules chudadam
/permissions allow read ~/myproject   # specific path allow
/permissions deny bash                # bash completely block
/permissions allow bash npm           # only npm commands allow
```

**Rules > Mode:**

```
Rule "deny bash" unte, auto mode lo kuda bash run cheyyadu.
Rules more specific, mode more general.
```

---

## Section 8: Modes vs Permission Rules — Fine-grained Control

**Modes** = coarse dial (broad setting).
**Permission rules** = fine dial (specific tool-level control).
Rendu kalipi use chesthe — maximum control.

```
Mode    -- session-level broad gate
Rules   -- tool/path-level specific gate
```

**settings.json lo rules define cheyyadam:**

```json
{
  "permissions": {
    "allow": ["Bash(git status)", "Bash(npm test:*)", "Edit"],
    "ask":   ["Bash(git push:*)"],
    "deny":  ["Read(./.env)", "Bash(curl:*)"]
  }
}
```

**Rules explain:**

```
allow: ["Bash(git status)", "Edit"]
  --> git status, file edits -- always auto-approve, never ask
  --> "Yes, don't ask again" cheppinaapudu Claude idi write chestundi

ask: ["Bash(git push:*)"]
  --> git push * pattern -- always ask, even in auto mode

deny: ["Read(./.env)", "Bash(curl:*)"]
  --> .env file read, curl commands -- ALWAYS blocked
  --> Every mode lo kuda -- bypassPermissions lo kuda deny wins
```

**Key rules to remember:**

```
1. deny wins everywhere
   deny set chesthe -- acceptEdits lo, auto lo, anni modes lo blocked
   Secrets, production access ki deny rules mandatory

2. allow = "Yes, don't ask again" shortcut
   Common safe commands ki allow pettadam -- manual mode livable chestundi
   Prathi time ask boring avvadam avoid

3. dontAsk mode lo -- allowlist = capability list
   Allow chesindi matrame run avutundi
   Allow cheyyaledu = silently skip (error kadu, ask kadu)

4. bypassPermissions lo -- allow/ask moot, kaani deny still works
   Modes switch chestunte deny rules survive
```

**Practical example — manual mode + rules combination:**

```json
{
  "permissions": {
    "defaultMode": "manual",
    "allow": [
      "Read",
      "Bash(git status)",
      "Bash(git diff:*)",
      "Bash(npm test:*)",
      "Bash(python -m pytest:*)"
    ],
    "deny": [
      "Read(./.env)",
      "Read(./.env.*)",
      "Bash(git push:*)",
      "Bash(rm -rf:*)"
    ]
  }
}
```

**Result:**

```
File reads        -- auto (ask cheyyadu -- readonly safe)
git status/diff   -- auto (safe commands)
npm test, pytest  -- auto (local only, safe)
.env files        -- BLOCKED always (secrets protect)
git push          -- BLOCKED always (manual review needed)
rm -rf            -- BLOCKED always (dangerous)
Everything else   -- ask (manual mode ki match)
```

**Enduku idi important?**

```
Without rules: manual mode lo every single action ki ask -- boring
With rules:    Safe actions auto, dangerous ones blocked or asked
               Best of both worlds
```

---

## Section 9: Which Mode Should I Use? — Decision Guide

**Situation based mode selection — Which one should I use?**

| Situation | Mode | Enduku? |
|---|---|---|
| Unfamiliar codebase, big vague task | `plan` first, then `acceptEdits` | First understand, tarvata implement |
| Normal feature work, committed repo | `acceptEdits` | git undo undi, file edits ok |
| Production, migrations, irreversible | `manual` (default) | Every step verify cheyyali |
| Long autonomous run, trusted code | `auto` | Claude decide chestundi, mostly ok |
| Disposable VM / Docker container | `bypassPermissions` | Worst case = restart container |
| CI/CD, cron, scheduled agents | `dontAsk` | Nobody prompt answer cheyyatam ledu |

---

**Recommended workflow — real projects lo:**

```
Step 1: plan mode start cheyyadam
        "ee feature ela implement cheyyali?"
        Claude: codebase read, plan chestundi
        Nothing break avvadam ledu -- safe exploration

Step 2: Plan approve chestam
        "Yes, approach 2 use cheyyi"

Step 3: acceptEdits mode switch (Shift+Tab)
        Claude: actual implementation chestundi
        File edits auto, commands still ask
        40 prompts ledu -- fast development

Step 4: Risky operation vastunapudu
        Shift+Tab -- back to manual
        git push, database migration, production deploy
        Each step carefully verify
```

---

**3 Golden Rules — internalize cheyyadam:**

**Rule 1: Commit before mode loosen cheyyadam (Commit before you loosen the mode)**

```
Every mode above manual assumes meeru undo option undi.
acceptEdits, auto, bypass -- anni assume git history exists.

Habit:
  git add -A && git commit -m "checkpoint"
  claude --permission-mode acceptEdits
```

**Rule 2: Mode is per session, not per repo**

```
Existing session ki attach chestunapudu -- mode changes ignored.
"--permission-mode is ignored when attaching"

Example:
  claude --permission-mode plan    # new session -- works
  # same session ki attach chestunte -- existing mode remains
```

**Rule 3: Mode to blast radius match cheyyandi, impatience kadu**

```
Question is NEVER: "Do I trust Claude?"
Question IS:       "What can this session reach if something goes wrong?"

Session reaches production DB   --> manual mode
Session reaches only test files --> acceptEdits ok
Session in throwaway Docker     --> bypass ok
Session in CI/CD pipeline       --> dontAsk

Risk = scope of potential damage
Mode = gate proportional to that risk
```

---

**Common mistakes — avoid cheyyadam:**

```
Mistake 1: bypassPermissions personal machine lo use cheyyadam
  Risk: Claude malicious content execute cheyyocchu
  Fix:  VM/container lo only

Mistake 2: dontAsk lo allowlist check cheyyadam
  Risk: Job "success" chesindi kaani half work silently skipped
  Fix:  Transcript always read cheyyadam, just exit code kadu

Mistake 3: plan mode tarvata directly bypass jump cheyyadam
  Risk: No review, no undo checkpoint
  Fix:  plan --> review --> commit --> acceptEdits --> commit --> risky ops

Mistake 4: Production lo acceptEdits use cheyyadam
  Risk: File edits auto, dangerous changes slip through
  Fix:  Production lo always manual
```

---

# PART 3: Claude Models — Complete Details

## Model Tiers — 3 Levels

Anthropic Claude models **3 main tiers** lo design chesaru:

```
Speed/Cost    <---------------------------------------------> Capability/Price
 Haiku 4.5          Sonnet 5              Opus 5             Fable 5
 (fastest,          (balanced,            (most capable,      (hardest,
  cheapest)          recommended)          agentic)            rare)
```

**Analogy:**

```
Haiku  = Bike  -- cheap, fast, short distance, daily commute
Sonnet = Car   -- daily driver, most situations handle
Opus   = Plane -- long-haul complex journeys, expensive kaani worth it
Fable  = Rocket -- extreme edge cases, cost no object
```

---

## Current Models — August 2026

| Model | Context | Max Output | Input $/M | Output $/M | Knowledge | Best For |
|---|---|---|---|---|---|---|
| **Haiku 4.5** | 200K | 64K | $1.00 | $5.00 | Feb 2025 | Fast, cheap, volume |
| **Sonnet 5** | 1M | 128K | $2.00 | $10.00 | Jan 2026 | Most apps, default |
| **Opus 5** | 1M | 128K | $5.00 | $25.00 | May 2026 | Complex, agentic |
| **Fable 5** | 1M | 128K | $10.00 | $50.00 | Jan 2026 | Absolute hardest |

**1M tokens ante enti?**

```
1 million tokens =~ 800,000 English words
             =~ oka entire library of books one context window lo
             =~ mana entire Python codebase (thousands of files) one conversation lo
```

---

## Claude Haiku 4.5 — Speed Champion

**Enduku Haiku choose cheyyali?**

- Fastest model — low latency, takkuva time
- Cheapest — $1 input / $5 output per million tokens
- High-volume apps ki perfect — thousands of users same time handle

**Best use cases:**

```
Chatbots:       Real-time responses, 200ms lo answer
Search apps:    Query rewriting, result summarization
Tagging:        Document classification, entity extraction
Pipelines:      RAG lo retrieval step, preprocessing light tasks
Simple Q&A:     FAQ bots, customer support first layer
```

**Limitations:**

```
Complex multi-step reasoning   -- Sonnet/Opus kante weak
Very long analysis             -- 200K window smaller, Sonnet 5x bigger
Deepest creative writing       -- Opus kante takkuva quality
```

---

## Claude Sonnet 5 — Default Workhorse

**Enduku Sonnet?**

Anthropic itself officially recommend chestundi: "default to Sonnet 5 for new applications."
Speed + intelligence perfect balance. Most production apps ki sufficient.

**Best use cases:**

```
Coding:        Code generation, review, debugging, refactoring
RAG:           Document Q&A, knowledge base, search
Writing:       Reports, emails, content creation, summaries
Analysis:      Contract review, data interpretation, research
Agentic:       Multi-step tool use, workflow automation
LangChain:     Most chain types, agents, RAG pipelines
```

**Adaptive thinking feature:**

```
Hard problem vastuundi --> Sonnet automatically more compute use chestundi
Simple problem         --> Less compute, faster response
Auto-adjusts — meeru manually configure cheyyalanakkarledu
```

**Context window — 1M tokens:**

```
Entire Python repository  -- anni files oka conversation lo
Long legal documents      -- complete contracts, all clauses
Historical conversation   -- hours of chat history maintain
Multi-document analysis   -- 10+ documents simultaneously
```

---

## Claude Opus 5 — The Powerhouse

**Enduku Opus?**

Highest reasoning capability. Most current knowledge (May 2026). Claude Code heavy tasks ki default.
Sonnet 5 insufficient aite — Opus ki upgrade.

**Best use cases:**

```
Research:       Scientific analysis, deep literature review
Complex coding: Architecture design, hard algorithmic problems
Long-context:   Entire codebase analysis, 1M token documents
Agentic tasks:  Many tool calls, long autonomous runs, multi-day projects
Reasoning:      Math, logic, philosophical analysis
When Sonnet fails: Fallback to Opus for better results
```

**Cost consideration:**

```
Opus 5:   $5/$25 per 1M tokens
Sonnet 5: $2/$10 per 1M tokens
--> Opus 2.5x more expensive
--> Meaningful capability difference ainapudu matrame use cheyyadam
--> Rule: Sonnet 5 tho try, result takkuva aithe Opus upgrade
```

---

## API Cost Optimization

### Prompt Caching — 90% Savings

Same system prompt, same documents repeated ga send chestunte — cache cheyyadam:

```
Without caching:
  System prompt (10K tokens) * 100 API calls
  = 1M input tokens * $2/M = $2.00

With caching:
  First call:    Cache write = 10K * $2.50/M = $0.025
  Calls 2-100:   Cache hit   = 990K * $0.20/M = $0.198
  Total: $0.223  --> 89% savings!
```

**Python code:**

```python
response = client.messages.create(
    model="claude-sonnet-5",
    messages=[...],
    system=[{
        "type": "text",
        "text": "Long system prompt here...",
        "cache_control": {"type": "ephemeral"}  # cache this prefix
    }]
)
```

### Batch API — 50% Off

Real-time response avasaram lēni bulk jobs ki:

```
Normal API  --> Immediate response, normal price
Batch API   --> Jobs queue lo, 24hr window, 50% cheaper

Use cases:
  Nightly data processing
  Large-scale document classification
  Offline report generation
```

| Model | Normal Input | Batch Input | Normal Output | Batch Output |
|---|---|---|---|---|
| Haiku 4.5 | $1.00/M | $0.50/M | $5.00/M | $2.50/M |
| Sonnet 5 | $2.00/M | $1.00/M | $10.00/M | $5.00/M |
| Opus 5 | $5.00/M | $2.50/M | $25.00/M | $12.50/M |

---

# PART 4: Claude.ai Plans

## Plan Overview

```
Free       --> Basic usage, try cheyyadaniki, casual users ki
Pro        --> $20/mo, 5x usage, all models, daily professionals ki
Max        --> $100+/mo, 20x usage, heavy power users ki
Teams      --> Multiple people, admin controls, small businesses ki
Enterprise --> Large org, SSO, HIPAA, compliance, regulated industries ki
```

---

## Free Plan

**Idi enduku?** Claude try cheyyadaniki — student, curious person, occasional user.

```
Features:
  Basic Claude access (Sonnet model)
  Daily usage limit (takkuva messages)
  Web app only
  Basic Projects
  Web search (limited)

Limitations:
  Peak hours lo slow / unavailable
  Opus model access ledu
  Skills / Cowork features limited or unavailable
  Usage cap hit avutundi daily
```

---

## Pro Plan — $20/month

**Idi enduku?** Daily Claude use chese developer, writer, analyst ki. Most individuals ki sufficient.

```
Features:
  5x more usage than Free
  All models access: Haiku, Sonnet, Opus
  Priority access (peak hours lo slow avvadu)
  Unlimited Projects
  Web search (full)
  Memory across chats
  Skills (+ menu — reusable task modules)
  Desktop + Mobile apps (full features)
  Claude tools: Code, Cowork, Design, Science
```

**Worth ita?**

```
$20/mo = oka OTT subscription cost
Daily work lo Claude use chestunte = hours save avutundi
Time value > $20 by far for most professionals
```

---

## Claude Max — From $100/month

**Idi enduku?** Pro plan lo usage limit hit avutundi anipistunnaru? Max ki upgrade.

```
Options:
  Max 5x:   $100/mo  -- 5x more than Pro
  Max 20x:  $200/mo  -- 20x more than Pro

Features:
  Everything in Pro
  Much higher usage limits
  Early access to new features before general release
  Maximum output limits (longer responses possible)

Best for:
  Heavy daily power users
  Developers doing intensive prototyping
  Researchers processing large text volumes
```

---

## Teams Plan

**Idi enduku?** 2+ people organizations ki — central billing, shared workspace.

```
Features:
  Everything in Pro
  Central admin billing (one invoice)
  Organization-level Projects (shared across team)
  Member usage analytics (who uses how much)
  Connectors: Slack, Google Workspace integration
  Cowork tab (team collaboration full features)
  Admin controls: who uses what, what models

Best for:
  Startups (5-50 people)
  Product teams, engineering teams
  Marketing, content, sales teams
```

---

## Enterprise Plan

**Idi enduku?** Large organizations, regulated industries ki.

```
Security:
  SSO (Single Sign-On) — SAML/OIDC (employees company login tho access)
  SCIM — automated user provisioning/deprovisioning (AD sync)
  Audit logs — every action track, compliance requirement
  HIPAA compliance — healthcare data safe ga handle
  Data retention controls — data ela long undi, delete policies

Scale:
  Custom context window per org
  Usage commitments (predictable monthly cost)
  Dedicated support + SLA guarantees (uptime promises)

Deployment:
  Private marketplace (org-specific plugins only)
  Custom model behavior (org-wide system prompts)
  On-premises or private cloud options (some cases)
  Sales-assisted setup

Best for:
  Banks, hospitals, law firms, government
  1000+ employee organizations
  Regulated data handling required
  Custom security + compliance requirements
```

---

# PART 5: Anthropic API — Developer Access

## API ante enti?

Anthropic API = Claude models ni programmatically call cheyyadam.
Claude.ai UI kadu — mana own applications lo Claude integrate cheyyadam.

**Real use cases:**

```
Product build: Customer ki Claude-powered chatbot embed cheyyadam
LangChain:     LLM ga Claude use, chains, agents, RAG
Automation:    Nightly document processing pipeline
Custom app:    Code review tool, writing assistant, data analyzer
```

**Quick start:**

```bash
pip install anthropic
export ANTHROPIC_API_KEY="sk-ant-..."
```

---

## Basic Python Usage

```python
import anthropic

client = anthropic.Anthropic()  # ANTHROPIC_API_KEY env lo auto reads

response = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=1024,
    messages=[
        {"role": "user", "content": "Python lo fibonacci raayu"}
    ]
)
print(response.content[0].text)
```

---

## System Prompt — Claude ki Permanent Instructions

```python
response = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=2048,
    system="Meeru Telugu-English mix lo explain cheyye Python tutor vi.",
    messages=[
        {"role": "user", "content": "Decorators ante enti?"}
    ]
)
```

**System prompt uses:**

```
Claude ki role assign cheyyadam       -- "You are a Python tutor"
Specific format follow cheyyadam      -- "Always use bullet points"
Domain restrict cheyyadam             -- "Only answer coding questions"
Language style set cheyyadam          -- "Telugu-English mix lo explain"
Company context provide cheyyadam     -- "You work for TechCorp support"
```

---

## Streaming — Real-time Token Output

```python
with client.messages.stream(
    model="claude-sonnet-5",
    max_tokens=1024,
    messages=[{"role": "user", "content": "Long explanation raayu"}]
) as stream:
    for text in stream.text_stream:
        print(text, end="", flush=True)  # token by token print
```

**Enduku streaming?**

```
Normal mode: Claude full response ready ayyaka one shot pamputundi
             User 30 seconds wait cheyali -- bad UX

Stream mode: Token by token vastuundi (typing effect)
             User immediately reading start cheyyadam
             Claude.ai chat UI ila work avutundi
```

---

## Tool Use — Claude calling Your Functions

```python
tools = [
    {
        "name": "get_weather",
        "description": "City ki current weather data return chestundi",
        "input_schema": {
            "type": "object",
            "properties": {
                "city": {"type": "string", "description": "City name"}
            },
            "required": ["city"]
        }
    }
]

response = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=1024,
    tools=tools,
    messages=[{"role": "user", "content": "Hyderabad lo weather ela undi?"}]
)
# stop_reason == "tool_use" aithe Claude tool call cheyyadam anukuntundi
# Meeru actual weather API call chesi result back pamputam
# Claude final natural language answer istundi
```

**Flow:**

```
User: "Hyderabad weather?"
         |
         v
Claude: "get_weather tool call cheyyali" (stop, tool_use)
         |
         v
Our code: weather API call chestundi
         |
         v
Claude: "Hyderabad lo 35 degrees, clear sky" (final answer)
```

---

## Vision — Image Analysis

```python
import base64

with open("screenshot.png", "rb") as f:
    image_data = base64.b64encode(f.read()).decode()

response = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=1024,
    messages=[{
        "role": "user",
        "content": [
            {
                "type": "image",
                "source": {
                    "type": "base64",
                    "media_type": "image/png",
                    "data": image_data
                }
            },
            {"type": "text", "text": "Ee screenshot lo enti chupistundi? Bug unnaa?"}
        ]
    }]
)
```

**Use cases:**

```
Chart analysis:        Sales chart trends explain cheyyadam
Screenshot debugging:  UI bug lo enti wrong unnado identify
Document OCR:          Scanned documents text extract
Architecture diagrams: System design explain cheyyadam
```

---

# PART 6: Skills & Plugins — Detailed

## Skills ante enti?

**Simple ga:** Skill = oka `.md` file — Claude ki specific task ela cheyalo detailed instructions.
Same instructions prathi conversation lo repeat cheyyalanakkarledu.

**Problem Skills solve chestunnayi:**

```
Without skill:
  Meeru: "Quarterly report raayu. Ila format cheyyi. Company template use cheyyi.
           Executive summary cheyyi. Financial overview add cheyyi. Action items list
           cheyyi. Professional tone lo. 2 pages max. Data lo numbers bold cheyyi.
           Charts include cheyyi..."
  (Every single conversation lo idi repeat cheyyadam boring, time waste)

With skill:
  Meeru: "Q3 report prepare cheyyi"
  Claude: [quarterly-report skill auto-detect + load] --> everything automatic
```

---

## SKILL.md File Format

```markdown
---
name: python-code-review
description: Review Python code files for bugs, PEP-8 style, performance, and security issues.
---

# Instructions
1. Syntax errors and runtime bugs check cheyyadam
2. PEP-8 style compliance verify cheyyadam (naming, spacing, line length)
3. Performance bottlenecks identify cheyyadam (O(n^2) loops, unnecessary operations)
4. Security vulnerabilities flag cheyyadam (injection, hardcoded secrets)
5. Output format: Bug list --> Style suggestions --> Performance --> Security
6. Severity levels use cheyyadam: Critical / High / Medium / Low
```

**3 parts:**

```
--- metadata block ---
name:        Skill identifier (short, kebab-case)
description: Claude idi chusi trigger chestundi — CLEAR + SPECIFIC ga raayadam important

# Instructions
Step-by-step what Claude should do
```

**Good description raayadam crucial:**

```
BAD:  "Code review"
      -- too vague, wrong tasks trigger avvocchu

GOOD: "Review Python code files for bugs, PEP-8 style, performance bottlenecks, and security"
      -- specific, Claude correctly trigger avutundi

BAD:  "Reports"
      -- ambiguous

GOOD: "Create quarterly business reports with executive summary, financial overview, and action items"
      -- clear scope
```

---

## Skill Folder Structure

```
quarterly-report/
    SKILL.md               <-- Required (instructions + metadata)
    QBR_Template.docx      <-- Optional (reference template file)
    calculate_metrics.py   <-- Optional (executable script Claude can run)
    sample_output.md       <-- Optional (example output for Claude to reference)
    README.md              <-- Optional (human notes about the skill)
```

---

## Skill Auto-trigger Flow

```
Meeru: "Idi Python code review cheyyi"
              |
              v
Claude: Installed skills lo "description" compare chestundi
              |
              v
Match found?
    YES --> Skill SKILL.md load chestundi
            Instructions + scripts apply
            Task execute chestundi
            |
    NO  --> Normal conversation continues (no skill active)
```

---

## Skill Install — 3 Ways

```
Way 1: Marketplace (easiest)
  claude.com/skills --> Browse --> One click install
  Thousands of community + official skills available
  Categories: coding, writing, analysis, legal, finance...

Way 2: GitHub
  git clone <skill-repo>
  Move folder to Claude skills directory
  Claude auto-discovers

Way 3: Build your own (most flexible)
  mkdir my-code-reviewer
  Create SKILL.md with your instructions
  Claude interface --> + --> Skills --> Upload folder
```

---

## Skill Access in Interface

```
Chat lo + button click
    |
    v
Skills option select
    |
    v
Installed skills list vastuundi
    |
    +--> Specific skill manually select cheyyadam
    +--> Just task type chesthe auto-detect + load
```

---

## Plugins (Cowork Tab) — Department-level Automation

**Plugin vs Skill — key difference:**

```
Skill  = Oka recipe card
         "Write quarterly reports this specific way"
         Single task, one SKILL.md

Plugin = Full restaurant kitchen
         Sales dept: research + CRM + emails + reports + all automated
         Multiple skills + live connectors + slash commands + sub-agents
```

**Plugin lo unna components:**

```
Skills:           Task-specific instruction modules
Connectors:       Live SaaS integrations (Google Drive, Slack, Salesforce...)
Slash commands:   /draft-email, /research-prospect, /analyze-data
Sub-agents:       Specialized mini-AI for specific steps
Configuration:    Permissions, API keys, data access rules
```

---

## Plugin Examples by Department

```
Sales Plugin:
  /research-prospect "Microsoft" --> web search + CRM pull + competitive intel
  /prep-call-notes               --> talking points, known objections, company history
  /send-followup                 --> personalized email draft + send

Legal Plugin:
  /review-contract "vendor.pdf"  --> clause analysis, risk flags, redline suggestions
  /check-compliance              --> regulatory requirements verify
  /draft-nda                     --> standard NDA with custom terms

Finance Plugin:
  /monthly-report                --> accounting data + trends + charts + draft
  /expense-analysis              --> categories, anomalies, cost reduction opportunities
  /budget-variance               --> planned vs actual comparison

HR Plugin:
  /screen-resume "candidate.pdf" --> skills match, experience score, red flags
  /draft-jd "Senior Python Dev"  --> job description with requirements
  /onboarding-doc                --> new hire checklist, first week plan
```

---

## MCP (Model Context Protocol) — Connector Layer

**MCP ante enti?**

Claude ni real external systems tho connect cheyye **universal protocol**.
Custom integration code raayanakkarledu — MCP server install chesthe Claude automatically use chestundi.

```
Claude <--> MCP Server <--> PostgreSQL DB     (real queries)
       <--> MCP Server <--> GitHub            (PRs, issues)
       <--> MCP Server <--> Notion            (pages, databases)
       <--> MCP Server <--> Slack             (messages)
       <--> MCP Server <--> Custom API        (anything)
```

**Claude Code lo MCP setup (.mcp.json):**

```json
{
  "mcpServers": {
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres"],
      "env": {
        "POSTGRES_URL": "postgresql://localhost/mydb"
      }
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_TOKEN": "ghp_..."
      }
    }
  }
}
```

**Tarvata:**

```
$ claude "Show me all users who signed up last week"
Claude: postgres MCP use chesi actual query run chestundi, results istundi
```

---

# PART 7: Architecture Diagrams — Explained in Telugu-English

## 10,000-Foot View

```
                        +---------------------------------------------+
                        |              A N T H R O P I C              |
                        |    Safety-first AI company, San Francisco    |
                        |    Mission: Responsible AI development       |
                        +--------------------+------------------------+
                                             |
                                             | trains & deploys
                                             v
                        +---------------------------------------------+
                        |           C L A U D E   M O D E L S         |
                        |                                              |
                        |  Haiku 4.5   Sonnet 5   Opus 5   Fable 5   |
                        |  (fast/cheap) (balanced) (complex) (hardest)|
                        +--------------------+------------------------+
                                             |
              +------------------------------+-----------------------------+
              |                              |                            |
              v                              v                            v
   +------------------+         +-----------------+         +------------------+
   [   Claude.ai      ]         [  Anthropic API  ]         [   Claude Code    ]
   [ Consumer product ]         [ Developer API   ]         [ Agentic Coding   ]
   [ Chat + Cowork    ]         [ REST + SDKs     ]         [ Terminal CLI     ]
   [ Free/Pro/Teams   ]         [ Pay-per-token   ]         [ File/Shell/MCP   ]
   +------------------+         +-----------------+         +------------------+
```

**Explanation:**

```
Anthropic:
  Mana behind scenes lo models train chestuundi
  Safety research chestundi (Constitutional AI)
  API, Claude.ai, Claude Code service chestundi

Claude Models:
  Haiku   = fast, cheap, high-volume ki
  Sonnet  = balanced, most apps ki default
  Opus    = complex reasoning, agentic tasks ki
  Fable   = rarest, absolute hardest ki

3 Access Points:
  Claude.ai  = regular users, chat, cowork (UI lo)
  API        = developers, product builders (code lo)
  Claude Code = developers, agentic coding (terminal lo)
```

---

## Constitutional AI Training — Explained

```
Phase 1: Pre-training
  Millions of books, articles, code, web pages lo train chestaru
  --> Claude language, knowledge, reasoning learn chestundi

Phase 2: Supervised Fine-tuning (SFT)
  Humans "helpful response" examples raaschesaru
  --> Claude helpfulness learn chestundi

Phase 3: Constitutional AI (CAI) -- Anthropic's unique innovation

  +-- Constitution (100+ principles) define chesaru --+
  |                                                    |
  | "Be honest"                                        |
  | "Don't deceive users"                              |
  | "Avoid harm"                                       |
  | "Respect human autonomy"                           |
  | ... (100+ rules)                                   |
  +----------------------------------------------------+

  RLHF: Human raters responses rank chesaru
    +
  RLAIF: Claude itself own responses evaluate chestuundi
         Constitution ki against chesimdaa check
         Self-critique loop -- scalable, cost-effective

Final Result:
  Helpful   -- genuinely useful, not sycophantic
  Harmless  -- dangerous requests refuse
  Honest    -- uncertainty acknowledge, no hallucination hide
```

**Why CAI important?**

```
Traditional RLHF: Humans rank every response -- expensive, slow, human bias
CAI (RLAIF):      Claude itself evaluate -- scalable, consistent, cost-effective

Result:
  Jailbreaks ki resistant -- strong principles baked in
  Nuanced refusals -- "I can't help with X because Y" explanation
  Uncertainty acknowledge -- "I'm not sure, verify this"
```

---

## LangChain + Claude Integration

```python
from langchain_anthropic import ChatAnthropic
from langchain_core.messages import HumanMessage, SystemMessage

# LLM initialize
llm = ChatAnthropic(
    model="claude-sonnet-5",
    temperature=0,       # 0 = deterministic, consistent outputs
    max_tokens=2048,
)

# Multi-turn conversation
messages = [
    SystemMessage(content="You are a Telugu-English Python tutor. Explain concepts clearly."),
    HumanMessage(content="Lambda functions ante enti?"),
]
response = llm.invoke(messages)
print(response.content)
```

**LangChain tho Claude powerful cheyye things:**

```
Chains:    Multiple steps sequence lo — retrieve, process, generate
RAG:       Documents tho ground chesukoni answer
Agents:    Tools use cheyyadam (web search, calculator, database)
Memory:    Conversation history maintain
LangGraph: Complex stateful multi-node agents
```

---

# PART 8: Claude vs Other AI Assistants

## Comparison

| | Claude | ChatGPT | Gemini | Deepseek | Grok |
|---|---|---|---|---|---|
| Company | Anthropic | OpenAI | Google | High-Flyer | xAI |
| Context | 1M tokens | 128K | 1M | 128K | 131K |
| Safety | Constitutional AI | RLHF | RLHF + Google | RLHF | Limited |
| Coding | Excellent | Excellent | Good | Excellent | Good |
| Long docs | Best (1M) | Limited | Good | Limited | Limited |
| Agentic | Claude Code | Limited | No | No | No |
| API cost | $1-50/M | $0.15-60/M | Varies | $0.14-2.19/M | Varies |

**Claude unique advantages:**

```
1. Longest context: 1M tokens -- entire codebase one conversation lo
2. Claude Code: Actual agentic coding -- real files, real commands
3. Constitutional AI: Safest, most nuanced responses
4. Instruction following: Very precise, complex instructions follow
5. Writing quality: Natural, nuanced, less robotic than GPT
6. Honesty: Uncertainty clearly acknowledge chestundi
```

---

# PART 9: Model Selection — Quick Guide

## Decision Tree

```
Task undi. Enduku model?
        |
        v
Simple, fast, high-volume, latency-critical?
    YES --> Haiku 4.5  ($1/$5 per M)
    NO  --> Sonnet 5 try cheyyadam

Sonnet 5 result insufficient? Complex reasoning required?
    NO  --> Stick with Sonnet 5  ($2/$10 per M)
    YES --> Opus 5  ($5/$25 per M)

Opus 5 kuda insufficient? Cost no object?
    YES --> Fable 5  ($10/$50 per M)
```

## Practical Examples

```
Task                               --> Choose
-----------------------------------+-----------
FAQ chatbot (1000 users/day)        --> Haiku 4.5
Document classification pipeline   --> Haiku 4.5
Code generation (feature work)      --> Sonnet 5
RAG Q&A system                     --> Sonnet 5
Contract review                    --> Sonnet 5
LangChain agent default            --> Sonnet 5
Complex architecture design        --> Opus 5
Full codebase analysis (>500K)     --> Opus 5
Claude Code heavy tasks            --> Opus 5 (auto default)
Scientific research paper analysis --> Opus 5
```

---

# PART 10: Quick Reference

## Model IDs

```python
# API lo use cheyye model names -- August 2026
"claude-haiku-4-5"    # fast, cheap
"claude-sonnet-5"     # default, balanced
"claude-opus-5"       # powerful
"claude-fable-5"      # most powerful, rare
```

## Pricing

```
Per 1 Million tokens:
  Haiku 4.5:  $1.00 in  / $5.00 out
  Sonnet 5:   $2.00 in  / $10.00 out
  Opus 5:     $5.00 in  / $25.00 out
  Fable 5:    $10.00 in / $50.00 out

Batch API (50% off):
  Haiku 4.5:  $0.50 / $2.50
  Sonnet 5:   $1.00 / $5.00
  Opus 5:     $2.50 / $12.50

Cache hits (10% of input price):
  Haiku 4.5:  $0.10/M
  Sonnet 5:   $0.20/M
  Opus 5:     $0.50/M
```

## Claude.ai Plans

```
Free:       Basic, limited usage, try cheyyadaniki
Pro:        $20/mo -- 5x usage, all models, daily professionals ki
Max:        $100+/mo -- 20x usage, heavy power users ki
Teams:      Pro + admin + org workspace + connectors
Enterprise: Teams + SSO + SCIM + HIPAA + SLA + private deploy
```

## Claude Code Commands

```bash
claude                                 # interactive session
claude "fix the login bug"             # one-shot task
claude --permission-mode plan          # read-only planning
claude --permission-mode acceptEdits   # file edits auto-approve
claude --dangerously-skip-permissions  # bypass all (CAUTION: VM only)
claude -p "task" --output-format json  # headless/CI mode
```

## Permission Mode Summary

```
manual:           Prathi action ki ask -- safest
acceptEdits:      File edits auto, commands ask -- daily dev
plan:             Read-only -- new codebase explore
auto:             AI decide chestundi -- long runs
bypassPermissions:Never asks -- VM only, DANGEROUS
dontAsk:          Allowlist only -- CI/CD, automation
```

## Which Surface Use Cheyyali?

```
Conversation, Q&A, writing          --> Claude.ai Chat
Repetitive task automation          --> Claude.ai Skills (+ menu)
Department workflows, files, SaaS   --> Claude.ai Cowork + Plugins
Build product on Claude             --> Anthropic API
AI agent pipelines, RAG             --> API + LangChain/LangGraph
Actual codebase editing             --> Claude Code (terminal)
Database / internal tools           --> MCP servers
Large org, regulated industry       --> Claude Enterprise
```

---

> **Last updated:** August 2026
> **Verified:** Anthropic docs, platform.claude.com, Claude Code CLI v2.1.237
> **Style:** Telugu-English mix — prathi concept detailed ga, examples tho explain chesam
> **Note:** Pricing verify cheyyadaniki: platform.claude.com/docs/en/about-claude/pricing

---

---

# PART 11: Claude Reasoning Modes & Speed vs Intelligence (Image Explanation)

> Image source: platform.claude.com/docs/en/about-claude/models/overview

---

## Image lo Chupinchindi — 3 Diagrams

Image lo 3 separate diagrams unnay:

```
Diagram 1 (Left):   Claude Reasoning Modes — "Speed vs Deep Thinking"
                    Normal Mode vs Extended Thinking Mode ela differ avutundoo

Diagram 2 (Center): Claude Models — Speed vs Intelligence
                    Haiku / Sonnet / Opus / Extended Thinking — model choose cheyyadam

Diagram 3 (Right):  Claude Models — Choosing the right model for the task
                    Prathi model ki detailed capabilities + use cases + selection rule

Bottom:             Tokens/Text — Input → Output (basic concept)
```

---

## Diagram 1: Claude Reasoning Modes — Speed vs Deep Thinking

**Image lo tagline:** "Speed vs Deep Thinking"
**Core message:** More thinking → better answers for complex problems, kaani time ekkuva

### Normal Mode — Standard Response (Fast)

```
Flow:
Prompt
  |
  v
Quick Prediction  (Claude immediately respond chestundi)
  |
  v
Answer

Result: "Fast responses"
```

**Normal mode ante enti?**

Meeru question adugutamu → Claude immediately answer istundi.
Idi default behavior — prathi regular conversation lo ila jarigipotundi.

```
Strengths:
  Speed       — fast, low latency
  Simple Q&A  — straightforward questions ki perfect
  Conversational — back-and-forth chat ki

Best for:
  "Python lo list sort ela cheyyali?"   — immediate answer
  "Capital of India?"                   — instant recall
  "Email draft cheyyi"                  — quick generation
  Daily chat, FAQ, simple tasks
```

### Extended Mode — Extended Thinking (Deep Reasoning)

```
Flow:
Prompt
  |
  v
Reasoning Steps   <--- Claude internally "thinks" chestundi
  |                    (meeru kanipiyyadam ledu — internal scratchpad)
  v
Evaluation        <--- Reasoning validate chestundi, better approach check
  |
  v
Answer

Result: "Deeper reasoning"
```

**Extended Thinking ante enti?**

Claude answer iccheyyadaniki mundu **longer reasoning chestundi** — step by step.
Idi "chain of thought" reasoning — hard problems ki accurate answers.

```
Strengths:
  Deep reasoning    — complex math, logic, multi-step problems
  Self-evaluation   — own thinking validate chestundi
  Better accuracy   — hard problems lo less hallucination
  Nuanced analysis  — ambiguous situations handle well

Slower kaani smarter:
  Normal mode:   50ms-2s response
  Extended mode: 5-30s response (reasoning time)
  Trade-off: Speed vs Accuracy
```

### Speed ↔ Reasoning Depth Trade-off

```
Image lo arrow:
Speed <-----------------------> Reasoning Depth

Normal Mode    |                         | Extended Mode
(Fast)         |                         | (Deep thinking)
               |                         |
Quick answer   |     Middle ground       | Thorough answer
Less accurate  |     (Sonnet default)    | More accurate
for hard tasks |                         | for hard tasks
```

**Image lo bottom tagline:**
```
Question → Claude Thinking → Final Answer
"More thinking improves complex problem solving"
```

---

## Diagram 2: Claude Models — Speed vs Intelligence

**Full axis:**
```
Fast ←─────────────────────────────────────────→ Deep Reasoning
Haiku          Sonnet (default)          Opus
```

### Haiku — Fast, Simple, Cheap

```
Image lo description:
  Fast
  Simple tasks
  Low cost
  Quick answers

Idi enduku choose cheyyali:
  High-volume requests (thousands per day)
  Real-time responses required
  Simple, straightforward tasks
  Cost optimization important

Quick rule (image lo): "Haiku = quick tasks"
```

### Sonnet — Balanced, Everyday Work

```
Image lo description:
  Balanced
  Everyday work
  Default model

Idi enduku choose cheyyali:
  Most day-to-day work
  Coding, writing, analysis, research
  Good speed + good quality balance
  99% of use cases ki sufficient

Quick rule (image lo): "Sonnet = most work"
Image tagline: "Default model"
```

### Opus — Powerful, Complex, Advanced

```
Image lo description:
  Powerful
  Complex tasks
  Deep reasoning
  Advanced problems

Idi enduku choose cheyyali:
  Complex reasoning required
  Long, intricate analysis
  Scientific research, architecture decisions
  When Sonnet insufficient

Quick rule (image lo): "Opus = complex problems"
```

### Extended Thinking — Optional Layer

```
Image lo description:
  "Think longer before answering"
  complex problems
  debugging
  analysis
  "Slower → smarter answers"
```

**Extended Thinking = separate feature (model kadu)**

Idi Haiku/Sonnet/Opus tho alongside use cheyyochu (API lo enable cheyyadam possible).
Model ni enable cheyyadam kadu — reasoning depth increase cheyyadam.

```
Without Extended Thinking:  Quick prediction → Answer
With Extended Thinking:     Reason → Evaluate → Refine → Answer
```

### Complete Flow (Image lo)

```
User Prompt
    |
    v
Claude Model (Haiku / Sonnet / Opus choose)
    |
    v
(Optional) Extended Thinking
    |
    v
Clear Answer

"Match the model to the problem."
```

---

## Diagram 3: Detailed Model Capabilities — Right Side

### Claude Haiku — Speed Focused Model

```
Image lo:
  Fastest response time
  Optimized for simple tasks
  Low cost / high efficiency
  Great for real-time workloads

Example use cases:
  quick answers
  summarization
  chat assistants
  automation at scale

Image tagline:
  "Speed focused model"
  "Designed for high-volume tasks where speed matters most"
```

**Telugu explanation:**

Haiku = production lo high-volume deployments ki backbone model.
Prathi user request ki fast response kaavali, thousands of parallel requests handle cheyyali,
cost kuda control lo unchali — aapudu Haiku perfect.

```
Real examples:
  Customer support chatbot     — 10,000 conversations/day handle
  Document auto-tagging        — 1 lakh docs classify cheyyadam
  Real-time autocomplete       — typing lo suggestions
  API rate limiting layer      — quick classification before expensive model
```

---

### Claude Sonnet — Most Efficient Everyday Model

```
Image lo:
  Balanced intelligence and speed
  Strong reasoning ability
  Handles longer context well
  Best for everyday work

Example use cases:
  research
  writing
  analysis
  coding

Image tagline:
  "Most efficient everyday model"
  "Default model cost-to-use Claude users"
```

**Telugu explanation:**

Sonnet = 90% of use cases ki go-to model.
Speed too slow kaadu, intelligence too low kaadu — perfect balance.
Anthropic itself "default to Sonnet" ani recommend chestundi.

```
Real examples:
  Coding assistant          — feature implement, bug fix
  RAG Q&A system            — document questions
  Contract review           — clause analyze, risks flag
  Email/report writing      — professional drafts
  LangChain agent           — most agentic workflows
```

---

### Claude Opus — Frontier Reasoning Model

```
Image lo:
  Most capable Claude model
  Strong reasoning and language
  Strong coding and analysis
  Best for complex problems

Example use cases:
  strategy planning
  complex data analysis
  AI agents

Image tagline:
  "Frontier reasoning model"
  "Designed for difficult tasks and ambitious work"
```

**Telugu explanation:**

Opus = Claude family lo most powerful. Cost ekkuva, kaani hardest problems solve chestundi.
Claude Code lo heavy tasks ki default ga Opus 5 use avutundi.

```
Real examples:
  Strategic business analysis   — market research, competitive analysis
  Complex multi-step coding     — architecture redesign, performance optimization
  Long-horizon AI agents        — days of autonomous work
  Scientific research           — data analysis, hypothesis generation
  When Sonnet result insufficient — final fallback
```

---

### Extended Thinking Mode — Deep Analysis Layer

```
Image lo:
  "Claude spends more time reasoning before answering"

Benefits:
  deeper reasoning
  multi-step problem solving
  complex planning
  detailed analysis

Example:
  debugging code
  designing systems
  research analysis

Image tagline: "Slower but more thoughtful answers"
```

**Telugu explanation:**

Extended Thinking = Claude ki "think out loud" option.
Normal lo Claude immediately answer istundi. Extended lo Claude internally reason chestundi,
steps evaluate chestundi, tarvata final answer istundi.

```
When to enable Extended Thinking:
  Math problems with multiple steps
  Code architecture decisions
  Ambiguous situations with nuance
  Research questions requiring synthesis
  Any time "fast answer" is wrong answer

API lo enable cheyyadam:
  model.create(..., thinking={"type": "enabled", "budget_tokens": 10000})
```

---

### Model Selection Rule (Image lo)

```
Image lo clear rule:
  Simple tasks      → Haiku
  Most work         → Sonnet
  Complex reasoning → Opus
```

**Detailed version:**

```
Task type                        | Choose     | Reason
---------------------------------+------------+---------------------------
FAQ chatbot, quick Q&A           | Haiku      | Speed + cost
Summarization, classification    | Haiku      | Volume + efficiency
Coding (feature work)            | Sonnet     | Balance
Writing, research, analysis      | Sonnet     | Quality + speed
RAG, document Q&A                | Sonnet     | Context handling
Architecture decisions           | Opus       | Deep reasoning
Complex debugging                | Opus       | Multi-step analysis
Long autonomous agent runs       | Opus       | Sustained reasoning
Strategy, research analysis      | Opus       | Nuanced judgment
Any of the above, hard problems  | + Extended | More thorough answers
```

---

### How Claude Processes Tasks (Image — Right Bottom)

```
Image lo flow:
User Prompt
    |
    v (Designed to understand and show question complexity)
Claude Model
    |
    v
Extended Thinking (optional)
    |
    v (Choose the model based on task complexity)
Structured Output

Simple ga:
  Input → Claude brain → (optional deeper thinking) → Output
```

---

## Bottom of Image: Tokens/Text — Input → Output

```
Image lo:
  Tokens / Text
  Input ──────────────────────────────→ Output
```

**Token ante enti?**

```
Claude text ni "tokens" ga process chestundi — characters/words chunks.

Examples:
  "Hello"                = ~1 token
  "Hello world"          = ~2 tokens
  "import numpy as np"   = ~4 tokens
  1 English word         =~ 1.3 tokens average
  1000 words             =~ 1300 tokens

Pricing token based:
  Input tokens  = meeru send chesindi (prompt + context)
  Output tokens = Claude generate chesindi (response)
  Output tokens are more expensive than input tokens
```

**Input → Output flow:**

```
Input side (what you send):
  System prompt    ─┐
  Chat history     ─┤─→ ALL counted as INPUT tokens → meeru pay
  Documents        ─┤    ($2/M for Sonnet 5)
  User message     ─┘

Output side (what Claude returns):
  Response text    ─→ OUTPUT tokens → meeru pay
                       ($10/M for Sonnet 5 — 5x more than input)

Optimization tip:
  Short, clear prompts  → takkuva input tokens → cost takkuva
  Concise responses     → takkuva output tokens → cost takkuva
  Caching               → repeated prefix 90% cheaper
```

---

## Summary — Image lo 3 Diagrams oka Saari

```
Diagram 1: Reasoning Modes
  Normal Mode    = Prompt → Quick Answer (fast, default)
  Extended Mode  = Prompt → Think → Evaluate → Better Answer (slower, deeper)
  Trade-off: Speed ↔ Reasoning Depth

Diagram 2: Model Selection Spectrum
  Fast ──── Haiku ──── Sonnet ──── Opus ──── Deep Reasoning
  Optional Extended Thinking any model tho add cheyyochu

Diagram 3: Detailed Capabilities
  Haiku  = Speed focused, high-volume, cheap
  Sonnet = Balanced, everyday default, most efficient
  Opus   = Frontier reasoning, complex tasks, ambitious work
  Extended Thinking = Deeper answers, debugging, research
  Rule: Simple→Haiku, Most→Sonnet, Complex→Opus

Bottom: Tokens
  Input tokens + Output tokens = what you pay for
  Output costs more than input
```

---

# PART 12: Normal Mode vs Extended Thinking — Code Examples

## Normal Mode vs Extended Thinking — Difference Enti?

```
Normal Mode:
  Prompt → Claude → Answer
  Fast, default, most tasks ki sufficient

Extended Thinking:
  Prompt → Claude internally reasons (hidden scratchpad) → Answer
  Slower, deeper, complex problems ki better
```

---

## Setup — Install & API Key

```python
# Install cheyyadam
# pip install anthropic

import anthropic

# Client create — ANTHROPIC_API_KEY env lo unte auto reads
client = anthropic.Anthropic(api_key="sk-ant-...")
```

---

## Normal Mode — Standard Response

```python
import anthropic

client = anthropic.Anthropic()

# Normal mode — default ga idi, extra settings avasaram ledu
response = client.messages.create(
    model="claude-sonnet-5",          # model choose
    max_tokens=1024,                  # max output tokens
    messages=[
        {
            "role": "user",
            "content": "27 * 48 calculate cheyyi, step by step cheppu"
        }
    ]
)

# Response print
print("=== Normal Mode Response ===")
print(response.content[0].text)
print(f"\nInput tokens:  {response.usage.input_tokens}")
print(f"Output tokens: {response.usage.output_tokens}")
print(f"Stop reason:   {response.stop_reason}")
```

**Output (normal mode):**
```
=== Normal Mode Response ===
27 * 48 calculate cheyyadam:

Step 1: 27 * 48 = 27 * (50 - 2)
Step 2: 27 * 50 = 1350
Step 3: 27 * 2  = 54
Step 4: 1350 - 54 = 1296

Answer: 1296

Input tokens:  28
Output tokens: 52
Stop reason:   end_turn
```

---

## Extended Thinking Mode — Deep Reasoning

```python
import anthropic

client = anthropic.Anthropic()

# Extended Thinking mode — thinking parameter add cheyyadam
response = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=16000,                 # extended thinking ki ekkuva tokens kaavali
    thinking={
        "type": "enabled",
        "budget_tokens": 10000        # reasoning ki max tokens allocate cheyyadam
        # budget_tokens = Claude reasoning ki use chesukone max tokens
        # ekkuva = deeper thinking, kaani cost ekkuva
    },
    messages=[
        {
            "role": "user",
            "content": "27 * 48 calculate cheyyi, step by step cheppu"
        }
    ]
)

print("=== Extended Thinking Mode Response ===")

# Response lo rendu parts untay: thinking block + text block
for block in response.content:
    if block.type == "thinking":
        # Claude's internal reasoning — meeru debug ki chudochu
        print("\n--- Claude's Internal Thinking ---")
        print(block.thinking)
        print("--- End of Thinking ---\n")
    elif block.type == "text":
        # Final answer
        print("--- Final Answer ---")
        print(block.text)

print(f"\nInput tokens:  {response.usage.input_tokens}")
print(f"Output tokens: {response.usage.output_tokens}")
```

**Output (extended thinking):**
```
=== Extended Thinking Mode Response ===

--- Claude's Internal Thinking ---
Let me work through 27 * 48 carefully.

I can break this down:
27 * 48 = 27 * (40 + 8)
       = (27 * 40) + (27 * 8)
       = 1080 + 216
       = 1296

Let me verify another way:
27 * 48 = (30 - 3) * 48
       = (30 * 48) - (3 * 48)
       = 1440 - 144
       = 1296

Both methods give 1296. Confirmed.
--- End of Thinking ---

--- Final Answer ---
27 × 48 = **1296**

Step-by-step:
1. 27 × 48 = 27 × (40 + 8)
2. 27 × 40 = 1080
3. 27 × 8  = 216
4. 1080 + 216 = **1296**

Input tokens:  28
Output tokens: 312
```

---

## Extended Thinking — Complex Problem Example

Simple math ki extended thinking overkill. Real difference complex problems lo kanipistundi:

```python
import anthropic

client = anthropic.Anthropic()

complex_problem = """
Oka company ki 3 products unnay: A, B, C.
- Product A: profit margin 30%, monthly sales 1000 units, price Rs.500
- Product B: profit margin 20%, monthly sales 3000 units, price Rs.200
- Product C: profit margin 40%, monthly sales 500 units, price Rs.800

Marketing budget Rs.50,000 undi. Ela allocate chestే total profit maximize avutundi?
Constraints: Prathi product ki minimum 20% budget ivvaali.
"""

# --- Normal Mode ---
normal_response = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=1024,
    messages=[{"role": "user", "content": complex_problem}]
)

print("=== NORMAL MODE ===")
print(normal_response.content[0].text[:500], "...")  # first 500 chars

# --- Extended Thinking Mode ---
extended_response = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=16000,
    thinking={
        "type": "enabled",
        "budget_tokens": 8000         # complex problem ki ekkuva budget
    },
    messages=[{"role": "user", "content": complex_problem}]
)

print("\n=== EXTENDED THINKING MODE ===")
for block in extended_response.content:
    if block.type == "thinking":
        print(f"[Internal reasoning: {len(block.thinking)} chars]")
    elif block.type == "text":
        print("Final Answer:")
        print(block.text)
```

---

## Streaming tho Extended Thinking

```python
import anthropic

client = anthropic.Anthropic()

# Extended thinking + streaming combination
with client.messages.stream(
    model="claude-sonnet-5",
    max_tokens=16000,
    thinking={
        "type": "enabled",
        "budget_tokens": 5000
    },
    messages=[
        {"role": "user", "content": "Quicksort algorithm implement cheyyi, time complexity explain cheyyi"}
    ]
) as stream:
    current_block_type = None

    for event in stream:
        # Block type change detect cheyyadam
        if hasattr(event, 'type'):
            if event.type == 'content_block_start':
                block = event.content_block
                if block.type == 'thinking':
                    print("\n[Claude thinking...]", end="", flush=True)
                    current_block_type = 'thinking'
                elif block.type == 'text':
                    print("\n[Answer]:", end="", flush=True)
                    current_block_type = 'text'

            elif event.type == 'content_block_delta':
                delta = event.delta
                if hasattr(delta, 'thinking'):
                    print(".", end="", flush=True)  # thinking progress dots
                elif hasattr(delta, 'text'):
                    print(delta.text, end="", flush=True)  # real-time answer
```

---

## budget_tokens — How to Choose

```python
# budget_tokens = Claude reasoning ki allocate chesina max tokens
# Ekkuva budget = deeper thinking, kaani:
#   1. Cost ekkuva (reasoning tokens kuda count avutay)
#   2. Time ekkuva (thinking cheyyadaniki time teesukuntundi)

# Recommended values:
budget_examples = {
    "simple_math":       1000,   # 27*48 type simple calculations
    "code_review":       5000,   # moderate complexity analysis
    "architecture":      8000,   # system design decisions
    "research_analysis": 10000,  # complex multi-faceted problems
    "maximum":           32000,  # absolutely hardest problems (claude-opus-5 ki)
}

# Example — problem complexity based budget:
def get_budget(problem_type):
    return budget_examples.get(problem_type, 5000)  # default 5000

response = client.messages.create(
    model="claude-opus-5",            # hard problems ki Opus
    max_tokens=20000,
    thinking={
        "type": "enabled",
        "budget_tokens": get_budget("architecture")  # 8000
    },
    messages=[{"role": "user", "content": "Design a distributed caching system..."}]
)
```

---

## Normal vs Extended — Comparison Table

```python
# Ye situation lo edi choose cheyyali? — code perspective

scenarios = {
    "FAQ chatbot":            ("normal", "claude-haiku-4-5",  "Fast, cheap, simple"),
    "Code generation":        ("normal", "claude-sonnet-5",   "Default, balanced"),
    "Complex bug fix":        ("extended","claude-sonnet-5",  "Reasoning helps"),
    "Math / logic problems":  ("extended","claude-sonnet-5",  "Step-by-step thinking"),
    "Architecture design":    ("extended","claude-opus-5",    "Deep analysis needed"),
    "Research synthesis":     ("extended","claude-opus-5",    "Multi-step reasoning"),
    "Simple summarization":   ("normal", "claude-haiku-4-5",  "No deep thinking needed"),
}

for task, (mode, model, reason) in scenarios.items():
    print(f"{task:<25} | {mode:<8} | {model:<20} | {reason}")
```

**Output:**
```
FAQ chatbot               | normal   | claude-haiku-4-5     | Fast, cheap, simple
Code generation           | normal   | claude-sonnet-5      | Default, balanced
Complex bug fix           | extended | claude-sonnet-5      | Reasoning helps
Math / logic problems     | extended | claude-sonnet-5      | Step-by-step thinking
Architecture design       | extended | claude-opus-5        | Deep analysis needed
Research synthesis        | extended | claude-opus-5        | Multi-step reasoning
Simple summarization      | normal   | claude-haiku-4-5     | No deep thinking needed
```

---

## Cost Comparison — Normal vs Extended

```python
# Extended thinking tokens kuda cost avutay — billing example

# Normal mode example:
# Input: 100 tokens * $2/M = $0.0002
# Output: 200 tokens * $10/M = $0.002
# Total: $0.0022 per call

# Extended thinking:
# Input: 100 tokens * $2/M = $0.0002
# Thinking: 5000 tokens * $2/M = $0.01    <-- reasoning tokens cost!
# Output: 300 tokens * $10/M = $0.003
# Total: $0.0132 per call (6x more expensive)

# Rule:
# Simple tasks  --> Normal mode (cheap)
# Complex tasks --> Extended thinking (worth the extra cost for accuracy)

# Rough cost estimate function:
def estimate_cost(
    input_tokens,
    output_tokens,
    thinking_tokens=0,
    model="sonnet"
):
    rates = {
        "haiku":  {"input": 1.0,  "output": 5.0},
        "sonnet": {"input": 2.0,  "output": 10.0},
        "opus":   {"input": 5.0,  "output": 25.0},
    }
    r = rates[model]
    input_cost    = input_tokens   * r["input"]  / 1_000_000
    output_cost   = output_tokens  * r["output"] / 1_000_000
    thinking_cost = thinking_tokens * r["input"] / 1_000_000  # thinking = input rate
    total = input_cost + output_cost + thinking_cost
    print(f"Input cost:    ${input_cost:.6f}")
    print(f"Thinking cost: ${thinking_cost:.6f}")
    print(f"Output cost:   ${output_cost:.6f}")
    print(f"Total:         ${total:.6f}")
    return total

print("Normal mode (sonnet):")
estimate_cost(input_tokens=100, output_tokens=200, model="sonnet")

print("\nExtended thinking (sonnet, 5000 budget):")
estimate_cost(input_tokens=100, output_tokens=300, thinking_tokens=5000, model="sonnet")
```

**Output:**
```
Normal mode (sonnet):
Input cost:    $0.000200
Thinking cost: $0.000000
Output cost:   $0.002000
Total:         $0.002200

Extended thinking (sonnet, 5000 budget):
Input cost:    $0.000200
Thinking cost: $0.010000
Output cost:   $0.003000
Total:         $0.013200
```

---

## Quick Reference — Extended Thinking API

```python
# Enable extended thinking
response = client.messages.create(
    model="claude-sonnet-5",     # or claude-opus-5
    max_tokens=16000,            # thinking + output tokens ki kaavali — ekkuva set cheyyadam
    thinking={
        "type": "enabled",       # enable cheyyadam
        "budget_tokens": 10000   # max reasoning tokens (1024 minimum)
    },
    messages=[...]
)

# Response lo blocks:
for block in response.content:
    if block.type == "thinking":
        # Claude's internal scratchpad — debug ki useful
        print(block.thinking)
    elif block.type == "text":
        # Final answer
        print(block.text)

# Disable extended thinking (normal mode):
response = client.messages.create(
    model="claude-sonnet-5",
    max_tokens=1024,
    # thinking parameter ledu = normal mode
    messages=[...]
)

# Rules:
# 1. max_tokens > budget_tokens + expected output tokens set cheyyaali
# 2. minimum budget_tokens = 1024
# 3. Extended thinking tho temperature = 1 only (forced by API)
# 4. Streaming supported — thinking blocks dots ga, answer real-time
# 5. Models: claude-sonnet-5, claude-opus-5 support extended thinking
#    claude-haiku-4-5 does NOT support extended thinking
```

---

---

# PART 13: Web Search vs Research Mode — Complete Guide

> Image lo chupinchindi: **"Same toggle bar — very different jobs"**
> Web Search = Fast (seconds) ←────────────────→ Research Mode = Deep (up to 45 min)
> Rendu kuda Claude.ai lo toggle chesi use cheyyochu — kaani completely different purposes

---

## Image lo Full Diagram — Explained

```
                Web Search vs Research Mode
           "Same toggle bar — very different jobs"

Fast — seconds ←─────────────────────────────────→ Deep — up to 45 minutes

┌─────────────────────────┐         ┌──────────────────────────────┐
│      Web Search         │   VS    │       Research Mode          │
│   (magnifier + bolt)    │ ←───→   │    (brain + document)        │
│                         │         │                              │
│ • Runs 1 quick search   │         │ • Writes its own plan        │
│ • Results 5-15 seconds  │         │ • Visits multiple websites   │
│ • Best for facts & news │         │ • Cross-references & synth   │
│ • Single answer + cites │         │ • Produces 1-2 page report   │
│ • Toggle OFF by default │         │ • Runs 2-45 min              │
│                         │         │                              │
│ "Quick fact. Right now."│         │ "Your analyst. Full brief."  │
└─────────────────────────┘         └──────────────────────────────┘

Flow:
[Question] → [Pick the Right Mode] → [Cited Output] → [Share or Act]
"Neither mode stays on — toggle before every new chat"

Use Which?
  Price of something      → Web Search
  Competitive landscape   → Research Mode
  Recent news             → Web Search
  Board-ready brief       → Research Mode
```

---

## 1. Web Search — "Quick Fact. Right Now."

**Web Search ante enti?**

Claude.ai lo real-time internet access. Oka question ki oka quick live search run chestundi — seconds lo answer vastundi.

**Image lo features:**

```
• Runs 1 quick live search      — oka search query run chestundi
• Results in 5–15 seconds       — fast response, low latency
• Best for current facts & news — real-time data kaavali ante idi
• Single answer, with citations — oka clean answer + source links
• Toggle OFF by default         — every new chat lo manually turn on cheyyali
```

**Enduku Web Search use cheyyali?**

```
Telugu: Quick, factual information kaavali ante

Examples:
  "Today's dollar to rupee exchange rate?"  → 5 seconds lo answer
  "Who won IPL 2025?"                       → recent news, quick fact
  "Python 3.13 release date?"               → specific fact
  "Current price of gold?"                  → real-time price
  "Latest Claude model release?"            → current news

Idi enduku fast avutundi:
  Oka search query run → top results read → answer synthesize → done
  Complex analysis kadu — just facts fetch cheyyadam
```

**When NOT to use Web Search:**

```
"Who are the top 5 AI companies and their strategy?" → Research Mode use cheyyandi
"Market analysis of EV industry?"                  → Research Mode use cheyyandi
Web Search = single quick lookup
             Complex multi-angle analysis kadu
```

---

## 2. Research Mode — "Your Analyst. Full Brief."

**Research Mode ante enti?**

Claude ki oka research analyst laga pani chestuundi. Meeru question ichi vellipotam — Claude plan raasi, multiple websites visit chesi, information cross-reference chesi, complete report prepare chestundi.

**Image lo features:**

```
• Writes its own research plan  — question based on plan create chestundi
• Visits multiple websites      — different sources check chestundi
• Cross-references and synth    — sources compare, contradict cheyyevaadi filter
• Produces 1-2 page cited report— structured, professional output
• Runs 2–45 min — use notifs   — background lo run avutundi, done aite notify
```

**How it works internally:**

```
Step 1: Meeru question type chestam
Step 2: Claude oka research plan raastundi:
          - "First, I'll look at X"
          - "Then compare with Y"
          - "Finally synthesize Z"
Step 3: Multiple searches run chestundi (5-20+ searches possible)
Step 4: Prathi source read, extract, note chestundi
Step 5: Information cross-reference chestundi (contradictions flag)
Step 6: 1-2 page structured report raastundi with citations
Step 7: Complete ayyaka notification vastundi
```

**Enduku Research Mode use cheyyali?**

```
Complex questions requiring deep analysis:

  "What is the competitive landscape of AI coding assistants in 2026?"
  → Web search: oka article istundi
  → Research: 10+ sources, compare ChatGPT/Claude/Copilot/Cursor,
              market share, features, pricing — full analyst report

  "Board-ready brief on generative AI adoption in banking?"
  → Research raasi, formatted, cited, professional

  "Compare LangChain vs LlamaIndex for RAG applications"
  → Multiple docs read, pros/cons, use cases, code examples synthesize

2–45 minutes:
  Simple research: 2-5 min
  Medium analysis: 10-20 min
  Deep investigation: 30-45 min
```

---

## 3. Key Differences Table

| Feature | Web Search | Research Mode |
|---|---|---|
| **Speed** | 5–15 seconds | 2–45 minutes |
| **Searches** | 1 quick search | Multiple (5-20+) |
| **Output** | Single answer + citation | 1-2 page cited report |
| **Best for** | Facts, prices, recent news | Analysis, strategy, reports |
| **Works in background** | No | Yes (use notifications) |
| **Toggle default** | OFF | OFF |
| **Analogy** | Google search | Research analyst |
| **Cost** | Included in Pro+ | Included in Pro+ |

---

## 4. Taglines — Deep Meaning

```
Web Search: "Quick fact. Right now."
  → Oka question, oka answer, oka source
  → Speed priority
  → "What is X?" type questions

Research Mode: "Your analyst. Full brief."
  → Multiple questions internally generate
  → Depth priority
  → "How does X compare to Y, what are implications, what should I do?" type
  → Boss ki present cheyyataniki brief ready avutundi
```

---

## 5. Toggle Behavior — Important Note

**Image lo:** "Neither mode stays on — toggle before every new chat"

```
Default state: Both OFF
  → Normal Claude conversation = no web access
  → Claude training data lo unna information only

Web Search turn on cheyyadam:
  New chat start chesaka toggle → Web Search ON
  Chat complete ayyaka → automatically OFF
  Next chat: again toggle cheyyali

Research Mode turn on cheyyadam:
  Same — prathi new chat lo toggle
  Background lo run avutundi — notifications enable cheyyandi

Enduku auto-stay off?
  Privacy: Web access = external calls
  Cost: Searches have limits (Pro plan lo monthly quota)
  Intentionality: User deliberately choose cheyyali
```

---

## 6. Flow — Question to Action

**Image lo flow:**

```
[Question]
    ↓
[Pick the Right Mode]   ← idi most important step!
    ↓
[Cited Output]          ← sources tho backed answer/report
    ↓
[Share or Act]          ← email cheyyadam, decision teesukoddam, presentation
```

**"Pick the Right Mode" decision:**

```
Question type                    | Mode
---------------------------------+------------------
Current fact/price/news          | Web Search
Single specific lookup           | Web Search
Multi-source deep analysis       | Research Mode
Competitive intelligence         | Research Mode
Academic/professional report     | Research Mode
Quick verification of claim      | Web Search
Strategy recommendation          | Research Mode
```

---

## 7. Use Which? — Image lo Examples

**Image lo exact examples:**

```
Price of something        → Web Search
  "Tesla stock price?"    → Web Search (real-time, single fact)

Competitive landscape     → Research Mode
  "Top AI startups in India and their funding?" → Research Mode

Recent news               → Web Search
  "What happened at Apple event yesterday?"  → Web Search

Board-ready brief         → Research Mode
  "Executive summary of cloud adoption trends for our Q4 deck?" → Research Mode
```

**More examples (Telugu context):**

```
Web Search use cases:
  "India vs Australia cricket score?"        → fast fact
  "Hyderabad property rate today?"           → current price
  "ChatGPT-5 release date?"                  → recent news
  "Python 3.15 new features?"                → specific lookup
  "Dollar to rupee rate right now?"          → real-time data

Research Mode use cases:
  "Comprehensive analysis of AI job market impact on IT sector in India?"
  "Compare all major RAG frameworks with pros, cons, use cases?"
  "Board brief: Should our company adopt AI coding assistants?"
  "Deep dive: LangChain vs AutoGen for enterprise agentic systems?"
  "Market research report on generative AI in healthcare?"
```

---

## 8. Pro Tips

```
Tip 1: Notifications enable cheyyandi
  Research Mode background lo run avutundi — 2-45 min
  Notification vasthe open cheyyandi — wait cheyyadam boring
  Browser notifications + desktop app lo especially useful

Tip 2: Web Search first, Research second
  Quick check: Web Search lo fast answer
  If need deep dive: Research Mode lo full analysis

Tip 3: Research Mode prompt clearly raayandi
  BAD:  "Tell me about AI"
  GOOD: "Provide a 2-page research report on the competitive landscape
         of AI coding assistants (GitHub Copilot, Cursor, Claude Code)
         comparing features, pricing, market share, and user reviews
         in 2026"

Tip 4: Prathi chat lo toggle cheyyandi
  Both modes off by default — forget kaaraleddi
  Browser extension or habit: chat open chesaka check toggle

Tip 5: Citations verify cheyyandi
  Both modes sources cite chestay
  Important decisions ki — source links click chesi verify cheyyandi
  AI hallucinate cheyyocchu — citations = accountability
```

---

## 9. AI lo Context — Why This Matters for Developers

```
Developer perspective:

Web Search:
  → Quick API lookup ("langchain latest version?")
  → Error message search ("numpy MemoryError fix?")
  → Recent library changes ("pandas 3.0 breaking changes?")

Research Mode:
  → Architecture decision ("Which vector DB should I choose for RAG?")
  → Technology comparison ("FastAPI vs Django for AI microservices?")
  → Market research ("Most used LLM APIs in enterprise applications 2026?")

LangChain + Web Search:
  from langchain_community.tools import DuckDuckGoSearchRun
  search = DuckDuckGoSearchRun()
  result = search.run("latest claude model api name")
  # Claude lo built-in Web Search idi same concept

LangChain + Research Mode equivalent:
  from langchain.agents import AgentExecutor
  # Multi-step research agent: plan → search → synthesize → report
  # Research Mode idi internally chestundi
```

---

## 10. Summary

```
Web Search:
  What: oka quick internet search → fast answer
  When: facts, prices, news, specific lookups
  How long: 5-15 seconds
  Output: single answer + citations
  Tagline: "Quick fact. Right now."

Research Mode:
  What: autonomous research agent → deep analysis
  When: analysis, comparison, strategy, reports
  How long: 2-45 minutes (background)
  Output: 1-2 page cited report
  Tagline: "Your analyst. Full brief."

Both:
  Toggle OFF by default — prathi chat lo enable cheyyali
  Same toggle bar — different power
  Citations included — sources verify cheyyochu

Decision rule:
  "5 seconds lo answer raavacha?"  → Web Search
  "Full analysis kaavali?"          → Research Mode
```
