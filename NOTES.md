# Courtside — Dev Notes

Running log of what we built, why, and key decisions.
Updated after every feature so any session can catch up fast.

---

## Session 1 — Project setup (2026-06-28)

### What we decided
Chose the tech stack for the whole project before writing any feature code.

### Stack & reasoning

| Layer | Technology | Why |
|---|---|---|
| Backend | Java + Spring Boot | User already knows Java from CS courses; Spring Boot is industry-standard and explicit about what it does |
| Database | PostgreSQL + Spring Data JPA | Relational DB that maps well to NBA stats (players, games, stats are naturally tabular); JPA maps Java classes to tables |
| Frontend | Angular + TypeScript | More opinionated than React (less decision fatigue for a learner); TypeScript enforces types which catches mistakes early |
| LLM | Claude API (Haiku model) | Simple HTTP call, affordable, fast; we'll use context-stuffing (pass relevant stats as text in the prompt) rather than a vector DB |
| Stats source | balldontlie API | Free, no auth required for basic endpoints |

### Key decisions
- **No vector database (yet).** For the LLM layer we'll use "context stuffing" — fetch the relevant rows from our own DB and paste them into the prompt. Simple, understandable, good enough for this data volume.
- **TypeScript everywhere on the frontend.** Angular uses TS by default; no extra config needed.
- **One feature at a time.** We build vertical slices (data → DB → API → UI) rather than building all layers at once.

### What we built this session
- `.gitignore` covering Java/Maven, Angular/Node, secrets, and IDEs
- `README.md` with project description and stack summary
- This `NOTES.md`

### What's next
- Scaffold the Spring Boot backend project
- Connect it to a local PostgreSQL database
- Pull the first piece of data from balldontlie (e.g. today's games)

---
