# 🚀 Algo Arena AI

> **An AI-powered competitive programming and developer learning platform built for problem solving, assessments, skill development, and career growth.**

---

## 🏗️ System Architecture

```text
┌─────────────────────────────────────────────────────────────┐
│                    ALGO ARENA AI                            │
│                 Next.js + React + TypeScript                │
│                    App Router + Tailwind                    │
└─────────────────────────────┬───────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                       APP SHELL                             │
│                                                             │
│        Sidebar        │       Header       │   Main Content │
└───────────────────────┬─────────────────────────────────────┘
                        │
          ┌─────────────┴─────────────┐
          │                           │
          ▼                           ▼
┌─────────────────────┐     ┌─────────────────────────┐
│    UI COMPONENTS    │     │    FEATURE SCREENS      │
│                     │     │                         │
│ Button              │     │ Problems                │
│ Card                │     │ Contests                │
│ Input               │     │ AI                      │
│ Modal               │     │ Dashboard               │
│ Badge               │     │ Profile                 │
│ Toast               │     │ Skills                  │
│ Loading / States    │     │ Assessments             │
└──────────┬──────────┘     │ Projects                │
           │                │ Interviews              │
           │                └────────────┬────────────┘
           │                             │
           └──────────────┬──────────────┘
                          ▼
                 ┌─────────────────┐
                 │  API INTEGRATION │
                 │    /api/v1/*    │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │    NestJS API   │
                 └────────┬────────┘
                          │
              ┌───────────┴───────────┐
              ▼                       ▼
       ┌──────────────┐        ┌──────────────┐
       │ PostgreSQL   │        │    Redis     │
       │              │        │              │
       │ System of    │        │ Cache        │
       │ Record       │        │ Queue        │
       │              │        │ State        │
       └──────┬───────┘        └──────┬───────┘
              │                       │
              │                ┌──────┴──────┐
              │                ▼             ▼
              │          AI Workers     Judge Workers
              │                │             │
              │                ▼             ▼
              │               AI      Secure Sandbox
              │
              ▼
        Core Application
           Modules
```

---

# 💻 Frontend Stack

| Technology | Purpose |
|---|---|
| **Next.js** | Frontend framework |
| **React** | UI development |
| **TypeScript** | Type-safe development |
| **App Router** | Application routing |
| **Tailwind CSS** | Styling & responsive UI |
| **ESLint** | Code quality |
| **Turbopack** | Development bundler |

---

# 🎨 Design System

The frontend is being developed around a reusable design system.

```text
Design System
│
├── Design Tokens
│   ├── Colors
│   ├── Typography
│   ├── Spacing
│   ├── Border Radius
│   └── Shadows
│
└── UI Primitives
    ├── Button
    ├── Card
    ├── Input
    ├── Modal
    ├── Toast
    ├── Badge
    └── States
```

### Design Principles

- Consistent visual language
- Reusable components
- Responsive-first development
- Accessibility-friendly UI
- Clear interaction states
- Scalable component architecture

---

# 🧩 Core Application Modules

```text
apps/api/src/modules/

├── auth/
├── users/
├── profiles/
├── problems/
├── submissions/
├── judge/
├── contests/
├── ratings/
├── skills/
├── recommendations/
├── ai/
├── research/
├── variants/
├── sql/
├── dbms/
├── system-design/
├── interviews/
├── projects/
├── collaboration/
├── community/
├── notifications/
├── organizations/
├── career/
├── billing/
├── integrity/
├── admin/
└── analytics/
```

---

# 🔌 API Contract

### Health

```http
GET /api/v1/health
```

### Authentication

```http
POST /api/v1/auth/register
POST /api/v1/auth/login
POST /api/v1/auth/logout
```

### User

```http
GET /api/v1/me
```

### Problems

```http
GET  /api/v1/problems
GET  /api/v1/problems/:slug
POST /api/v1/problems/:id/submissions
GET  /api/v1/submissions/:id
```

### Challenges

```http
GET /api/v1/daily-challenge
```

### Contests

```http
GET /api/v1/contests
GET /api/v1/contests/:slug
```

---

# 📦 Standard API Response

### Success

```json
{
  "success": true,
  "data": {},
  "message": "Request successful",
  "error": null,
  "requestId": "..."
}
```

### Error

```json
{
  "success": false,
  "data": null,
  "message": "Validation failed",
  "error": {
    "code": "VALIDATION_ERROR",
    "details": []
  },
  "requestId": "..."
}
```

---

# ⚡ Domain Events

### User

```text
user.created
user.onboarded
```

### Problems & Submissions

```text
problem.created
problem.published

submission.created
submission.queued
submission.started
submission.completed
```

### Skills & Recommendations

```text
skill.updated
recommendation.created
```

### AI

```text
ai.job.created
ai.job.completed
ai.job.failed
```

### Contests

```text
contest.joined
contest.submitted
contest.completed
```

### Assessments

```text
assessment.started
assessment.completed
```

### Projects

```text
project.created
project.completed
```

---

# 🔐 Roles & Permissions

### Roles

```text
USER
AUTHOR
MENTOR
MODERATOR
ADMIN
ORGANIZATION_ADMIN
RECRUITER
```

### Problem Permissions

```text
problem.read
problem.create
problem.edit
problem.publish
```

### Submission

```text
submission.create
```

### Contest

```text
contest.create
contest.manage
```

### Assessment

```text
assessment.create
```

### Organization

```text
organization.manage
```

### Moderation

```text
user.moderate
```

---

# 🔒 Content Visibility

The platform supports multiple visibility levels:

```text
PRIVATE
PUBLIC
UNLISTED
ORGANIZATION_ONLY
```

Supported content types include:

```text
Profile
Submission
Contest
Project
Skill Passport
Assessment
Social Activity
Organization Content
```

---

# 📅 Today's Development Target

## Algo Arena AI Web

```text
Algo Arena AI Web
│
├── App Shell
│   ├── Sidebar
│   ├── Header
│   └── Main Content
│
├── Design Tokens
│   ├── Colors
│   ├── Typography
│   ├── Spacing
│   ├── Radius
│   └── Shadows
│
└── UI Primitives
    ├── Button
    ├── Card
    ├── Input
    ├── Modal
    ├── Toast
    ├── Badge
    └── States
```

---

# ⚙️ Frontend Initialization

The Next.js application was initialized using:

```bash
cd /workspaces/Algo-Arena-Ai

ls apps/web

npm exec --yes create-next-app@latest apps/web
```

### Configuration

```text
TypeScript       → Yes
ESLint           → Yes
Tailwind CSS     → Yes
src/ Directory   → Yes
App Router       → Yes
Turbopack        → Yes
Import Alias     → Yes
Alias            → @/*
```

---

# 🛣️ Development Roadmap

### P1 — UI Foundation

- [ ] App Shell
- [ ] Sidebar
- [ ] Header
- [ ] Main Layout
- [ ] Design Tokens
- [ ] UI Primitives
- [ ] Responsive foundation

### P2 — API Integration

- [ ] Define API client
- [ ] Integrate API contracts
- [ ] Authentication flow
- [ ] Problem APIs
- [ ] Submission APIs
- [ ] Error handling
- [ ] Loading states

### P3 — AI Features

- [ ] AI Dashboard
- [ ] AI-powered problem assistance
- [ ] Recommendation components
- [ ] AI job states
- [ ] AI result interface
- [ ] AI component architecture

### P4 — Quality & Production Readiness

- [ ] Responsive optimization
- [ ] Accessibility
- [ ] UI testing
- [ ] Error boundaries
- [ ] Performance optimization
- [ ] Production build validation

---

# ▶️ Run the Web Application

Using pnpm:

```bash
pnpm --filter web dev
```

The development workflow is based on a **monorepo architecture**, keeping the web application and backend services modular and independently scalable.

---

# 🎯 Current Focus

> **Build the frontend foundation first.**

The immediate priority is to create a **clean, scalable and reusable UI architecture** before connecting the complete backend.

```text
UI Foundation
      ↓
Reusable Components
      ↓
Feature Screens
      ↓
API Integration
      ↓
AI Features
      ↓
Testing & Accessibility
      ↓
Production
```

---

## 🚀 Vision

**Algo Arena AI** aims to become a unified platform where developers can:

- Practice programming
- Participate in contests
- Submit and evaluate code
- Track technical skills
- Take assessments
- Build projects
- Prepare for interviews
- Use AI-powered learning tools
- Discover personalized recommendations
- Build a developer-focused profile

> **Learn. Practice. Build. Compete. Grow.**
