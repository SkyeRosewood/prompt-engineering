# prompt-engineering
A comprehensive guide to prompt engineering:

| Prompt Type | Example |
| :--- | :--- |
| ❌ **Vague Prompt** | "Tell me how to build a website." |
| ✅ **Engineered Prompt** | "Act as a senior developer. Give me a 7-day roadmap to build a portfolio website using HTML/CSS. Assume I know nothing about code. Format as a table with 'Day,' 'Task,' and 'Why this matters.'" |


This guide teaches you how to consistently get the result on the right.
## 1. What to think of when crafting a prompt
A prompt is simply a set of instructions given to an AI. You can think of it like a musical score(prompt) for an orchestra(AI) to play.  

The orchestra performs completely differently depending on what it is given. And when an instructor is writing the musical score, they must think of what the goal of the orchestra is. This goal depends on given the audience what should come across. This score doesn’t make sound itself—it’s a set of precise instructions that tells an orchestra who plays, what they play, how they play it, and when. 

Your AI is that orchestra. A vague prompt is like handing them a napkin with “play something sad” scribbled on it. A perfect prompt is a fully orchestrated score—every section knows its role, the structure is clear, and the emotional intention is baked into the instructions.

## 2. The 4 Key Ingredients (Mapped to the Score)

| Ingredient | Musical Analogy | Definition |
| :--- | :--- | :--- |
| **Role** | Instrumentation | Who is playing? Assign the AI a persona, expertise level, or perspective. |
| **Context** | Key & Tempo | The setting, constraints, and background information that frame the response. |
| **Task** | The Melody | The single, clear action you want performed. |
| **Structure & Format** | Form & Dynamics | How the answer should be organized, styled, and delivered. |

### Ingredient 1: Role (Instrumentation)
Weak: “Give me marketing ideas.”
Strong: “Act as a senior brand strategist who specializes in launching D2C products to Gen Z. Avoid clichés like ‘disrupt’ and ‘synergy.’”

Why it works: The weak version leaves the AI to guess its own voice. The strong version selects the right “instrument” and even gives stylistic guardrails.

### Ingredient 2: Context (Key & Tempo)

Weak: “Explain what a blockchain is.”
Strong: “Explain blockchain to my 70‑year‑old father who understands banking but has never used a computer. Use a comparison to a physical ledger book that multiple people hold.”

Why it works: Context sets the level, the metaphor, and the user’s background. Without it, the AI defaults to a generic textbook definition.

### Ingredient 3: Task (The Melody)

Weak: “What should I do about my team conflict?”
Strong: “List three actionable steps I can take as a manager to de‑escalate a conflict between two senior engineers who disagree on system architecture. Each step should include a suggested script I can say in a 1:1 meeting.”

Why it works: The weak task is open‑ended and invites vague advice. The strong task specifies a precise output (list of steps) with a concrete deliverable (scripts).

### Ingredient 4: Structure & Format (Form & Dynamics)

Weak: “Tell me about productivity methods.”
Strong: “Compare the Pomodoro Technique and time blocking in a table with three columns: ‘Best for (type of work)’, ‘Key downside’, and ‘One‑sentence summary’. End with a recommendation for a software developer who has frequent interruptions.”

Why it works: The weak format leaves the AI to choose (often resulting in a paragraph). The strong format dictates the exact container, making the output immediately usable.

## 3. The Golden Rule Framework: P.A.C.T.

Before you hit Enter, run your prompt through P.A.C.T.:

    P – Persona
    Have I assigned a clear role or perspective?

    A – Audience & Aim
    Who is this for, and what is the single goal?

    C – Constraints
    What are the boundaries? (length, tone, what to avoid, what to include)

    Task

    T – Template
    How should the answer be structured? (list, table, step‑by‑step, first‑principles explanation, etc.)

4 Ingredients     P.A.C.T. Check\
──────────────────────────────────\
Role            ──────────►  Persona\
Context & Task  ──────────►  Audience & Aim\
Context & Task  ──────────►  Constraints\
Structure       ──────────►  Template

If any of these four is missing, your score has a blank staff—fill it in.

## 4. Industry Standard: Introduce "Structured Prompting" (XML Tags)
Industry Standard: Google, Microsoft, and OpenAI recommend using XML tags or Markdown headers to separate instructions from content. This prevents the AI from confusing your "instructions" with the "context" you are giving it.

To ensure the AI doesn’t get confused, wrap your instructions in tags. This is how professionals structure prompts:

    <system>
    You are a friendly coding tutor for teenagers.
    </system>

    <context>
    I am 15 years old. I know what a variable is but I don't understand loops.
    </context>

    <instruction>
    Explain 'for loops' using a pizza delivery analogy.
    </instruction>

    <format>
    Use bullet points, and end with a 3-question quiz to test my understanding.
    </format>

## 5. Before‑and‑After Example

#### Unstructured Prompt
*“Help me write a cover letter for a job at a bookstore.”*

**Why it’s weak:**  
- **Persona:** None – the AI doesn’t know if it’s a career coach, a friend, or a formal HR tool.  
- **Audience & Aim:** Unclear – is this for a manager? A chain store? What’s the goal?  
- **Constraints:** No limits – the AI might write a novel or three sentences.  
- **Template:** No structure – it’s likely to produce a standard, forgettable paragraph.

#### Structured Prompt (Using P.A.C.T.)

**Persona**  
Act as an experienced hiring manager who has worked in independent bookstores for years.

**Audience & Aim**  
I’m a 16‑year‑old applying for my first job at “Cornerstone Books,” a local indie shop. I want to highlight my love for reading, reliability, and willingness to learn. My goal is to get an interview.

**Constraints**  
- Keep the letter to one page.  
- Use a friendly but professional tone.  
- Include a short sentence about my experience organizing a school book fair (even though it wasn’t a paid job).  
- Avoid buzzwords like “synergy” or “rockstar.”

**Template**  
Format as a standard business letter (my address, date, their address, salutation, body, closing). In the body, use three short paragraphs:  
1. Why I love this specific bookstore.  
2. How my skills match the job (even without prior work experience).  
3. A call to action (I’ll follow up next week).

**Why the structured prompt works:**  
Every element of P.A.C.T. is filled. The AI now knows exactly what voice to use, who the letter is for, what to include (and avoid), and how to structure it. The result is a tailored, interview‑worthy letter rather than a generic template.

### Example 2: Advanced – IoT System with ESP32‑S3
The Scenario:
You’re building an ESP32‑S3 embedded system that collects sensor data (I2C daisy chain + UART sensors). You need a roadmap to store that data in an online database and display it on a website—all within one week.

#### Unstructured prompt

Prompt: Give me a guide to building a website with SQL as the backend.

Why it's weak:
- Persona: No Role given(The AI could reply as a junior developer, a marketing writer, or even a poet.)
- Audience or Aim: No direction(Who is this for? The reader? A presentation? The goal is unclear—just “a guide.”)
- Constraints: No limits(No limits on length, depth, or what to include/exclude. The AI doesn’t know about the ESP32, sensors, or the one‑week deadline.
- Template: No structure(leads to random styling, AI will not give information in a structure for teaching someone without knowledge)

#### Structured prompt
~~~
<Persona>
Act as an experienced full-stack developer who has led IoT applications at scale.
</Persona>

<Audience and Aim> 
I am a solo developer building an ESP32-S3 system. My goal is to have sensor data stored in an online database and displayed on a website within one week. I would like data to format itself when coming into the database. Your task is to create a daily roadmap. The audience for this roadmap is me (technical, but needs clear steps).
</Audience and Aim>

<Constraints> 
- The ESP32-S3 uses an I2C daisy chain with two UART sensors.
- The website should display the readings of each of the sensors individually on different tabs
- Include a daily timeline for the next week with 2 hours of work each day
- Three critical risks when directly sending sensor data to a database and showing it in HTML, with mitigations
- Keep the private website until it can be published
- Include how an ESP32-S3 can connect to the database
- Recommendations for making this project stand out on a resume in AI/embedded systems for FAANG companies.
</Constraints>

<Template>
Template: Present this as a clear, actionable document with section headings. Please explain technical jargon. Provide a quick case before refining it.
</Template>
~~~
The weak prompt is a napkin scribble; the strong prompt is a fully orchestrated score.

## 6. Common Pitfalls (and Why They Happen)

### Pitfall 1: No Persona
**What you type:**  
*"Write a poem about space."*
**What the AI thinks:** 
*"I have no identity. I will write the most generic, neutral poem possible to avoid offending anyone."*
**The Result:**
Boring, cliché poetry.
**The Fix (Persona):**
*"Act as a grumpy astronaut who misses Earth. Write a poem about space."*
**Why it works:**
You give the AI a perspective to filter language through. It now knows to use words like "lonely," "tin can," and "blue dot" instead of "vast" and "mysterious."

---

### Pitfall 2: Forgetting Output Language or Level
**What you type:**  
*“Explain how a CPU works.”*

**What the AI thinks:**  
*“I don’t know if you’re a computer science professor or a curious 10‑year‑old. I’ll default to a mid‑level textbook explanation.”*

**The result:**  
Often too technical or too simplistic—rarely a perfect fit.

**The fix (Constraints):**  
*“Explain how a CPU works as if I’m a 12‑year‑old who loves Minecraft. Use a redstone comparator analogy.”*

**Why it works:**  
The AI adjusts its vocabulary, analogy, and depth to match the specified audience.

---

### Pitfall 3: Vague Verbs Like “Talk about” or “Discuss”
**What you type:**  
*“Talk about climate change.”*

**What the AI thinks:**  
*“Should I list causes? Effects? Solutions? Argue for action? Write a poem? You didn’t specify.”*

**The result:**  
A broad, unstructured essay that might not give you what you actually needed.

**The fix (Task):**  
*“List three specific actions an individual can take to reduce their carbon footprint. For each, include a rough cost estimate and a one‑sentence explanation of why it helps.”*

**Why it works:**  
Concrete verbs (*list, compare, summarize, create, evaluate*) force a precise output shape, eliminating guesswork.

---

### Pitfall 4: Asking Multiple Unrelated Questions in One Prompt
**What you type:**  
*“What’s the weather in Tokyo? Also, give me a pasta recipe. And tell me a joke.”*

**What the AI thinks:**  
*“I’ll try to jam three unrelated things together, probably with awkward transitions. Something will get buried.”*

**The result:**  
A messy answer where one part (often the last) is brief or forgotten.

**The fix (Aim):**  
Pick **one goal per prompt**. If you need multiple answers, run separate prompts.

**Why it works:**  
The AI gives each request its full attention. You get cleaner, deeper outputs.

## 7. Why this works

- Persona – Large language models predict likely continuations based on context. A persona primes the model’s internal “role” distribution, narrowing the space of plausible responses.
- Constraints – Reducing the degrees of freedom prevents hallucinations and off‑topic tangents. It’s like giving a painter a canvas size and color palette instead of a blank wall.
- Template – Explicit format instructions override the model’s default tendency to produce prose, leading to more usable outputs.
- Audience & Aim – Aligning the output to a specific reader and goal reduces the need for iterative refinement.
