**FutureSelf AI - System Design**

**1. High-Level Architecture**

User (VS Code Extension) | v FastAPI Backend (Python) | v PostgreSQL | v Trajectory Simulation Engine (Scikit-learn / PyTorch) | v Recommendation Generator | v React Dashboard 

**2. Core Components**

**A. Skill Graph Model**

-   Nodes: Programming Concepts
-   Edge Weight: Dependency strength
-   Node Score: Confidence level (0--100)
-   Decay Factor: Forgetting coefficient

Implementation: - Graph represented using adjacency matrix - Stored in
PostgreSQL JSON

**B. Trajectory Simulation Engine**

Input: - Historical skill scores - Session duration - Error frequency

Model Options: - Linear Regression (Scikit-learn) - Reinforcement
scoring heuristic - Gradient boosting (Optional)

Output: - 3-month projection - 6-month projection - Optimal growth trajectory

**C. Burnout Risk Predictor**

Inputs: - Consecutive coding hours - Declining performance trend - Increased error rate

Method: - Weighted scoring model - Simple classification model (Logistic regression)

**D. Intervention Generator**

Logic: - Identify gap between current trajectory & optimal trajectory -
Generate micro-task recommendation - Suggest topic focus shift

**3. Data Flow**

1.  User writes code
2.  Extension captures metadata (time, errors, patterns)
3.  Backend updates Skill Graph
4.  Simulation Engine recalculates projections
5.  System computes delta from optimized state
6.  Dashboard displays analytics & recommendations

**4. Security Model**

-   JWT Authentication
-   HTTPS
-   No raw source code stored
-   Local-first architecture supported

**5. Deployment Plan**

Development: - Local machine

Testing: - Docker (Open-source)

Production: - Backend: Render - Database: Supabase - Frontend: Vercel Free - LLM Runtime: Ollama Local

**6. Scalability Plan**

-   Containerized services
-   Horizontal scaling possible
-   Stateless backend design