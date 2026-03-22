# prompt-engineering
A comprehensive guide to prompt engineering:

## 1. What to think of when crafting a prompt
A prompt is simply a set of instructions given to an AI. You can think of it like a musical score(prompt) for an orchestra(AI) to play.
The orchestra performs completely differently depending on what it is given. And when an instructor is writing the musical score they must think of what the goal of the orchestra is. This goal depends on given the audience what should come across. Using this the instructor writes the score. This score doesn’t make sound itself—it’s a set of precise instructions that tells an orchestra who plays, what they play, how they play it, and when. 

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

Before you hit Enter, run your prompt through P.A.C.T. :

    P – Persona
    Have I assigned a clear role or perspective?

    A – Audience & Aim
    Who is this for, and what is the single goal?

    C – Constraints
    What are the boundaries? (length, tone, what to avoid, what to include)

    T – Template
    How should the answer be structured? (list, table, step‑by‑step, first‑principles explanation, etc.)

If any of these four is missing, your score has a blank staff—fill it in.

## 4. Before‑and‑After Example
The Scenario:
You’re building an ESP32‑S3 embedded system that collects sensor data (I2C daisy chain + UART sensors). You need a roadmap to store that data in an online database and display it on a website—all within one week.

Prompt Given: Give me a guide to making a website with sql in backend.

Why it's weak:
Persona: No Role given(The AI could reply as a junior developer, a marketing writer, or even a poet.)

Audience or Aim: No direction(Who is this for? The reader? A presentation? The goal is unclear—just “a guide.”)

Constraints: No limits(No limits on length, depth, or what to include/exclude. The AI doesn’t know about the ESP32, sensors, or the one‑week deadline.

Template: No structure(leads to random styling, AI will not give information in a structure for teaching someone without knowledge)

Structured prompt


Act as an experienced full-stack developer who has led IoT applications at scale.

I am a one-person team who has been working on creating an ESP32-S3 embedded system which will take input from multiple sensors in a I2C daisy chain with 2 sensors using UART. I am able to see my outputs when debugging and i can successfully store them on the chip. I have one week until I would like to get my project up and running taking data and storing it onto an online database. My goal is to have the sensor data correctly stored onto a database without having to manually format them. 


Your task is to create a roadmap.
-website should display the reading of each of the sensors individually on different tabs
-include a daily timeline for the next week with 2 hours of work each day
-three critical risks with directly inputting sensor data into database which is shown on html
-how to private website until it can be published
-how an esp32-s3 can connect to the database
-please suggest options that would be best for resume in an AI and embedded systems world in order to put on resume

Format: Present this as a clear, actionable document with section headings. Please explain technical jargon. Provide a quick case before refining it.
