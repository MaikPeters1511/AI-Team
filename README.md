# AI Team Project Workspace

Dieses Projekt ist eine hochmoderne, agentengesteuerte Entwicklungsumgebung, die auf agilen Scrum-Prozessen, Domain-Driven Design (DDD) und Clean Architecture basiert. Das Setup umfasst spezialisierte KI-Agenten, die unterschiedliche Rollen in einem agilen Software-Entwicklungsteam übernehmen.

## 🚀 Tech Stack

- **Backend:** .NET Core 10, C# 14, Wolverine
- **Frontend:** Angular 22, TypeScript 6, DaisyUI 5, i18n (DE/EN), ARIA (Accessibility)
- **Datenbanken:** PostgreSQL, Qdrant (Vektor-Datenbank)
- **Infrastruktur & Hosting:** .NET Aspire, Docker
- **Sicherheit & Auth:** Microsoft Identity, OWASP Guidelines
- **Künstliche Intelligenz:** OpenAI API, LMStudio, RAG (Retrieval-Augmented Generation)

## 🤖 Das Agenten-Team

Das Projekt wird von einem autarken Team spezialisierter Agenten unterstützt:

1. **`po-agent` (Product Owner):** Erstellt und verfeinert User Stories im Ordner `UserStories` und pflegt Backlogs mittels OpenSpec (`*.openspec.md`).
2. **`sm-agent` (Scrum Master):** Moderiert Dailys, löst Blocker und übernimmt die Sprintplanung.
3. **`architect-agent` (Tech Lead):** Überwacht Clean Architecture, Vertical Slices, schreibt ADRs (Architecture Decision Records) und führt High-Level Code Reviews durch.
4. **`frontend-agent` (Frontend Developer):** Entwickelt responsive UI-Komponenten nach TDD-Vorgaben. Baut "Dumb" und "Smart" Angular 22 Standalone Components mit DaisyUI.
5. **`backend-agent` (Backend Developer):** Implementiert APIs und Domain-Logik (.NET 10, C# 14, PostgreSQL) unter strenger Einhaltung von TDD und Clean Architecture/Vertical Slices.
6. **`ai-agent` (KI & Data Engineer):** Verwaltet LLM-Integrationen, RAG-Pipelines und Vector-Embeddings mit Qdrant.
7. **`qa-agent` (Quality Assurance):** Führt E2E-, Last- und API-Compliance-Tests durch.
8. **`devops-agent` (Platform Engineer):** Zuständig für .NET Aspire, Docker, CI/CD und Observability.
9. **`sec-agent` (Security & Identity):** Kapselt Authentifizierung, RBAC (Microsoft Identity) und sichert die API/Frontend-Routen ab.
10. **`ux-agent` (UX & Accessibility):** Garantiert WCAG-Konformität (ARIA), semantisches HTML und feingetuntes Interaction-Design.
11. **`doc-agent` (Technical Writer):** Erstellt Swagger/OpenAPI Doks, Readmes und hält alle Systemübersichten aktuell.

## 📐 Architektur- und Entwicklungsrichtlinien

* **Agile & OpenSpec:** Alle Anforderungen müssen als `*.openspec.md` im Ordner `UserStories` spezifiziert sein.
* **Test-Driven Development (TDD):** Tests (xUnit für .NET, Angular Testing) werden *vor* der Implementierung geschrieben. **Alle Tests liegen zwingend im Ordner `Tests`.**
* **Clean Architecture & Vertical Slices:** Strikte Trennung von Domain, Application, Infrastructure und Presentation/Web.
* **Domain-Driven Design (DDD):** Klare Definition von Aggregate Roots, Value Objects und Domain Events im Core-Layer.

## 📂 Projektstruktur

```text
.
├── CLAUDE.md          # Globale Projektregeln, von Claude Code automatisch geladen
├── .claude/
│   ├── agents/        # Subagenten-Definitionen (eine Rolle je Datei)
│   └── skills/        # Skills mit Details, Vorgehen und Templates je Rolle
├── UserStories/       # Zentrale Ablage für alle *.openspec.md Features & Stories
├── Tests/             # Zentraler Ordner für alle Frontend- und Backend-Tests
├── docs/adr/           # Architecture Decision Records
├── LICENSE            # MIT Lizenz
└── README.md          # Diese Datei
```

Dieses Projekt ist für **Claude Code** eingerichtet: `CLAUDE.md` wird bei jeder Session automatisch geladen, jede Rolle steht als Subagent (`.claude/agents/`) sowie als Skill (`.claude/skills/`) zur Verfügung.

## 📜 Lizenz

Dieses Projekt ist lizenziert unter der MIT Lizenz. Weitere Details findest du in der [LICENSE](LICENSE) Datei.
