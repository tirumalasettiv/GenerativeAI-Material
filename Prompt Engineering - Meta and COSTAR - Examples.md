# Prompt Engineering — Meta and COSTAR

*Companion examples for the "Prompt Engineering — Meta and COSTAR" deck.*

Prompt engineering is just **structuring your instructions** so an AI gives you its best output — like giving precise directions instead of "go somewhere nice." Two tools cover almost every situation:

| Tool | Use it when… | One-line idea |
|---|---|---|
| **Meta Prompting** | You *don't* know how to structure the request | Let the AI write the prompt for you |
| **COSTAR** | You *know* how to structure the request | Fill six parts so nothing is left to chance |

> **Vague vs. precise, in one line**
> ❌ *"Take me somewhere nice."*
> ✅ *"Take me to Times Square NYC using the fastest route."*
> Same idea applies to every prompt below.

---

## Tool 1 — Meta Prompting

**Idea:** Don't struggle to structure a complex request. Tell the AI your *goal* and let it act as your prompt engineer. You stay in charge of the goal; the AI does the crafting.

### The meta-prompt template (copy this)

```text
Act as an expert Prompt Engineer. Please write the best possible prompt
that I can use to get a world-class response from you. Include any
necessary context, role-playing personas, or constraints that will make
the output high-quality.

My goal: <describe what you want in plain language>
```

### Example — *Draft a job description for an AI Engineer*

**❌ Vague prompt**

```text
Write a job description for an AI Engineer.
```

*Likely output:* a generic, interchangeable posting — "We are seeking a talented AI Engineer to join our team. Responsibilities include developing AI models…" Could belong to any company; says nothing about you.

**✅ Meta-prompted approach**

Step 1 — hand the AI your goal using the template:

```text
Act as an expert Prompt Engineer. Write the best possible prompt I can use
to get a world-class response.

My goal: Draft a job description for hiring an AI Engineer — responsibilities,
must-have skills, and why our team is a great place to work.
```

Step 2 — the AI returns a *structured prompt* you can run, e.g.:

```text
You are an experienced technical recruiter and hiring manager. Write a job
description for a Senior AI Engineer.

Context: a product team shipping GenAI features (RAG, agents) in an
enterprise setting.
Include: role summary, 5–7 key responsibilities, must-have skills
(Python, LLMs/RAG, cloud), nice-to-haves, and a short "why join us"
section highlighting impact, growth, and team culture.
Tone: confident and human, not corporate boilerplate.
Format: headed sections, scannable bullet points, ~350 words.
```

Step 3 — run that prompt → a targeted, on-brand job description instead of filler.

**Why it works:** the hard part (structuring the request) shifts from you to the AI.

---

## Tool 2 — COSTAR

**Idea:** A six-part checklist. Fill all six and the AI knows not just *what* to do, but *how*, *for whom*, and *in what format*.

| Part | Stands for | What to put |
|---|---|---|
| **C** | Context | Background that helps the AI understand your situation and constraints |
| **O** | Objective | The specific goal or outcome you want the AI to achieve |
| **S** | Style | The writing style — formal, casual, technical, creative, journalistic |
| **T** | Tone | The emotional register — encouraging, authoritative, empathetic, direct |
| **A** | Audience | Who will read or use the output — experts, beginners, executives, customers |
| **R** | Response | The output format — paragraph, bullet list, table, email, code block |

### Reusable COSTAR template

```text
Context:  <situation + constraints>
Objective: <what you want produced>
Style:     <writing style>
Tone:      <emotional register>
Audience:  <who it's for>
Response:  <format, length, structure>

Task: <the thing to write>
```

### Example — *Write a rejection email to a strong candidate*

**❌ Vague prompt**

```text
Write a rejection email to a candidate.
```

*AI returns:*
> "We have decided to move forward with other candidates. Thank you for your interest."

Cold, generic, forgettable — and a burned relationship.

**✅ COSTAR prompt**

```text
Context:  Rejecting a high-potential candidate over cultural-fit concerns
          (strong skills, but not the right pace for our team).
Objective: Write a rejection email that preserves the relationship.
Style:     Professional, warm, conversational.
Tone:      Empathetic, encouraging, honest.
Audience:  A talented engineer with 10 years of experience.
Response:  Email format, 3–4 paragraphs, 150–200 words.

Task: Write the rejection email.
```

*AI returns (excerpt):*
> "Your technical skills are genuinely impressive… This wasn't about your
> qualifications — it's about cultural fit… We'd love to stay connected."

Warm, specific, relationship intact.

**Why it works:** miss even one part and the output drifts generic. All six, and the AI has the full picture.

---

## Side-by-side summary

| | Vague | Meta Prompting | COSTAR |
|---|---|---|---|
| **You provide** | A one-liner | Your *goal* | Six labeled inputs |
| **AI provides** | A guess | A polished prompt to run | A targeted output |
| **Best for** | Nothing reliable | When you don't know how to structure it | When you know how to structure the request |
| **Result** | Generic, hit-or-miss | World-class prompt, then output | Precise output first try |

**Combine them for complex work:** meta-prompt to break the task down, then COSTAR to execute each piece.

---

## Three rules before you ship anything

1. **Verify what matters.** A great prompt improves quality — it does not guarantee truth. AI can state wrong facts with full confidence. Check anything before it leaves your hands.
2. **Protect the data.** Never paste confidential, customer, or personal data into AI tools that aren't company-approved. When in doubt, leave it out.
3. **You stay accountable.** The AI drafts; you decide. Judgment, sign-off, and responsibility always remain with the human.

---

### This week
1. Pick one task you write or analyze often.
2. Don't know how to structure it? **Meta-prompt it** — let the AI draft the prompt from your goal.
3. Know how to structure it? **Run COSTAR** — tune all six parts, then save the prompt to reuse.
