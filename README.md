# Courtside

An AI-powered NBA fan dashboard built as a learning project.

## What it does
- Pulls live game and player stats from the [balldontlie API](https://www.balldontlie.io/)
- Stores them in a PostgreSQL database
- Exposes a REST API built with Java + Spring Boot
- Displays stats in an Angular dashboard
- Lets you ask natural-language questions about the stats (e.g. *"how has this player's 3-point % trended this season?"*) using the Claude API

## Stack

| Layer | Technology |
|---|---|
| Backend | Java 21 + Spring Boot 3 |
| Database | PostgreSQL + Spring Data JPA |
| Frontend | Angular 17+ (TypeScript) |
| LLM | Anthropic Claude API (Haiku) |
| Stats source | balldontlie API |

## Project structure (will grow over time)
```
courtside/
├── backend/    # Spring Boot application
├── frontend/   # Angular application
└── NOTES.md    # Running dev log — decisions, what we built and why
```

## Getting started
_Setup instructions will be added as each piece is built._
