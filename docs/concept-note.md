# TedGy: A Paper-Loop AI System for Classroom Project Management

*Concept note — May 2026*

---

## The Problem

Middle school project-based learning is hard to manage. Teachers like Ted run multi-week projects with multiple teams, each moving at its own pace. Rigid tools — Trello, Jira, Google Classroom — enforce a fixed workflow and require kids to be on computers. Human tutoring at the per-team level is too labor-intensive to scale. And most adaptive systems treat all teams identically, unable to respond to the real divergence that happens when five teams tackle the same project differently.

## The Idea

What if you could have an AI tutor for each team — one that remembers everything the team has done, adapts to their specific progress, and communicates entirely through paper?

TedGy is a **paper-loop AI system**. Each day, every team gets a printed sheet: a kid-friendly task list, a Gantt chart showing where they are in the project, and fill-in sections for that day's work. Students annotate it by hand — checking off tasks, writing in names, filling out diagrams — and never touch a computer. Each evening, the teacher's aide scans the sheets. The AI reads them, updates each team's running context, and generates tomorrow's sheets — adapted to what each team actually accomplished today.

## What Makes It New

**The combination hasn't been done before:**

- Paper kanban (Toyota, 1950s) — physical, tactile, but static
- AI tutoring systems — adaptive, but screen-bound
- Per-team scaffolding — exists in research, not in practice at this scale
- Wizard of Oz interfaces — a human steering an AI system, well-studied in HCI

TedGy combines all four: AI that reads physical paper, maintains a separate long-running conversational context per team, and writes back to paper — with a human operator ("The Wizard") steering the whole thing nightly.

## How It Works

**Setup:** The teacher provides a project plan (as a PowerPoint — no new tools to learn). The system extracts the day-by-day structure and initializes a separate AI conversation for each team.

**Each morning:** The system generates a printed PDF for each team. One page. It includes:
- A header: team name, current day, where they are in the project arc
- A plain-English "where we are / where we're going" paragraph written by the AI specifically for that team
- A kid-friendly Gantt chart (weeks × tasks, shaded by status)
- Today's task checklist with physical checkboxes
- Fill-in sections (role assignments, structured diagrams, etc.)

**During the day:** Students work entirely on paper. They check off tasks, pencil in names, fill out diagrams. No screens.

**Each evening (the "Wizard's loop"):**
1. Aide scans the day's annotated sheets (grayscale, document feeder)
2. The AI reads each team's scan and produces a summary — progress, issues flagged, teams ahead or behind
3. The Wizard (operator) reads the summary and writes an "OzNote": plain-English guidance for the next day ("remind team Alpha to finish their uncompleted task," "team Beta is ready to move ahead")
4. The AI generates tomorrow's sheets, one per team, incorporating the OzNote and each team's individual history
5. Wizard reviews and iterates on the OzNote until the sheets look right
6. Sheets are printed and ready for morning

**The key insight:** Each team has its own independent AI conversation that accumulates context over the entire project. The AI knows team Alpha spent two days stuck on their persona definition. It knows team Beta is ahead of schedule. It knows team Gamma has a strong product manager but a weak marketing lead. No database captures this — it lives in the conversation.

## Why Paper?

- **Keeps students off screens** during collaborative work — a deliberate pedagogical choice
- **Paper is a shared object**: teams spread it on a desk, point at it, argue over it, carry it around
- **Lower stakes than digital**: students mark up paper freely in ways they wouldn't click through a form
- **No distractions**: no browser tabs, no notifications, no temptation to Google the answer

## Why AI?

- **Flexibility that rigid tools can't fathom**: the daily sheet adapts to what each team actually did, not what the tool expected them to do
- **Scales human attention**: one Wizard can oversee five teams with fifteen minutes of nightly review
- **Longitudinal memory**: the AI never forgets that team Alpha had that rough day in week two

## The Name

Working title: **TedGy** (Ted's Guidance). The operator role is called **The Wizard** and nightly instructions are called **OzNotes** — the man behind the curtain steering the AI without the students ever knowing.

---

*This is a working concept note. No code exists yet — the architecture is designed and implementation is the next step.*
