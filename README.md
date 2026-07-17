Project 1:
# Full Stack Project — Responsive Frontend Interface

A responsive website built for DecodeLabs' Full Stack Development Industrial Training Kit — **Project 1: The Responsive Layout**.

A mobile-first, framework-free frontend interface built with pure HTML, CSS, and JavaScript — no libraries, no build step.

## Features
- **Semantic HTML5** — `header`, `nav`, `main`, `article`, `aside`, `footer` landmarks instead of div-soup
- **CSS Grid** for macro page layout, **Flexbox** for micro components (nav, buttons, filter chips)
- **Mobile-first responsive design** — single column by default, expanding at `768px` (tablet) and `1024px` (desktop)
- **Fluid typography** via `clamp()` — text scales smoothly instead of jumping at breakpoints
- **Interactive JavaScript** — mobile nav toggle, light/dark theme toggle, live search and category filtering, a checklist-driven progress bar, and a scroll-aware back-to-top button
- **Accessible by design** — skip link, visible focus states, `aria-*` attributes, and support for `prefers-reduced-motion`

## Tech stack
- HTML5
- CSS3 (Grid, Flexbox, custom properties)
- Vanilla JavaScript (no frameworks)
## Getting started
No build tools required. Just open `index.html` in a browser, or serve it locally:
python3 -m http.server 8000
## File structure
index.html   # Semantic page structure
style.css    # Mobile-first styles, design tokens
script.js    # Vanilla JS interactivity

project 3:
# DecodeLabs Tasks

A Task Manager API built for DecodeLabs' Full Stack Development Industrial Training Kit — **Project 3: Database Integration**.

Connects a backend to a database to store, retrieve, update, and delete data through a RESTful API, with a small demo console to exercise it.

## Features
- **Users, Tasks, Categories** — full CRUD over all three resources
- **Relational schema** — one-to-many (users → tasks) and many-to-many (tasks ↔ categories via a junction table)
- **RESTful routes** — CREATE = POST, READ = GET, UPDATE = PUT, PARTIAL UPDATE = PATCH, DELETE = DELETE
- **Data integrity** — `UNIQUE`, `NOT NULL`, and `CHECK` constraints enforced at the database level
- **SQL injection protection** — every query uses parameterized statements, never string concatenation
- Zero external dependencies — built with Node's built-in `node:sqlite` and `http` modules

## Tech stack
- Node.js (built-in `http` server, no Express)
- SQLite via `node:sqlite`
- Vanilla HTML/CSS/JS demo frontend

## Getting started
node server.js

Then open `http://localhost:3000` for the demo console, or hit the API directly at `http://localhost:3000/api`.

## API overview

| Resource | Endpoints |
|---|---|
| Users | `GET/POST /api/users`, `GET/PUT/DELETE /api/users/:id` |
| Categories | `GET/POST /api/categories`, `DELETE /api/categories/:id` |
| Tasks | `GET/POST /api/tasks`, `GET/PUT/PATCH/DELETE /api/tasks/:id` |
| Task ↔ Category links | `POST /api/tasks/:id/categories`, `DELETE /api/tasks/:id/categories/:categoryId` |
## File structure
server.js       # HTTP server + REST routing
db.js           # Schema, connection, seed data
public/
  index.html    # Demo console
README.md



## About

Batch 2026 · Powered by [DecodeLabs](https://www.decodelabs.tech)
