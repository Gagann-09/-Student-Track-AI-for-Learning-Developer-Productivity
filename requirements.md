**FutureSelf AI - Requirements**

**1. Functional Requirements**

-   Email/password authentication (JWT-based)
-   VS Code Extension (Open-source)
-   Code activity metadata capture (no raw code storage)
-   Skill Graph creation & dynamic update
-   Basic growth trajectory prediction (Linear regression model)
-   Dashboard displaying:
    -   Current skill index
    -   6-month projected growth
    -   Suggested micro-improvement tasks
-   Repeated mistake detection
-   Burnout risk indicator (heuristic-based)

**2. Non-Functional Requirements**

-   Must run on a laptop with 8GB RAM
-   Backend memory usage < 1.5GB
-   API response time < 2 seconds
-   Fully deployable on free cloud tiers
-   Modular and extensible architecture

**3. Software Stack**

Backend: - Python 3.x - FastAPI - Uvicorn

Database: - PostgreSQL

Frontend: - React.js (Open-source) - Tailwind CSS

AI / ML: - Scikit-learn - PyTorch (Open-source) - Ollama (Local LLM runtime)

IDE Integration: - VS Code Extension API

Deployment: - Render - Railway - Fly.io - GitHub Pages (Frontend)

**4. MVP Scope**

-   Track coding session duration
-   Track error frequency
-   Compute skill confidence score
-   Display projected growth graph
-   Generate improvement recommendations

**5. Constraints**

-   No paid APIs
-   No proprietary LLM dependency
-   Must run fully offline if required