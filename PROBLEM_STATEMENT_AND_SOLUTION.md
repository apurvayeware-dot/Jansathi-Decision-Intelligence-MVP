# Jansathi — Problem Statement & Solution

> **Jansathi — One Need. Multiple Support Paths.**  
> An AI-assisted decision-support platform that helps people discover, understand, compare, and act on relevant support opportunities.

---

## 1. Problem Statement

Millions of people are eligible for scholarships, government schemes, subsidies, grants, loans, employment programs, skill-development initiatives, healthcare assistance, housing support, agricultural schemes, and other forms of financial or social support.

However, the existence of these programs does not guarantee that people can actually access them.

The main problem is not simply the lack of information. It is the **difficulty of finding the right information, understanding eligibility, comparing multiple options, and deciding what to do next.**

Information is often distributed across different portals, departments, institutions, websites, PDFs, application systems, and local channels.

A person may need to answer questions such as:

- Which schemes are relevant to my situation?
- Am I eligible?
- What documents do I need?
- How much support could I potentially receive?
- Which options can be combined?
- What happens if one application is rejected?
- How much of my financial need will remain uncovered?
- What should I apply for first?
- What should I do next?

For a common user, answering these questions manually can be time-consuming and confusing.

---

# 2. Core Problem

### Information exists, but decision-making is difficult.

Traditional scheme-discovery systems generally require users to:

1. Know what program they are looking for.
2. Search through multiple sources.
3. Read eligibility requirements.
4. Compare different programs manually.
5. Understand complex documentation requirements.
6. Calculate how different forms of support could help.
7. Decide which applications to prioritize.
8. Track applications separately.

This creates a gap between:

> **"There may be support available for me."**

and

> **"I know exactly which support paths I can pursue and what I should do next."**

Jansathi is designed to address this decision gap.

---

# 3. Why Existing Approaches Are Not Enough

A conventional search experience may return a list of schemes.

But a list alone does not answer the user's complete problem.

For example:

### User situation

> "I am a student from Maharashtra. My family income is ₹2.5 lakh per year and I need ₹1 lakh for college fees."

A basic search system might return several scholarships.

Jansathi aims to go further:

```text
Understand the situation
        ↓
Identify relevant information
        ↓
Ask only necessary questions
        ↓
Check available support
        ↓
Evaluate eligibility
        ↓
Compare support options
        ↓
Build possible support combinations
        ↓
Estimate remaining financial gap
        ↓
Explain why each option matters
        ↓
Recommend next actions based on the available data
```

The goal is to turn **information discovery into structured decision support.**

---

# 4. Target Users

Jansathi is designed for people who may need assistance but do not know where to start.

Potential users include:

- Students
- Farmers
- Job seekers
- Families
- Small business owners
- Entrepreneurs
- Low-income households
- People looking for healthcare assistance
- People seeking housing support
- People looking for skill-development opportunities
- Individuals seeking financial assistance

The platform is intended to be understandable even for users who are not familiar with government portals or complex application processes.

---

# 5. Solution — Jansathi

## One Need. Multiple Support Paths.

Jansathi is an AI-assisted decision-support platform that starts with the **user's need**, rather than requiring the user to already know the name of a scheme.

Instead of asking:

> "Which scheme are you looking for?"

Jansathi asks:

> **"What do you need help with?"**

The system then builds an understanding of the user's situation and identifies relevant support opportunities.

---

# 6. How Jansathi Solves the Problem

## Step 1 — Tell Jansathi Your Need

The user can describe their situation naturally.

Example:

> "I am a student from Maharashtra. My family income is ₹2.5 lakh per year and I need ₹1 lakh for college fees."

The user does not need to know the name of a scholarship or scheme.

---

## Step 2 — Understand the User

Jansathi converts the user's natural-language description into structured information.

For example:

```text
Category:
Education

Location:
Maharashtra

User Type:
Student

Annual Family Income:
₹2.5 lakh

Required Amount:
₹1 lakh

Purpose:
College fees
```

AI is used for natural-language understanding and clarification.

---

## Step 3 — Ask Relevant Questions

Instead of presenting a long form, Jansathi asks only questions that are relevant to the user's situation.

Examples:

- What is your education level?
- Which state do you live in?
- What is your annual family income?
- Are you currently enrolled in an institution?
- Do you belong to any applicable category?
- Do you already receive another scholarship?

This makes the process more conversational and accessible.

---

# 7. Eligibility Intelligence

Jansathi evaluates support opportunities using structured eligibility rules.

Each opportunity can produce a status such as:

```text
ELIGIBLE
POTENTIALLY_ELIGIBLE
NOT_ELIGIBLE
INSUFFICIENT_INFORMATION
```

This allows the platform to distinguish between:

### Eligible

The available information satisfies the defined eligibility conditions.

### Potentially Eligible

Some information matches, but additional verification is required.

### Not Eligible

The available information conflicts with a defined eligibility requirement.

### Insufficient Information

There is not enough information to make a reliable determination.

---

# 8. Decision Intelligence

Jansathi does not simply display opportunities.

It can organize them using a structured decision model.

The current decision engine considers:

| Factor | Weight |
|---|---:|
| Eligibility | 30% |
| Need Relevance | 25% |
| Potential Support Coverage | 20% |
| Deadline Urgency | 10% |
| Document Readiness | 10% |
| Application Effort | 5% |

These weights are part of the deterministic decision engine and are separate from the AI language layer.

The purpose is to make the reasoning behind the support-plan generation more transparent.

---

# 9. Multiple Support Paths

One of Jansathi's central concepts is that a user's need may not always be solved by a single program.

For example:

```text
Total Need
₹1,00,000

        │
        ├── Scholarship
        │      ₹50,000
        │
        ├── Education Assistance
        │      ₹20,000
        │
        └── Other Eligible Support
               ₹10,000

Potential Support
₹80,000

Remaining Gap
₹20,000
```

Instead of asking:

> "Which single scheme solves everything?"

Jansathi can explore:

> **"What combination of available support paths could help address the user's need?"**

This is the basis of the platform's **Support Path Optimizer**.

---

# 10. Funding Gap Analysis

Jansathi can calculate the difference between:

```text
User's Need
        -
Potential Support
        =
Remaining Gap
```

Example:

```text
Required:
₹1,00,000

Potential Support:
₹80,000

Remaining Gap:
₹20,000
```

This gives the user a clearer understanding of their situation.

The platform does not claim that potential support is guaranteed funding. Users are instructed to verify actual eligibility, deadlines, documents, and approval with the official source.

---

# 11. What-If Simulation

Real-world applications do not always succeed.

Jansathi therefore includes a **What-If** concept.

Example:

> "What if my scholarship is rejected?"

The system can recalculate the available support paths and remaining gap using the scenario.

Example:

```text
Original Plan

Scholarship       ₹50,000
Assistance        ₹20,000
Other Support     ₹10,000
--------------------------------
Potential Support ₹80,000

Gap                ₹20,000
```

After scholarship rejection:

```text
Remaining Support

Assistance        ₹20,000
Other Support     ₹10,000
--------------------------------
Potential Support ₹30,000

New Gap            ₹70,000
```

This helps users understand the consequences of changes in their support plan.

---

# 12. Explainable Results

Jansathi is designed to explain results in plain language.

Instead of simply showing:

> "Eligibility Score: 82"

the system should explain:

- Why the opportunity appears relevant.
- Which eligibility conditions matched.
- Which information is still missing.
- What documents may be required.
- What the user should verify.
- What the next action is.

This makes the system more understandable to ordinary users.

---

# 13. AI + Deterministic Logic

A key design principle of Jansathi is:

> **AI assists understanding; deterministic logic controls decision calculations.**

### AI is responsible for:

- Natural-language understanding
- Intent extraction
- Clarifying questions
- Multilingual conversation
- Plain-language explanations
- Conversational assistance

### Deterministic engines are responsible for:

- Eligibility evaluation
- Decision scoring
- Support calculations
- Funding-gap calculations
- Scenario calculations
- Support-path optimization

This separation reduces the risk of allowing a language model to invent numerical eligibility results.

---

# 14. Accessibility and Simplicity

Jansathi is designed for common users rather than only technically experienced users.

The interface focuses on:

- Large readable typography
- Spacious layouts
- Clear buttons
- Simple language
- Visual hierarchy
- Responsive design
- Mobile usability
- English
- Hindi
- Hinglish
- Reduced-motion accessibility
- Clear status indicators

The objective is to make a complex decision process feel simple.

---

# 15. Main User Journey

```text
┌──────────────────────┐
│   User Has a Need    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Tell Jansathi        │
│ What You Need        │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Understand User      │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Ask Relevant         │
│ Questions            │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Build User Profile   │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Find Support         │
│ Opportunities        │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Check Eligibility    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Compare Options      │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Build Support Paths  │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Calculate Gap        │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Explain Results      │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Next Actions         │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ What-If Scenarios    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Track Applications   │
└──────────────────────┘
```

---

# 16. Key Features

## 🧭 Need-Based Discovery

Start from the user's problem instead of the name of a scheme.

## 🤖 AI Assistance

Understand natural-language requests and communicate in accessible language.

## 📝 Adaptive Questions

Ask relevant questions instead of forcing users through unnecessary forms.

## 🔎 Support Discovery

Identify relevant scholarships, schemes, grants, subsidies, loans, and other opportunities.

## ✅ Eligibility Intelligence

Classify opportunities using transparent eligibility statuses.

## 🧠 Decision Engine

Process multiple factors to organize relevant support opportunities.

## 🛣️ Support Path Optimizer

Explore combinations of support instead of relying on a single opportunity.

## 💰 Gap Calculator

Show potential support versus the user's stated need.

## 🔄 What-If Simulation

Recalculate the support plan when circumstances change.

## 📄 Application Tracking

Allow users to keep track of applications and their status.

## 💬 Ask Jansathi

Provide a conversational interface for questions about the user's support journey.

## 🌐 Multilingual Experience

Support English, Hindi, and Hinglish interactions.

---

# 17. Example Use Case

## Problem

A student needs ₹1,00,000 for education.

They do not know which scholarships or assistance programs they may qualify for.

## Traditional Approach

The student may have to:

```text
Search Google
   ↓
Open multiple websites
   ↓
Read eligibility conditions
   ↓
Compare schemes
   ↓
Collect documents
   ↓
Calculate possible support
   ↓
Choose applications
   ↓
Track them separately
```

## Jansathi Approach

```text
Tell Jansathi the need
        ↓
Answer relevant questions
        ↓
Receive structured opportunities
        ↓
Understand eligibility
        ↓
See potential support
        ↓
See remaining gap
        ↓
Explore alternatives
        ↓
Take next actions
```

---

# 18. Expected Impact

Jansathi is designed to reduce the gap between **available support** and **accessible support**.

The platform aims to help users:

- Discover opportunities they may not know about.
- Understand eligibility more easily.
- Reduce time spent searching across multiple sources.
- Compare different forms of support.
- Understand potential financial coverage.
- Prepare for applications.
- Plan alternatives when an application fails.
- Track their support journey in one place.

---

# 19. What Makes Jansathi Different

Jansathi is not intended to be just:

- A search engine
- A scheme directory
- A chatbot
- A static eligibility checker
- A list of government programs

Instead, it combines:

```text
Natural Language Understanding
            +
Structured User Profile
            +
Eligibility Intelligence
            +
Decision Intelligence
            +
Support Path Optimization
            +
Funding Gap Analysis
            +
What-If Simulation
            +
Application Tracking
```

This creates a complete decision-support workflow.

---

# 20. Responsible Use

Jansathi is a decision-support system.

It should not be presented as an official government portal or as a guarantee that a user will receive a particular benefit.

Information about:

- Eligibility
- Deadlines
- Required documents
- Funding amounts
- Application procedures

should be verified with the relevant official source before the user applies.

Demo opportunities in the MVP should be clearly labeled as **DEMO DATA**.

---

# 21. Vision

The long-term vision of Jansathi is to make support discovery more human-centered.

Instead of forcing people to understand complicated systems first, the platform starts with the person's situation.

### Traditional model

```text
Program
   ↓
Eligibility
   ↓
User
```

### Jansathi model

```text
Person
   ↓
Need
   ↓
Situation
   ↓
Possible Support
   ↓
Eligibility
   ↓
Support Paths
   ↓
Action
```

The goal is simple:

> **Help people move from "I need help" to "I understand my options and know what to do next."**

---

# 22. Project Summary

**Project Name:** Jansathi

**Tagline:** One Need. Multiple Support Paths.

**Category:** Civic Technology / AI / Decision Intelligence

**Primary Purpose:** Need-based support discovery and decision assistance

**Core Technologies:**

- AI / LLM
- JavaScript
- HTML
- CSS
- PostgreSQL
- Hatchable
- Deterministic decision engines

**Core Engines:**

- Eligibility Engine
- Decision Engine
- Support Path Optimizer
- AI Understanding Layer
- AI Explanation Layer
- What-If Simulation

---

## Final Statement

Jansathi addresses a practical problem:

> **People may have access to multiple forms of support, but finding, understanding, combining, and acting on that support can be difficult.**

Jansathi transforms this process into a guided decision journey.

```text
NEED
 ↓
UNDERSTAND
 ↓
DISCOVER
 ↓
CHECK
 ↓
COMPARE
 ↓
PLAN
 ↓
SIMULATE
 ↓
ACT
 ↓
TRACK
```

**Jansathi — One Need. Multiple Support Paths.**
