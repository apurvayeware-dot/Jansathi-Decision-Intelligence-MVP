# JANSATHI — One Need. Multiple Support Paths.

> **Jansathi** is a civic-tech decision-support platform that helps people discover potential scholarships, schemes, subsidies, grants, loans, employment programs, healthcare assistance, housing support, and other support opportunities based on their individual needs.

**Live Demo:** https://jansathi-yw09.hatchable.site

---

## 🌱 What is Jansathi?

Finding government and social-support programs can be difficult because information is scattered across different sources and eligibility rules can be complicated.

Jansathi turns a user's situation into a structured support journey:

```text
USER NEED
   ↓
UNDERSTAND THE USER
   ↓
ASK RELEVANT QUESTIONS
   ↓
CHECK AVAILABLE SUPPORT
   ↓
CHECK ELIGIBILITY
   ↓
COMPARE OPTIONS
   ↓
BUILD MULTIPLE SUPPORT PATHS
   ↓
CALCULATE REMAINING GAP
   ↓
EXPLAIN WHY
   ↓
SHOW NEXT ACTIONS
   ↓
WHAT-IF / FALLBACK SCENARIOS
   ↓
APPLICATION TRACKING
```

### Example

A student could enter:

> "I am a student from Maharashtra. My family income is ₹2.5 lakh per year and I need ₹1 lakh for college fees."

Jansathi can structure the situation, identify potential support options, estimate the potential coverage available in its support repository, show the remaining financial gap, and provide a next-step plan.

---

## ✨ Key Features

### 🧭 Need-based support discovery
Users can describe their requirement naturally instead of searching through complicated categories.

### 🤖 AI-assisted understanding
AI is used for:

- Natural-language understanding
- Clarifying questions
- English, Hindi, and Hinglish interaction
- Plain-language explanations
- Understanding user intent

### ⚙️ Deterministic decision engine
Important eligibility and decision calculations are handled by deterministic application logic rather than allowing an AI model to invent eligibility results.

The project separates:

```text
AI
→ Understands and explains

Decision Engine
→ Calculates and evaluates

Support Repository
→ Provides opportunity data
```

### 🧩 Multiple support paths

Jansathi is designed to go beyond showing a single scheme.

It can construct combinations of possible support sources and calculate:

- Potential support
- Remaining financial gap
- Eligibility status
- Document readiness
- Application effort
- Deadline urgency
- Need relevance

### 🔮 What-If analysis

Users can explore scenarios such as:

> "What if my scholarship is rejected?"

The system can recalculate the support strategy and show alternative paths.

### 📋 Application tracking

Users can keep track of support opportunities and their application progress.

### 🌐 Multilingual interface

The interface supports:

- English
- Hindi
- Hinglish-friendly input

### 📱 Responsive design

The interface is designed for desktop and mobile screens.

### ♿ Accessibility considerations

The project includes:

- Keyboard focus states
- Responsive layouts
- Reduced-motion support
- Readable contrast on form controls
- Semantic interactive elements

---

## 🖥️ Main Pages

Jansathi is structured as a multi-step experience rather than putting everything on one screen.

| Page | Purpose |
|---|---|
| Home | Introduces Jansathi and support categories |
| Tell Us Your Need | Captures the user's requirement |
| Questions | Collects only relevant personal details |
| Profile Review | Lets the user verify their information |
| Analysis | Processes the support request |
| Results | Displays potential support options |
| Support Details | Explains individual opportunities |
| Support Plan | Builds a combined support strategy |
| What If? | Tests alternative scenarios |
| Applications | Tracks support applications |
| Profile | Stores user-specific information |
| Ask Jansathi | Natural-language assistance |

---

## 🎨 Design

The interface follows a modern civic-tech / SaaS design language:

- Glassmorphism
- Large readable typography
- Spacious layouts
- Rounded cards
- Transparent dark surfaces
- Subtle shadows
- Animated background
- High-resolution Rashtrapati Bhavan background
- Indian-inspired green visual language
- Responsive navigation
- Clear call-to-action buttons

The goal is to make a complex decision-support system feel approachable to everyday users.

---

## 🏗️ Architecture

```text
                    ┌─────────────────────┐
                    │      Jansathi UI    │
                    │ HTML / CSS / JS     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    API Endpoints    │
                    ├─────────────────────┤
                    │ /analyze             │
                    │ /simulate            │
                    │ /opportunities       │
                    │ /profile             │
                    │ /applications        │
                    │ /ai/understand       │
                    │ /ai/explain          │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             ▼                 ▼                 ▼
      ┌─────────────┐  ┌──────────────┐  ┌───────────────┐
      │ Eligibility │  │ Decision     │  │ Support Path  │
      │ Engine      │  │ Engine       │  │ Optimizer     │
      └─────────────┘  └──────────────┘  └───────────────┘
             │                 │                 │
             └─────────────────┼─────────────────┘
                               ▼
                    ┌─────────────────────┐
                    │ PostgreSQL Database │
                    └─────────────────────┘
```

---

## 📁 Project Structure

```text
jansathi/
│
├── public/
│   ├── index.html
│   ├── app.js
│   ├── theme.css
│   ├── login.html
│   ├── jansathi-logo.svg
│   └── rashtrapati-bhavan-clear.jpg
│
├── api/
│   ├── analyze.js
│   ├── simulate.js
│   ├── opportunities.js
│   ├── opportunities/
│   │   └── [id].js
│   ├── profile.js
│   ├── applications/
│   │   ├── index.js
│   │   └── [id].js
│   └── ai/
│       ├── understand.js
│       └── explain.js
│
├── lib/
│   ├── eligibilityEngine.js
│   ├── decisionEngine.js
│   └── supportPathOptimizer.js
│
├── seed.sql
├── seed_more.sql
├── seed_three.sql
├── seed_four.sql
├── hatchable.toml
└── README.md
```

---

## 🧠 Decision Engine

Jansathi uses a weighted decision model for comparing support opportunities.

| Factor | Weight |
|---|---:|
| Eligibility | 30% |
| Need relevance | 25% |
| Potential support coverage | 20% |
| Deadline urgency | 10% |
| Document readiness | 10% |
| Application effort | 5% |

These weights are part of the application logic and are not generated by the AI model at runtime.

### Eligibility states

The deterministic eligibility engine uses states such as:

```text
ELIGIBLE
POTENTIALLY_ELIGIBLE
NOT_ELIGIBLE
INSUFFICIENT_INFORMATION
```

This allows Jansathi to distinguish between:

- clearly matching information,
- potentially matching information,
- known mismatches,
- and cases where more information is required.

---

## 🤖 Role of AI

AI is intentionally limited to tasks where natural-language reasoning is useful.

### AI handles

- Understanding user messages
- Extracting intent
- Multilingual clarification
- Generating follow-up questions
- Explaining results in simple language
- Conversational assistance

### AI does not have final authority over

- Eligibility calculations
- Numerical support amounts
- Decision weights
- Database records
- Application status
- Deterministic scoring

This separation is intended to reduce hallucinated eligibility decisions and make the system easier to audit.

---

## 🗄️ Data Model

The project uses PostgreSQL-backed application data.

Important entities include:

### Profiles

Stores user-specific information such as:

- Location
- Household income
- Age
- Student status
- Occupation
- Education
- Need category
- Required amount
- Available documents

### Support Opportunities

Represents potential sources of assistance.

Examples include:

- Scholarships
- Subsidies
- Grants
- Loans
- Training programs
- Employment programs
- Healthcare assistance
- Housing support

### Applications

Tracks the user's progress with support opportunities.

---

## 🔐 Authentication

Jansathi uses Hatchable's authentication system.

Current configuration supports:

```toml
[auth]
enabled = true
providers = ["email", "google"]
```

Email authentication is the primary supported flow. Google Sign-In can be activated through the Hatchable project configuration when the required Google OAuth setup is completed.

> Do not store passwords or authentication secrets directly in the frontend source code.

---

## ⚠️ Demo Data & Eligibility Disclaimer

The current Jansathi demonstration environment contains fictional/demo support data.

**DEMO DATA is clearly marked in the application.**

Jansathi should not be treated as an official government eligibility authority.

Before applying for any real program, users should verify:

- Official eligibility requirements
- Current application dates
- Required documents
- Available funding
- Official application procedure
- Information on the relevant government or authorized organization website

No eligibility result or support amount shown by the demo should be considered guaranteed.

---

## 🚀 Running / Deploying

Jansathi is currently built for the **Hatchable** platform.

The platform provides:

- PostgreSQL database
- API runtime
- Authentication
- AI services
- Storage
- Deployment
- Hosting

The project configuration is stored in:

```text
hatchable.toml
```

For a Hatchable deployment, project files are deployed through the Hatchable project environment.

If adapting Jansathi to another platform, the following pieces need to be replaced or configured:

1. Authentication
2. PostgreSQL connection
3. API runtime
4. AI provider
5. Environment secrets
6. Deployment configuration

---

## 🛠️ Technology Stack

### Frontend

- HTML5
- CSS3
- Vanilla JavaScript
- Responsive CSS
- SVG

### Backend

- JavaScript
- Hatchable API runtime
- PostgreSQL
- Hatchable SDK

### AI

- Hatchable AI service
- Natural-language understanding
- Explanation generation

### Architecture

- REST-style API endpoints
- Deterministic eligibility engine
- Weighted decision engine
- Support-path optimization
- Database-backed profiles and applications

---

## 🔒 Privacy & Security Principles

Jansathi is designed around the principle that personal information should only be used to improve the user's own support discovery experience.

Important principles:

- User profile data should be private.
- Applications should be scoped to the authenticated user.
- Authentication should be handled by the platform.
- Secrets should never be committed to GitHub.
- API authorization should be enforced server-side.
- Sensitive information should not be exposed through frontend JavaScript.

---

## 🗺️ Future Roadmap

Potential future improvements include:

- [ ] Verified real-world government scheme repository
- [ ] Official-source verification links
- [ ] More Indian states and districts
- [ ] Document checklist generation
- [ ] Application deadline reminders
- [ ] Application status notifications
- [ ] Personalized support timelines
- [ ] Voice-based interaction
- [ ] More Indian languages
- [ ] OCR/document understanding
- [ ] Mobile application
- [ ] Improved accessibility
- [ ] Public analytics dashboard using anonymized data
- [ ] More advanced support-path optimization

---

## 🤝 Contributing

Contributions are welcome.

A typical contribution workflow:

```bash
git clone <repository-url>
cd jansathi

git checkout -b feature/your-feature

# Make your changes

git add .
git commit -m "Add your feature"
git push origin feature/your-feature
```

Then open a Pull Request.

### Contribution guidelines

When contributing:

- Keep eligibility logic deterministic.
- Do not invent government schemes or official URLs.
- Clearly label demo/mock data.
- Do not commit secrets or credentials.
- Keep personal user data private.
- Prefer accessible UI components.
- Test responsive layouts.
- Keep AI responsible for language/reasoning assistance rather than authoritative eligibility decisions.

---

## 📜 License

Choose a license appropriate for your intended use before publishing the repository.

For example:

- MIT — permissive open-source use
- Apache-2.0 — permissive with additional protections
- GPL-3.0 — requires derivative distributions to remain under GPL

If this project is intended for a competition, college project, startup, or future commercial product, select the license after deciding how you want others to reuse the code.

---

## 👨‍💻 Project

**Jansathi**

> **One Need. Multiple Support Paths.**

Built as a civic-tech decision-support project focused on making support discovery simpler, more understandable, and more actionable.

**Current deployment:** v16
